---
title: About Takahē
---

Takahē is an ActivityPub server focused on microblogging, much like Mastodon,
Pleroma, and others. Our goals are:

* Allowing multiple domains on the same server ("virtual hosting")
* Efficient, stable background tasks via asynchronous state machines
* A default fast, low-JavaScript web interface
* Mastodon Client API compatibility (eventually!)


## Why start another server?

The main motivation was to prove two things - that virtual hosting of multiple
domains on a single ActivityPub server was possible (so you don't need
to run a whole new server for every person or organisation that brings their
own domain), and to explore the use of Python's asynchronous libraries to
speed up the large amount of background work ActivityPub involves.

Fortunately, both of those have proved themselves to work well in the initial
build-out phase, and so now development is focused towards a small, reliable,
stable release.

While we do not expect to grow as large and featureful as Mastodon, the goal
is to provide a smaller, lighter-weight server that is useful for small- to
medium-size instances. The architecture we've chosen is deliberately easy to
run and maintain but will not scale to a large install, and that's fine.

## More Insight

Takahē is, so far, mostly authored by [Andrew Godwin](https://aeracode.org/),
and you can read more about its development, choices made, and progress via
[my blog posts](https://aeracode.org/category/takahe).
