+++
title = "How to find someone across social media networks"
description = ""
date = "2019-03-09"
categories = [
    "OSINT",
]
menu = "main"
+++

Online awareness is important. In the last twenty years the internet evolved to something that is way bigger than their initial purpose and here we are.

We used it every day for everything and most of us don’t even care about what we do online or what possible outcomes can appear after doing something.


This article focuses on your online identity, specifically in your social network presence. Are you doing it right?

It is convenient to have the same username across every site. I’d love to have my username ImTheGuyWhoDances in Facebook, Twitter, Myspace, Reddit and Instagram! All my friends could find me with one click, magical!


From a security perspective, it is not right. Using the same username an attacker can easily discover more about you and most of the times proceed with their plan to make your live miserable.

Example: You have an account on Twitter with username MrMouseClicker23. The attacker can bulk search in another websites for the same usernames and find more about you, maybe finding your password in a breach [websites get hacked all the time](https://haveibeenpwned.com/).


## Presenting Comperio

Comperio is a reconnaissance tool that makes it super easier to find people using equal usernames across social networks. Currently supporting 80+ social network sites, it supports the most used websites in the world.

## Installation procedure:

```python
# clone this repo
git clone https://github.com/felipecaon/comperio.git

# change path
cd comperio/

# run comperio
python3 comperio.py user1 user2 ...
```

## Output

The output is straight forward, it generates a file with the websites that have the username listed in their databases.

![](/comperio.png)

Of course, looking from the initial perspective, one will only do it if the person has bad intentions. But no!

## From another perspective:

- Security firms can find if their clients are compromised before the bad guys do.

- [Bad guys can be found too!](https://krebsonsecurity.com/2019/02/bomb-threat-hoaxer-exposed-by-hacked-gaming-site/)

- Thinking about creating a brand name? You can check if the name is already taken.

- Open Source Intelligence. Terrorists can be found using this technique, [jester has done it a couple of times.](https://twitter.com/th3j35t3r)
