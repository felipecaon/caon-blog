# Parameter Discovery

There are two tools that I prefer when doing param scanning. X8, which is a tool made just for param discovery with advanced comparison and arjun, which does basically the same. From my tests I could not determine which one is better.

## X8

```
# https://github.com/Sh1Yo/x8

x8 -u "https://example.com/" -w <wordlist>
```

## Arjun

```
# https://github.com/s0md3v/Arjun

arjun -u https://target.com/ -w <wordlist>
```

## Param discovering from crawling results

Given a list with crawled urls, grep the ones that have known parameters and get only the url

```
# https://github.com/tomnomnom/unfurl

cat list.txt | grep "=" | unfurl format %d%p 
```

## Feed discovered parameters back to a param list

See [Wordlist generation](https://caon.io/docs/recon/wordlistgeneration/)
