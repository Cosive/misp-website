---
title: MISP 2.4.123 released (aka the dashboard and security fix release)
date: 2020-03-10
layout: post
banner: /img/blog/dashboard.png
---

# MISP 2.4.123 released

A new version of MISP ([2.4.123](https://github.com/MISP/MISP/tree/v2.4.123)) has been released. This version includes various security related fixed, and a new Dashboard system.

# Security fixes

Thanks to a pentest conducted on behalf of the Centre for Cyber Security Belgium (CCB), we have received a list of ideas to improve our security posture along with 2 vulnerabilities:

- 2 XSS vulnerabilities (reported and fixed, more info via [CVE-2020-10246](/security) and [CVE-2020-10247](/security))
- various improvements for our password policy
- Improvements by adding preventative headers
- Providing the more information to the users by revealing potential foul play

We would hereby like to thank both the contracted part as well as CCB for sharing the results with us. We are always glad to receive pentest results, it's a great way for organisations to improve the security of MISP and we highly encourage everyone to MISP for potential issues and to [let us know](/security) - we will do our best to fix any identified issues as soon as possible.

# Dashboard system

As an outcome of the spread of COVID-19, we ourselves at the MISP-project team have spent a considerable amount of our free time over the past few weeks tracking the spread of and informing ourselves in regards to the outbreak.

As an outcome of quickly setting up a Coronavirus-sharing community via MISP for ourselves, in order to share and track information emerging about COVID-19, we have implemented a whole new Dashboarding functionality for MISP.

The new Dashboard is accessible directly in MISP and fully customisable by users.

- The system relies on bundled and custom widgets
- widgets work similarly to other modular parts of MISP, design your own, drop it in the MISP directory to get started
- For instructions on how to develop a basic widget visit [The training slide repository](/misp-training/a.a-widget-dev.pdf)
- Under the hood it uses the user settings system, allowing for custom configurations per user
- Dashboard templates can be saved and shared, both via MISP and via JSON configuration files
- Widgets come with a host of support functionalities (ACL, caching, auto-reloading, configuration systems)

We welcome contributions to our ever growing widget collection from our community, let us know if you want to get involved in the effort!

If you are interested in the covid-19 specific widgets, they are not included in the code-base directly, but are rather available via the new [widget-collection](https://github.com/MISP/widget-collection) library.

# Selecting your home page within MISP

Users an now replace their landing page from it redirecting to the event index to any other page in MISP. We recommend the consideration of switching to the dashboard as the first point of entry. Simply navigate to the page you wish to bookmark and click on the little star icon in the header bar.

# A bug affecting correlations and an interesting bug hunt

Due to a recently introduced bug, we had cases of correlations disappearing after an attribute edit under certain conditions (any edit not touching fields used to decide on whether to correlate an attribute). We have resolved the issue along with a full recorrelation being triggered on update, simply fetch the latest version of MISP and your instance should have the issue resolved once the job finishes.

# Acknowledgement

We would like to thank all the [contributors](/contributors), reporters and users who have helped us in the past months to improve MISP and information sharing at large. This release includes multiple updates in [misp-objects](/objects.html), [misp-taxonomies](/taxonomies.html) and [misp-galaxy](/galaxy.html).

As always, a detailed and [complete changelog is available](/Changelog.txt) with all the fixes, changes and improvements.


