# Passive Resources

A passive resource means that you will grab subdomains that were already discovered by another tools or were found lying around in some place (open source code, legacy scripts, logs, etc).

```bash
# https://github.com/OWASP/Amass
amass enum -passive -d domain.com

# https://github.com/projectdiscovery/subfinder
subfinder -d domain.com -all -silent

# https://github.com/tomnomnom/assetfinder
assetfinder --subs-only example.com

# https://github.com/Findomain/Findomain
findomain -u example.com -q

# https://github.com/lc/gau
# https://github.com/tomnomnom/unfurl
gau --subs example.com | unfurl -u domains
```

```
# https://github.com/ARPSyndicate/puncia
puncia subdomain <domain>
```

## All in one script

```bash
amass enum -passive -d $1 -o amass_$1.txt > /dev/null 2>&1
echo "[+] Amass done"

subfinder -silent -d $1 -all -o subfinder_$1.txt > /dev/null 2>&1
echo "[+] Subfinder done"

findomain -t $1 -u findomain_$1.txt > /dev/null 2>&1
echo "[+] Findomain done"

assetfinder -subs-only $1 > assetfinder_$1.txt
echo "[+] Assetfinder done"

cat subfinder_$1.txt findomain_$1.txt assetfinder_$1.txt amass_$1.txt | uniq $1_subdomains
rm subfinder_$1.txt findomain_$1.txt assetfinder_$1.txt amass_$1.txt
```

## Google analytics ID

Extract Google tag manager from webiste, format: `UAXXXXXX`

- https://builtwith.com/relationships/tag/UAXXXXXX
- https://api.hackertarget.com/analyticslookup/?q=UAXXXXXX
- https://spyonweb.com/UAXXXXXX

```
# https://github.com/Josue87/AnalyticsRelationships
cat subdomains.txt | analyticsrelationships
```

## Google Tag Manager

```
https://googletagmanager.com/gtm.js?id=TAGID
```

## Favicon

Search for favicon md5 value in known search engines to find websites related to your search

```
Tip: Use http.favicon.hash:<hash> on Shodan
```

See more shodan dorks here: https://github.com/dootss/shodan-dorks
