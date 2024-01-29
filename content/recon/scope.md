A scope can be defined as of the limit of where your research should go, if you ever find a bug, this must reside inside the scope, otherwise, the finding is not valid.

Example of scope

| In-Scope | Out of scope |
|---|---|
|example.com| subdomain.example.com|
|*-dev.example.com||

The scope above states that `example.com` and `www.example.com` are valid (www is a subdomain, example.com points to www by default).

Any subdomain under `-dev.example.com`  is valid as well, the wildcard symbol (*) states that anything is valid. So, `test-dev.example.com`, `app-dev.example.com` are valid but `app.example.com` is not because the subdomain does not have the `-dev`part.

Some programs offer a wildcard scope, in those cases, it is a good idea to keep an eye in Out of scope domains. See the example:

| In-Scope | Out of scope |
|---|---|
|*.website.com| wow.website.com|
||ie.website.com| 


As written, `website.com` has a wildcard scope, meaning every subdomain is valid, except for those who are in the Out of scope list, which are `wow.website.com` and `ie.website.com`
