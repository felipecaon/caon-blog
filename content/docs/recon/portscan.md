# Port Scan

## Nmap

```
# https://github.com/nmap/nmap
./configure
make
make install
nmap -sC -sV example.com
nmap example.com
```

- https://3os.org/penetration-testing/cheatsheets/nmap-cheatsheet/

## Naabu

```
# https://github.com/projectdiscovery/naabu
naabu -p 80,443,21-23 -host example.com
naabu -list hosts.txt
cat lists | naabu -silent
echo example.com | naabu -nmap-cli 'nmap -sC -sV -oX nmap-output'
```
