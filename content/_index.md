---
title: "CF-Puppeteer: zero-downtime plugin"
featured_image: 'images/background.jpg'
description: "The Zero-downtime plugin for your cf cli."
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
The options you can use depends on v3 or legacy push

### V3 Push (without --legacy-push)
```bash
-f                              path to application manifest
-p                              path to application files
-s                              name of the stack to use
-t                              push timeout (in secounds)
--env                           add environment key value pairs dynamic; can specity multiple times
--venerable-action              option to delete or stop vendor application - default is delete,
--health-check-type             type of health check to perform,
--health-check-http-endpoint    endpoint for the 'http' health check type,
--invocation-timeout            timeout (in seconds) that controls individual health check invocations,
--process                       application process to update,
--show-crash-log                show recent logs when applications crashes while the deployment
--no-route                      deploy new application without adding routes
--route-only                    add routes from manifest to application only
--no-start                      don't start application after deployment
--docker-image                  docker image url                                                           (⭐️New since 1.1.2)
--docker-username               docker repository username; used with password from env CF_DOCKER_PASSWORD (⭐️New since 1.1.2)
--vars-file                     path to a variable substitution file for manifest                          (⭐️New since 1.2.0)
```

### Legacy-push (--legacy-push arg)
```bash
-f                              path to application manifest
-p                              path to application files
-s                              name of the stack to use
-t                              push timeout (in secounds)
--env                            add environment key value pairs dynamic; can specity multiple times
--legacy-push                   use legacy push instead of new v3 api
--show-crash-log                show recent logs when applications crashes while the deployment
--no-start                      don't start application after deployment
--no-route                      deploy new application without adding routes        (⭐️New since 1.1.2)
--route-only                    add routes from manifest to application only        (⭐️New since 1.1.2)
--vars-file                     path to a variable substitution file for manifest   (⭐️New since 1.2.0)
```

### Example

```
$ cf zero-downtime-push -f manifest.yml --env DB_PORT=3306 --env DB_VENDOR=MYSQL -t 120 --show-crash-log
```

### Legacy push Example

```
$ cf zero-downtime-push -f manifest.yml --legacy-push --env DB_PORT=3306 --env DB_VENDOR=MYSQL -t 120 --show-crash-log
```

## Tracing
To show more informations while running the plugin you have to set the environment variable CF_PUPPETEER_TRACE to true
```
export CF_PUPPETEER_TRACE=true
```
If you're using a UNIX System you can also combine it with CF_TRACE
```
CF_TRACE=/dev/stdout cf zero-downtime-push ...
```

--- 

# Version
You can find all released versions on Github

[Overview versions](https://github.com/HappyTobi/cf-puppeteer/releases)

Latest version: 1.2.1

--- 

# Changelog
All changes and features of the upcoming release are complete documented at the [Changelog](https://github.com/HappyTobi/cf-puppeteer/blob/master/CHANGELOG.md).

---

# About

## Source
The source code an be found on: [Github](https://github.com/HappyTobi/cf-puppeteer/)


## Issues
If there are any issue or bug pleas open an a [Issue on Github](https://github.com/HappyTobi/cf-puppeteer/issues)


## Like
If you like the plugin, don't forget to give it a ★ [star](https://github.com/HappyTobi/cf-puppeteer/) on github

## Contributors
Special thanks to all contributors
- [Skyfalke](https://github.com/skyfalke)
- [devorbitus](https://github.com/devorbitus)