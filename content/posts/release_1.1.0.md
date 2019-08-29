---
date: 2019-06-29
description: "New CF-Release"
featured_image: "images/cf-puppeteer-1.1.0.jpg"
tags: ["release"]
title: "Version 1.1.0"
---

Release 1.1.0

With the release of cf-puppeteer version 1.1.0 we bring some new features and bugfixes.

The new features and bugfixes are listed below.

```bash
--no-route
--route-only
``` 

---

## Examples

### No-routes
Deploy the application without route switching - old application should still run and new one should be stoped after deployment

```bash
cf zero-downtime-push -f ./manifest.yml --no-route --vendor-option none
```

right now you can add new services or what ever you want.
To start the new application with routes and cleanup the old one you can do the following things:

```bash
cf zero-downtime-push -f ./manifest.yml --routes-only
```

---


## Feedback

Please give some feedback and open a issues if you find one. [github-issue tracker](https://github.com/HappyTobi/cf-puppeteer/issues)


## Changelog

### Changed 🛠
    
- vendor-option argument now supports the options: "stop,delete,none"
- env argument changed to POSIX style. (--env)

### Fixed 🐛

- upload file with v3 api temp file path generation was wrong
- delete application and rename vendor app when upload fails

### Features 🚀

- no-routes option added - ignore route switching, should be combined with vendor-option
- route-only add routes only - took routes from manifest and add them to the application (without vendor extension)
- no-start option for new deployed application

---

Download:
[Github](https://github.com/HappyTobi/cf-puppeteer/releases/tag/1.1.0)
