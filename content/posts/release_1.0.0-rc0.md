---
date: 2019-05-05
description: "New CF-Release"
featured_image: "images/cf-puppeteer-1.0.0-rc0.jpg"
tags: ["release"]
title: "Version 1.0.0-rc.0"
---

Release 1.0.0-rc.0 - First release candiate

With the first rc we dont bring "new" features!, we just pushed the deployment on the newest level of cf api's.
The new version now supports the newest structure of [cf-manifests.yml](https://docs.cloudfoundry.org/devguide/deploy-apps/manifest-attributes.html) files.
The plugin is also a "complete" rewrite of the older versions.

For the new rc versions we will focus on bringing docker support, adding more tests and clean / simplify the plugin implementation.

Please give some feedback and open issues if you find some. [github-issue tracker](https://github.com/HappyTobi/cf-puppeteer/issues)

## Changelog

### Changed 🛠

- push application with v3 api
- update ParseArgs to struct instead of multi return values
- Start code splitting

### Fixed 🐛

- manifest parser to understand new format (https://docs.cloudfoundry.org/devguide/deploy-apps/manifest-attributes.html#buildpack)

### Features 🚀

- add argument to stop old service only instead of deletion

---

## Specials

### Contributors 👩‍💻👨‍💻

Special thanks to the first contributor to cf-puppeteer plugin
[devorbitus](https://github.com/devorbitus)

---

Download:
[Github](https://github.com/HappyTobi/cf-puppeteer/releases/tag/1.0.0.rc.0)
