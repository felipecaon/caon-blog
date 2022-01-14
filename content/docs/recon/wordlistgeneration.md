# Wordlist generation

After spidering across the target it is a good idea to check the content discovered and append the newly discovered content to your wordlist.


## Parameters
```
# https://github.com/tomnomnom/anew

cat links.txt | unfurl -u keys | anew all_parameters.txt
```

## Paths
```
cat links.txt | unfurl paths | rev | cut -d '/' -f1 | rev | anew paths.txt
```



