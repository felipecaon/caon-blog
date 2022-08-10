# Spider


## Crawling

Use gospider or hakrawler. Personally, I found out hakrawler yields better results

## hakrawler

```
# go install github.com/hakluke/hakrawler@latest
cat hosts | hakrawler -t 20
```

## Check if hosts/paths are valid

```
# https://github.com/projectdiscovery/httpx
cat links.txt | httpx -follow-host-redirects -random-agent -status-code -silent -retries 2 -title -web-server -tech-detect -location -o webs_info.txt
```

## Find records

```
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
