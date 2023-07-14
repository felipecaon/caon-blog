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
cat list | naabu -top-ports 100 -ep 80,443,8080,8443
```
