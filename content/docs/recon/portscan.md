# Port Scan

```
# https://github.com/nmap/nmap
./configure
make
make install
```

```
# https://github.com/projectdiscovery/naabu
naabu -p 80,443,21-23 -host example.com
naabu -list hosts.txt
cat lists | naabu -silent
echo example.com | naabu -nmap-cli 'nmap -sC -sV -oX nmap-output'
```
