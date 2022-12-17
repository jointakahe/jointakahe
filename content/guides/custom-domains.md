---
title: Custom Domains Guide
---

So you want to point a custom domain at takahe.social? Great! Before you start,
you need to understand a few things:

* Custom domains are limited and available by request only. Email
  contact@jointakahe.org to request one; we may or may not have capacity.
  Each custom domain is administrative and operational overhead for us.

* Once you make accounts (identities) on your custom domain, you will not be
  able to move them away from takahe.social until we implement the move
  feature in the future. Even then, your posts will not follow you, only
  your followers.

* Custom domains are not separate servers - you will still be on the same
  "server" as everyone else, see everyone else in the Local feeds, use our
  global set of server emoji, and be subject to our moderation policies and
  rules.

If you're alright with that, then let's discuss how to set up your domain.

There's two ways you can route a domain to us:

* Pointing the whole domain at takahe.social. This is the easiest way, but
  it means you will not be able to use that domain for anything else
  (for example, if you want `@user@sub.domain.tld` to be your handle, you must
  point the entirely of `sub.domain.tld` at us and nothing else can exist on it).

* Routing users from a main domain to a Takahē-specific subdomain.
  This is generally preferred, as it lets you have `@user@domain.tld` work, while
  still serving a different website on `domain.tld`. Takahē will serve requests
  from a subdomain like `takahe.domain.tld`.

Please understand that once you have selected one of these options it
**cannot be changed** without you losing all your follows. Unless you are very
sure what you are doing, **we suggest using a Takahē-specific subdomain**.

You will be able to log into Takahē using the same credentials either at
[takahe.social](https://takahe.social) or under your custom domain; it will
work the same either way.


## Whole Domain

To point a whole domain at us, you need to add a DNS CNAME from that domain
to `takahe.social`.

If you are trying to point an apex domain that does not
support CNAMEs, you can make an A record that points to our IP address
of `104.198.180.195`. This IP may change as we get our network setup fully
stabilised; we will try and let you know via email when this is going to
happen.

Note that no subdomains of the domain you provide will work, not even `www`,
as we will only issue an SSL certificate for the exact one you provide.


## Takahē-Specific Subdomain

To point a subdomain at us, you will need to add a DNS CNAME for it to
`takahe.social`.

If you then want account handles to work off of your main domain, you will
need to proxy through these URLs from that main domain to the subdomain:

* `/.well-known/webfinger`
* `/.well-known/host-meta`
* `/.well-known/nodeinfo`
