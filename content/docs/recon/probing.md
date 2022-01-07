# Probing

Validates a list of urls, checks to see if they are alive or not.

Two tools were provided, choose the best fit, the do the same thing but in some cases httprobe is faster and resolves more urls correctly.

```
# https://github.com/tomnomnom/httprobe/
# go get -u github.com/tomnomnom/httprobe@master
cat urls | httprobe --prefer-https | tee -a out


# https://github.com/projectdiscovery/httpx
# go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest
cat urls | httpx -random-agent -retries 2 -o out
```
