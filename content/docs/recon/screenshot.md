# Screenshot

For large recons where manual website visit is not doable. The program would grab a list of valid urls and screenshot them using a headless browser.

{{< hint danger >}} **Hold down!**

A browser must be installed prior using an screenshotter. Chrome or chromium is recommended. {{< /hint >}}

## EyeWitness

```
# https://github.com/FortyNorthSecurity/EyeWitness
EyeWitness -f urls.txt --web
```

## GoWitness

```
# https://github.com/sensepost/gowitness
gowitness file -f websites.txt -t <threads> --disable-logging
```

{{< hint info >}} **webscreenshot.py**

webscreenshot is Kopfschmerzen {{< /hint >}}
