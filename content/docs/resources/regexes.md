# Regexes

## Subdomain level extraction

| Regex pattern | Domain level match |
| --- | --- |
| grep -P '^(?:[a-z0-9]+.){N}[^.]*$' | Nnd level domains only |
| grep -P '^(?:[a-z0-9]+.){2,3}[^.]*$' | 3rd to 4th level domains only |
| grep -P '^(?:[a-z0-9]+.){3,}[^.]*$' | 4th level domains or higher |
