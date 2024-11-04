+++
title = 'Probing'
+++

Validates a list of urls, checks to see if they are alive or not.

## httpX

```
# https://github.com/projectdiscovery/httpx
# go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest
cat urls | httpx -random-agent -retries 2 -o out
```

{{< hint danger >}} **Hold down!**

httpX fails to retrieve all good working urls in a single run. It is recommended to run httpx more than once to achieve better results. {{< /hint >}}
