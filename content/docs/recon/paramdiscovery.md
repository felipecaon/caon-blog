# Parameter Discovery

There are two tools that I prefer when doing param scanning. X8, which is a tool made just for param discovery with advanced comparison and ffuf, which is a general fuzzing tool that can be used for single param testing.


# https://github.com/Sh1Yo/x8
x8 -u "https://example.com/" -w <wordlist>
```

```
# https://github.com/ffuf/ffuf
ffuf -w /path/to/paramnames.txt -u https://target/script.php?FUZZ=test_value
```

## Param discovering from crawling results

Given a list with crawled urls, grep the ones that have known parameters and get only the url

```
# https://github.com/tomnomnom/unfurl

cat list.txt | grep "=" | unfurl format %d%p 
```

## Feed discovered parameters back to a param list

Given a list with crawled urls, grep only the parameter keys and feed back to a param list

```
# https://github.com/tomnomnom/anew
cat list.txt | unfurl keys | anew ~/path/to/param/wordlist
```
