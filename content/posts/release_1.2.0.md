---
date: 2020-02-24
description: "New CF-Release"
featured_image: "images/cf-puppeteer-1.2.0.jpg"
tags: ["release"]
title: "Version 1.2.0"
---

Release 1.2.0

With the release of cf-puppeteer 1.2.0 we just fixed some bugs and bring some droped features back.

---

## Feedback

Please give some feedback and open a issues if you find one. [github-issue tracker](https://github.com/HappyTobi/cf-puppeteer/issues)


## Changelog

### Features 🚀
- `--vars-file` argument was available again, so it's possible to use manifest files with placeholderst

### Changed 🛠

- All routes will be switched lazy (after starting up the new application)  
- Dropped CF_PUPPETEER_TRACE and replace them with CF_TRACE (read the README "Known issues section" for using it)

### Fixed 🐛
- Error while passing environment variables on legacy push (--env)
- Typos, error messages  

---

Download:
[Github](https://github.com/HappyTobi/cf-puppeteer/releases/tag/1.2.0)