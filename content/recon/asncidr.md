# ASN

An autonomous system number (ASN) is a unique identifier that allows its autonomous system to exchange routing information with other systems.

The five regional Internet registries are:

    African Network Information Center (AFRINIC)
    American Registry for Internet Numbers (ARIN)
    Asia-Pacific Network Information Centre (APNIC)
    Latin American and Caribbean Network Information Centre (LACNIC)
    Réseaux IP Européens Network Coordination Centre (RIPE NCC)

## Obtaining an ASN (autonomous system number)

### By Organization Name

- https://asrank.caida.org/asns/by-name/
- http://asnlookup.com

## ASN Lookup tools 

- https://www.bigdatacloud.com/asn-lookup/{ASN}
- https://bgp.he.net/{ASN}
- https://ipinfo.io/{ASN}
- https://bgpview.io/asn/{ASN}
- https://whois.ipip.net/{ASN}

# CIDR analysis

- https://whois.ipip.net/cidr/
- https://rdnsdb.com/
- https://www.robtex.com/
- https://bgp.tools/
- https://rapiddns.io/

## CIDR range to IP list

```
# https://github.com/robertdavidgraham/masscan
masscan -iL list-of-cidrs -oG output --rate 10000 -p 80,8443,443,8080
```

## Reverse CIDRs, IPs to domains

```
# https://github.com/projectdiscovery/tlsx
cat list | tlsx -san -cn -silent -resp-only
```

# IP information

- https://ipinfo.io
- https://www.dnsgrep.cn
- https://rdnsdb.com/
- https://db-ip.com/

# Whois

- https://www.whatsmydns.net/domain-name-owner
- https://tools.whoisxmlapi.com/reverse-whois-search (reverse whois, paid)
- https://www.whoxy.com/ (whois history)

## Whois checking:

- https://github.com/melbadry9/WhoEnum
