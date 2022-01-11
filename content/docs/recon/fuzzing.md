# Fuzzing


```
# https://github.com/ffuf/ffuf
ffuf -w /path/to/wordlist -u https://target/FUZZ

# Multiple sources
ffuf -w http-methods:METHOD -w payloads:PAYLOAD -w headers:HEADER -u "https://streetcontxt.com/PAYLOAD" -H "HEADER:127.0.0.1" -X "METHOD"

#Cool flags

-ac: Calibrate requests to unmatch false positives
-recursion: recursion
-se: Stop on erors
-sf: Stop on 95% 403 Forbidden, possible WAF ban
```
