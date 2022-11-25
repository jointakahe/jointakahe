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

## About The Takahē

The Takahē, after which this project is named, is a
[flightless bird from Aotearoa New Zealand](https://en.wikipedia.org/wiki/Takah%C4%93) -
once thought extinct, but in recent decades they were rediscovered and have
been the subject of a successful breeding and reintroduction programme.

If you'd like to donate to their cause, you can give money through
the [New Zealand Nature Fund](https://nznaturefund.org/projects/takahe-recovery-programme/).
