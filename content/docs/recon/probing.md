# Probing

Validates a list of urls, checks to see if they are alive or not.

Two tools were provided, choose the best fit, they do the same thing.

## Httprobe

```
# https://github.com/tomnomnom/httprobe/
# go get -u github.com/tomnomnom/httprobe@master
cat urls | httprobe --prefer-https | tee -a out

# HttpX

# https://github.com/projectdiscovery/httpx
# go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest
cat urls | httpx -random-agent -retries 2 -o out
```
