---
date: 2019-06-18
description: "New CF-Release"
featured_image: "images/cf-puppeteer-1.0.0.jpg"
tags: ["release"]
title: "Version 1.0.0"
---

Release 1.0.0 - Final release is here

With the first final release we bring the version 1.0.0 to cf-puppeteer.
We bring some small features, many bug fixes and a complete refactoring of the old version of cf-puppeterr.

Right now it's possible to choose between an v2 or v3 cf push of your application.
CF-Puppeteer checks the cf-controller version and use the v3 push if it's possible.
To use the old push manually you can pass the option: ```--legacy-push```

The new version now supports the newest structure of [cf-manifests.yml](https://docs.cloudfoundry.org/devguide/deploy-apps/manifest-attributes.html) files 
with multiple buildpacks 
```
buildpacks:
 - java_* 
 - http_*
```

But we don't want to stop here, a new post will be written in the next days to show a small
roadmap of the plugin. We will bring some cool stuff in the next versions like
- docker support
- no-routes / -routes only deployment
...

Please give some feedback and open issues if you find some. [github-issue tracker](https://github.com/HappyTobi/cf-puppeteer/issues)

## Changelog

### Changed 🛠
    
- cleanup code (refactor the complete plugin)
- colorized logging - use default cf terminal logging with color
- remove some parameters (like var, vars-file etc.)  
- update ParseArgs to struct instead of multi return values
- code splitting / complete refactoring 

### Fixed 🐛

- publishing applications
- fix some linter errors
- implement new manifest parser to understand new manifest format (https://docs.cloudfoundry.org/devguide/deploy-apps/manifest-attributes.html#buildpack)

### Features 🚀

- add argument to stop old service only instead of deletion
- choose between v2 and v3 push (v2 = legacy option)
- new argument to show crash log before old application will be deleted
- show crash log if your new applications doesn't start

---

## Specials

### Tester 👩‍💻👨‍💻

Special thanks for testing on different environments and giving some good feedback
[Skyfalke](https://github.com/skyfalke)
[Seinol](https://github.com/seinol)


---

Download:
[Github](https://github.com/HappyTobi/cf-puppeteer/releases/tag/1.0.0)
