# Active Resources

The ideia behind an active subdomain recon is to bruteforce subdomain in order to find anything that is valid.

Get resolvers at:
```
RESOLVER_SOURCE
```

## Pure DNS

```
# https://github.com/d3mondev/puredns
puredns resolve subdomains.txt -r resolvers.txt --write resolved_dns_domains

puredns bruteforce subdomains.txt example.com -r resolvers.txt --write resolved_dns_domains
```

## Permutations

```
# https://github.com/Josue87/gotator
gotator -sub subdomains/subdomains.txt -perm permutations_list.txt -depth 1 -numbers 10 -mindup -adv -md
```

