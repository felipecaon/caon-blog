## katana

```
# go install github.com/projectdiscovery/katana/cmd/katana@latest
cat hosts | katana -jc -kf all -nc -ef png,jpg,jpeg,css,gif,ttf,woff,woff2,svg,eot
```

## Find records

```
# https://github.com/projectdiscovery/dnsx
dnsx -retry 3 -a -aaaa -cname -ns -ptr -mx -soa -resp -silent -l subdomains.txt > dnsx_info.txt
```

## Webpaste chrome extension

```
# https://github.com/xnl-h4ck3r/webpaste
```
