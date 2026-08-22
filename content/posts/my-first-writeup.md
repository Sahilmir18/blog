+++
title = "Bypassing SSRF:A Walkthrough"
date = "2026-08-22T21:59:27+05:30"
#dateFormat = "2006-01-02" # This value can be configured for per-post date formatting
author = "Sahil Mir"
authorTwitter = "" #do not include @
cover = ""
draft = false
tags = ["pentest", "writeup"]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = false
hideComments = false
+++

## Overview

How to get SSRF? 
SSRF is a vulnerability that tricks the server to making a request to the other website whether its internal or external. Because the request comes from a server the receiver trusts it and makes the data accessible without authentication Because the server is making the request. 

<!--more-->

Eg. YOU WANT TO INFILTRATE A BUILDING but there are security guards everywhere around the building, you manage to make friends with one of the guards and now the guard trusts you as a friend. You make the guard tell other guards to go away so you can infiltrate the building. 

GUARD -> SERVER, YOU -> ATTACKER, BUILDING -> DATABASE. 

Simply, as as ATTACKER(You) you trick the SERVER(Guard) to give commands to other SERVERS(Guards), so YOU(Attacker) can steal the DATABASE(Building).

## Steps

1. Have Burp Suite Ready to intercept traffic
2. look for things you can use to trick the server (eg. api_links)
3. Change the api link to localhost. 
4. Send by Repeater.

```Bash
print(hello world)
```

## Takeaways

What you learned, mitigations, refreneces.