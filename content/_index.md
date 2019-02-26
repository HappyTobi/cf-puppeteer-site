---
title: "CF-Puppeteer: zero-downtime plugin"
featured_image: 'images/background.jpg'
description: "The Zero-downtime plugin for you cf cli."
---

Welcome to documentation of the CF-Puppeteer cf plugin.
The plugin was active maintained and fixed some issues from older versions of zero-downtime plugin.
So see all upcoming features or changes read the [Changelog](https://github.com/HappyTobi/cf-puppeteer/blob/master/CHANGELOG.md) on github.


# Installation

## CF-Community
```
$ cf install-plugin -r CF-Community "cf-puppeteer"
```

## Binary
```
$ cf install-plugin path/to/downloaded/binary
```


# Usage
```
$ cf zero-downtime-push [<App-Name>] -f <Manifest.yml> [options]
```

## Options
```
"-f":                "path to application manifest",
"-p":                "path to application files",
"-s":                "name of the stack to use",
"-t":                "push timeout (in secounds)",
"-show-app-log":     "tail and show application log during application start",
"-env":              "add environment key value pairs dynamic; can specity multiple times",
"-var":              "variable key value pair for variable substitution; can specify multiple times",
"-vars-file":        "Path to a variable substitution file for manifest; can specify multiple times",
```

### Example
```
$ cf zero-downtime-push -f manifest.yml -env DB_PORT=3306 -env DB_VENDOR=MYSQL -t 120 -show-app-log
```

# Version
You can find all released versions on Github

[Overview versions](https://github.com/HappyTobi/cf-puppeteer/releases)

Latest version: 0.0.12

# Changelog
All changes and features of the upcoming release are complete documented at the [Changelog](https://github.com/HappyTobi/cf-puppeteer/blob/master/CHANGELOG.md).

# About

## Source
The source code an be found on: [Github](https://github.com/HappyTobi/cf-puppeteer/)


## Issues
If there are any issue or bug pleas open an a [Issue on Github](https://github.com/HappyTobi/cf-puppeteer/issues)


## Like
If you like the plugin, don't forget to give it a ★ [star](https://github.com/HappyTobi/cf-puppeteer/) on github