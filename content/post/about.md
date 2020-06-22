---
title: "About Mnemonic as a Service"
date: 2020-06-21T22:14:24-04:00
draft: false
---

>There are only two hard things in Computer Science: cache invalidation and naming things.
>
>-- Phil Karlton

Long ago, some folks wrote a [blog post](http://mnx.io/blog/a-proper-server-naming-scheme/) about server naming schemes.  One of the included recomendations was to use Oren Tirosh’s [mnemonic encoding project](http://web.archive.org/web/20090918202746/http://tothink.com/mnemonic/wordlist.html) as a wordlist.

>Oren Tirosh created a wordlist of unique, short words that could be used universally for verbally encoding information.  He described it as the mnemonic encoding project and the resulting 1626 words are great for all kinds of things.

I've now written simple random name generators in many languages and keep this domain around to serve them out.

Today, I am serving the words through a simple Cloudflare Worker that you can access using curl like this:

```bash
curl -i -H "Accept: application/json" -H "Content-Type: application/json" https://mnemonic-as-a-service.com/api/
```