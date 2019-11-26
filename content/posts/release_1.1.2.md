---
date: 2019-11-21
description: "New CF-Release"
featured_image: "images/cf-puppeteer-1.1.2.jpg"
tags: ["release"]
title: "Version 1.1.2"
---

Release 1.1.2

With the release of cf-puppeteer 1.1.2 we worked on backporting some v3 features to the `legacy-push` option.
We also implemented the possibility to use all features with docker images.

All new features and bugfixes are listed below.

New Legacy-push options:

```bash
--route-only
--no-route
``` 

New v3 options:
```bash
--docker-image
--docker-username
``` 

---

## Feedback

Please give some feedback and open a issues if you find one. [github-issue tracker](https://github.com/HappyTobi/cf-puppeteer/issues)


## Changelog

### Changed 🛠

- refactor environment parsing
- cleanup code
- update documentation
- back port "--no-route" and "--route-only" option to "--legacy-push" (v2).
- enable docker support
- drop old `vendor-option` (replaced by `venerable-option`)
- printing the help option, was now sorted 

### Fixed 🐛  

- More stable environment variable parsing.
- Improve error handling while uploading artifact

---

Download:
[Github](https://github.com/HappyTobi/cf-puppeteer/releases/tag/1.1.2)


