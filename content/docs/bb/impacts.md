# Impacts

## SQLi

Attacker can obtain full database access holding private user information and other sensitive data.
An attacker can use information gathered in SQLi to login in admin panels and obtain access to private and sensitive information.

## XSS

A successful exploitation of a XSS allows an attacker to execute arbitrary JavaScript code in the victim's browser, allowing the attacker to steal cookies, tokens or any other sensitive information. 
It is also possible to inject code into the page, allowing the possibiliy of: phishing attacks, redirects and code manipulation.

## LFI

An attacker can read local files on the web server that should not be accessed, such as the application source code or configuration files containing sensitive information.

## Amazon Cognito Identity

Unauthorized access to AWS services with temporary user.
An attacker can genereate a temporary guest token to peek - and maybe exploit - the company infrastructure.

## ATO - password reset

An attacker can log into any account by just knowing it's email address.

## Open redirect

An attacker can send the link to users to get them redirected to a malicious domain.
To achieve success an attacker must trick vicitims into visiting the crafted URL.

## Sensitive README.md exposed

Information that is not supposed to be public became public due to misconfigurations.
Attacker can use information leaked to learn more about company internals.
