+++
title = 'Burp Suite'
+++

## Plugins

- Backslash powered scanner, find additional vulns
- JS Miner, gets sensitive content from js files
- Active Scan++, find additional vulns
- JS Link Finder, find links inside javascript files
- Param Miner, mines urls searching for parameters
- Reflector, find reflected inputs

## Tips n Tricks

### Send traffic from VPS to local burp

```
# Run this in terminal connecting to vps (if ssh with key is possible)
# When in WSL, portforwarding needs to be set
ssh -R 8080:127.0.0.1:8080 root@VPS_IP -f -N

# If you are in windows and need to pass passsord, use this
putty.exe -ssh user@host -pw password -R 8080:127.0.0.1:8080

# Visit the sites in VPS
curl URL -x http://127.0.0.1:8080
```

## Repositories

- [AwesomeBurpExtensions](https://github.com/snoopysecurity/awesome-burp-extensions)

## Articles

- [Payload Processing Rule in Burp suite (Part 1)](https://www.hackingarticles.in/payload-processing-rule-burp-suite-part-1/)
- [Payload Processing Rule in Burp suite (Part 2)](https://www.hackingarticles.in/payload-processing-rule-burp-suite-part-2/)
- [Beginners Guide to Burpsuite Payloads (Part 1)](https://www.hackingarticles.in/beginners-guide-burpsuite-payloads-part-1/)
- [Beginners Guide to Burpsuite Payloads (Part 2)](https://www.hackingarticles.in/beginners-guide-burpsuite-payloads-part-2/)
- [How to burp good](https://www.n00py.io/2017/10/how-to-burp-good/)
- [Using burp session handling rules](https://portswigger.net/support/using-burp-suites-session-handling-rules-with-anti-csrf-tokens)
