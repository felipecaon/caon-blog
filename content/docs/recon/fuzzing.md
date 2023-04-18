# Fuzzing

{{< hint info >}} **Rate Limited?**

Try to run techniques from [403 Bypass](https://caon.io/docs/exploitation/403bypass/) 
{{< /hint >}}

{{< hint info >}} **Configure your options!**
ffuf runs by default with ffuf custom user agent, some sites will not trust that and return dummy data. 
The solution for this is to implement a .ffufrc file with real headers:

https://gist.github.com/felipecaon/d1e7c980d7bab1312ea81df1d0241f42
{{< /hint >}}


```
# https://github.com/ffuf/ffuf
ffuf -w /path/to/wordlist -u https://target/FUZZ

# Multiple sources
ffuf -w http-methods:METHOD -w payloads:PAYLOAD -w headers:HEADER -u "https://example.com/PAYLOAD" -H "HEADER:127.0.0.1" -X "METHOD"

# Multiple URLs and mutiple files example
ffuf -u URL/FUZZ -w allipstoffuf:URL -w ~/.config/wordlists/envpath:FUZZ -maxtime 300 -t 500 -c -v

# Cool ffuf flags
-ac: Calibrate requests to unmatch false positives
-recursion: recursion
-se: Stop on erors
-sf: Stop on 95% 403 Forbidden, possible WAF ban
```

## Remove noise

Ffuf can generate a large output, even with `-ac` flag enabled. To filter dummy and extract only juicy information, it is possible to use `ffufPostprocessing`

```
# https://github.com/Damian89/ffufPostprocessing
ffufPostprocessing -result-file /tmp/ffuf/results.json -bodies-folder /tmp/ffuf/bodies/ -delete-bodies -overwrite-result-file
```

## Backup Files

Tempers file to find possible backup files based in file name

```
# https://github.com/mazen160/bfac
bfac --no-text --url http://example.com/test.php --level 2
```

## Wordlists

| URL | Description |
|---|---|
|https://github.com/p0dalirius/webapp-wordlists|This repo contains wordlists for a lot of webapps|
|https://github.com/six2dez/OneListForAll|Huge list of paths and files|
|https://github.com/TheKingOfDuck/fuzzDicts| Collection of lists for fuzzing |
| https://github.com/tennc/fuzzdb| Collection of lists for fuzzing |
| https://github.com/the-xentropy/samlists| List of files, paths and parameter based on usage in the wild |
