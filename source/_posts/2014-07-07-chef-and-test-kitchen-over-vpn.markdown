---
layout: post
title: "Chef and Test Kitchen over VPN"
date: 2014-07-07 20:09:04 -0700
comments: true
categories: chef test-kitchen
---

Been fighting with DNS over VPN really killing my local chef testing from home. After some digging around you need to set this in the kitchen.yml (or kitchen.local.yml):

``` yaml kitchen.yml
driver_config:
# ...
  customize:
    natdnshostresolver1: "on"
```

Hopefully this will save someone a headache.
