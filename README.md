# Mattermail Docker image running on Alpine Linux

[![Docker Layers](https://img.shields.io/badge/docker%20layers-5-blue.svg?maxAge=2592000?style=flat-square)](https://hub.docker.com/r/yobasystems/alpine-mattermail/) [![Docker Size](https://img.shields.io/badge/docker%20size-17.1%20MB-blue.svg?maxAge=2592000?style=flat-square)](https://hub.docker.com/r/yobasystems/alpine-mattermail/) [![Docker Stars](https://img.shields.io/docker/stars/yobasystems/alpine-mattermail.svg?maxAge=2592000?style=flat-square)](https://hub.docker.com/r/yobasystems/alpine-mattermail/) [![Docker Pulls](https://img.shields.io/docker/pulls/yobasystems/alpine-mattermail.svg?maxAge=2592000?style=flat-square)](https://hub.docker.com/r/yobasystems/alpine-mattermail/)

[![Alpine Version](https://img.shields.io/badge/alpine%20version-v3.6.2-green.svg?maxAge=2592000?style=flat-square)](http://alpinelinux.org/) [![Mattermail Version](https://img.shields.io/badge/caddy%20version-v3.5.0-green.svg?maxAge=2592000?style=flat-square)](https://github.com/rodcorsi/mattermail)



This Docker image [(yobasystems/alpine-mattermail)](https://hub.docker.com/r/yobasystems/alpine-mattermail/) is based on the minimal [Alpine Linux](http://alpinelinux.org/)  using the [Mattermail](https://github.com/rodcorsi/mattermail) plugin for [Mattermost](https://about.mattermost.com/).

##### Alpine Version 3.6.2 (Released Jun 17, 2017)
##### Mattermail Version 3.5.0

----

## What is Alpine Linux?
Alpine Linux is a Linux distribution built around musl libc and BusyBox. The image is only 5 MB in size and has access to a package repository that is much more complete than other BusyBox based images. This makes Alpine Linux a great image base for utilities and even production applications. Read more about Alpine Linux here and you can see how their mantra fits in right at home with Docker images.

## What is Mattermail?
MatterMail is an integration service for Mattermost, MatterMail listen an email box and publish all received emails in a channel or private group in Mattermost.

## Features

  * Minimal size only ?? MB and only ? layers
  * Memory usage is minimal on a simple install
  * REQUIRES MATTERMOST SERVER

## Architectures

* ```:amd64```, ```:latest``` - 64 bit Intel/AMD (x86_64/amd64)
* ```:i386```, ```:x86``` - 32 bit Intel/AMD (x86/i686)
* ```:arm64v8```, ```:aarch64``` - 64 bit ARM (ARMv8/aarch64)
* ```:arm32v7```, ```:armhf``` - 32 bit ARM (ARMv7/armhf)

#### PLEASE CHECK TAGS BELOW FOR SUPPORTED ARCHITECTURES, THE ABOVE IS A LIST OF EXPLANATION

## Tags

* ```:latest```, ```:amd64``` latest branch based on amd64
* ```:master``` master branch usually inline with latest
* ```:v0.0.0``` version number related to docker version
* ```:armhf```, ```:arm32v7``` Armv7 based on latest tag but arm architecture


## Environment Variables:

### Main Mattermail parameters:
* `URL`: specify the url with http:// or https://
* `Name`: "Orders", name of the alert
* `Server`: "https://mattermost.acme.co.uk", URL of Mattermost Server
* `Team`: "ACME", Team name (must already be created in Mattermost)
* `Channel`: "#orders", Channel name (must already be created in Mattermost)
* `MattermostUser`: "mattermail@acme.co.uk", Mattermost Username (must already be created in Mattermost)
* `MattermostPass`: "password", Mattermost Password (must already be created in Mattermost)
* `ImapServer`: "imap.gmail.com:143", Email imap server address including port
* `Email`: "orders@acme.co.uk", Email login username
* `EmailPass`: "password", Email login password

## Creating an instance

```sh
$ docker run -d --name mattermail -v $(PWD)/files/mattermail.json:/config.json yobasystems/alpine-mattermail:latest
```

Make sure you fill in the correct email server info in the mattermail.json config file.


##### Note
Your mattermail.json can be edited inside a running container like so;

```sh
$ docker exec -it mattermail /bin/sh
$ vi /config.json
```


## Source Repository

* [Bitbucket - yobasystems/alpine-mattermail](https://bitbucket.org/yobasystems/alpine-mattermail/)

* [Github - yobasystems/alpine-mattermail](https://github.com/yobasystems/alpine-mattermail)

## Links

* [Yoba Systems](https://www.yobasystems.co.uk/)

* [Dockerhub - yobasystems](https://hub.docker.com/u/yobasystems/)

* [Quay.io - yobasystems](https://quay.io/organization/yobasystems)
