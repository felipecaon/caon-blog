# Spider


```
# https://github.com/jaeles-project/gospider
gospider -S subdomains.txt --js -t 20 -d 5 --sitemap --robots -r > spider.txt
cat spider.txt | grep -o -E "(([a-zA-Z][a-zA-Z0-9+-.]*\:\/\/)|mailto|data\:)([a-zA-Z0-9\.\&\/\?\:@\+-\_=#%;,])*" | grep "example.com" >> links.txt

# https://github.com/projectdiscovery/httpx
cat links.txt | httpx -follow-host-redirects -random-agent -status-code -silent -retries 2 -title -web-server -tech-detect -location -o webs_info.txt

# https://github.com/projectdiscovery/dnsx
dnsx -retry 3 -a -aaaa -cname -ns -ptr -mx -soa -resp -silent -l subdomains.txt > dnsx_info.txt
```

The list generated from gospider `links.txt` can be used to discover additional subdomains

## Robots

Roboxtractor extract endpoints marked as disallow in robots files to generate wordlists.  
Also has a waybackmachine flag that will hunt robots.txt old versions.

```
# https://github.com/Josue87/roboxtractor
cat subdomains | roboxtractor -m 0 -wb
```
