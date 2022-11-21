# Spider


## Crawling

## katana

```
# go install github.com/projectdiscovery/katana/cmd/katana@latest
cat hosts | katana -jc -kf all -nc -ef png,jpg,jpeg,css,gif,ttf,woff,woff2,svg,eot
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
