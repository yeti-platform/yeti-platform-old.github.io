---
layout: post
cover: 'assets/images/cover2.jpg'
title: Introducing the Yeti
date: 2017-03-10 08:00:00
tags: announcements
subclass: post
author: tomchop
---

After months of hard work, trial and error, and fighting with CSS alignment, we are happy to announce the release of Yeti: Your everyday Threat Intelligence platform. Although originally an independent project, Yeti would not have been able to exist without the team at [CERT Société Générale](https://cert.societegenerale.com/){:target="_blank" class="external"}, who put in countless hours testing the tool and orienting development to best suit their needs.

<!--more-->

## Release the Yeti!

Yeti is a platform meant to organize observables, indicators of compromise, TTPs, and knowledge on threats in a single, unified repository. Yeti will also automatically enrich observables (e.g. resolve domains, geolocate IPs) so that you don't have to. Yeti provides an interface for humans (shiny Bootstrap-based UI) and one for machines (web API) so that your other tools can talk nicely to it.

{:.yeti-highlight}
Since it was raised in a very dynamic environment, Yeti is made to make Threat Intelligence management quick, efficient, and interoperable.

* GitHub Repo: [https://github.com/yeti-platform/yeti](https://github.com/yeti-platform/yeti){:target="_blank" class="external"}
* Installation instructions: [http://yeti-platform.readthedocs.io/en/latest/installation.html](http://yeti-platform.readthedocs.io/en/latest/installation.html)
* Getting started with Yeti: [http://yeti-platform.readthedocs.io/en/latest/getting-started.html](http://yeti-platform.readthedocs.io/en/latest/getting-started.html)
* Full documentation is on ReadTheDocs: [http://yeti-platform.readthedocs.io/en/latest/](http://yeti-platform.readthedocs.io/en/latest/){:target="_blank" class="external"}


## How Yeti came to be

Yeti was born out of frustration of having to answer the question "where have I seen this artifact before?" or Googling shady domains to tie them to a malware family.

In a nutshell, Yeti allows you to:

* Submit observables and get a pretty good guess on the nature of the threat.
* Inversely, focus on a threat and quickly list all TTPs, Observables, and
  associated malware.
* Let responders skip the "Google the artifact" stage of incident response.
* Let analysts focus on adding intelligence rather than worrying about
  machine-readable export formats.
* Visualize relationship graphs between different threats.

This is done by:

* Collecting and processing observables from a wide array of different sources
  (MISP instances, malware trackers, XML feeds, JSON feeds...)
* Providing a web API to automate queries (think incident management platform)
  and enrichment (think malware sandbox).
* Export the data in user-defined formats so that they can be ingested by
  third-party applications (think blocklists, SIEM).

## Under the hood

Yeti is mostly written in Python and JavaScript. Under the hood, it uses several other open-source projects:

* MongoDB: A document-oriented datastore
* Redis: A key-value storage (used by Celery for scheduling)
* Celery: A scheduler (uses Redis)
