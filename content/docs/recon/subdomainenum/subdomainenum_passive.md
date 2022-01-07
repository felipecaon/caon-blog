## Passive Resources

A passive resource means that you will grab subdomains that were already discovered from another tools or were registered in some place.

```
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
gau -subs example.com | unfurl -u domains

# https://github.com/gwen001/github-subdomains
# Need to configure github keys
github-subdomains -d example.com
```

## All in one script

```tpl
amass enum -passive -d domain.com -o amass_$1.txt > /dev/null 2>&1
echo "[+] Amass finalizado"

subfinder -silent -d $1 -o subfinder_$1.txt > /dev/null 2>&1
echo "[+] Subfinder finalizado"

findomain -t $1 -u findomain_$1.txt > /dev/null 2>&1
echo "[+] Findomain finalizado"

github-subdomains -d $1 -o github_$1.txt > /dev/null 2>&1
echo "[+] Github subdomains finalizado"

assetfinder -subs-only $1 > assetfinder_$1.txt
echo "[+] Assetfinder finalizado"

cat subfinder_$1.txt findomain_$1.txt github_$1.txt assetfinder_$1.txt amass_$1.txt | uniq $1_subdomains
rm subfinder_$1.txt findomain_$1.txt github_$1.txt assetfinder_$1.txt amass_$1.txt
```

## Third party websites

The following list contains sites that may have additional subdomains:


- https://chaos.projectdiscovery.io/
- https://phpinfo.me/domain/
- http://tool.chinaz.com/subdomain
- https://site.ip138.com/example.com/domain.html
- https://spyse.com/target/domain/example.com/subdomain-list
