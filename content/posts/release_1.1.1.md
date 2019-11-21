---
date: 2019-06-30
description: "New CF-Release"
featured_image: "images/cf-puppeteer-1.1.1.jpg"
tags: ["release"]
title: "Version 1.1.1"
---

Release 1.1.1

With the release of cf-puppeteer with version 1.1.1 we worked on some feedback of the community and make the usability easier and more user friendly

All new features and bugfixes are listed below.

```bash
--no-route
--venerable-action
``` 

---

## Examples

### No-routes
Deploy the application without route switching - old application should still run and new one should be stoped after deployment.
(Venerable-action will be set to none automatically )

```bash
cf zero-downtime-push -f ./manifest.yml --no-routes 
```

now you can add new services or what ever you want.
To start the new application with routes and cleanup the old one you can do the following things:

```bash
cf zero-downtime-push -f ./manifest.yml --routes-only
```

---


## Feedback

Please give some feedback and open a issues if you find one. [github-issue tracker](https://github.com/HappyTobi/cf-puppeteer/issues)


## Changelog

### Changed 🛠
    
- vendor-option to venerable-action - deprecation message will be written if old argument was used
- no-route option set venerable-action to none as default

---

Download:
[Github](https://github.com/HappyTobi/cf-puppeteer/releases/tag/1.1.1)


