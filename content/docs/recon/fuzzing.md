# Fuzzing

{{< hint info >}} **Rate Limited?**

Try to run techniques from [403 Bypass](https://caon.io/docs/exploitation/403bypass/) 
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
