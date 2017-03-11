---
layout: post
cover: 'assets/images/cover2.jpg'
title: Introducing Yeti
date: 2017-03-10 08:00:00
tags: announcements
subclass: post
author: tomchop
---

# Release the Yeti!

After months of hard work, trial and error, and fighting with CSS alignment, we are happy to announce the release of Yeti: Your everyday Threat Intelligence platform. Although originally an independent project, Yeti would not have been able to exist without the team at CERT Société Générale, who put in countless hours debugging the tool and orienting development to best suit their needs.

**Since it was raised in a very dynamic environment, Yeti is made to make Threat Intelligence management quick, efficient, and interoperable.**

Yeti is a platform meant to organize observables, indicators of compromise, TTPs, and knowledge on threats in a single, unified repository. Yeti will also automatically enrich observables (e.g. resolve domains, geolocate IPs) so that you don't have to. Yeti provides an interface for humans (shiny Bootstrap-based UI) and one for machines (web API) so that your other tools can talk nicely to it.

GitHub Repo: https://github.com/yeti-platform/yeti
Documentation is on ReadTheDocs: http://yeti-platform.readthedocs.io/en/latest/

## Some extra information

Yeti was born out of frustration of having to answer the question "where have I seen this artifact before?" or Googling crimeware domains to tie them to a family.

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
