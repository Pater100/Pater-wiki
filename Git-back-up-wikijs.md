---
title: Git back-up Wiki.js
description: Back-up installen Wiki.js
published: true
date: 2020-04-29T12:34:50.777Z
tags: 
---

# Git back-up Wiki.js
Instellingen om Wiki.js te back-uppen naar Github

### SSH Key-pair
Open een Terminal window in Portainer, en crëeer een SSH key pair met onderstaande comand:

``` bash
$ ssh-keygen -t rsa -b 4096
```

Als er word gevraagd voor naam van de key, geef het volgende op:

``` bash
$ /wiki/git
```

Navigeer naar de map waar de key staat:

``` bash
$ cd /wiki
```

Open het bestand git.pub met een text editor:

``` bash
$ vi git.pub
```

Kopieer de waarde van `git.pub` ergens in een tekstbestand om later te gebruiken in Github

### Instellingen Github
Navigeer via de browser naar Github, en open de repository van de wiki.
![github_settings.jpg](/software/software/git-back-up-wiki/git-back-up-wiki/github_settings.jpg)