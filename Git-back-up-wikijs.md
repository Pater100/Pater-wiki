---
title: Git back-up Wiki.js
description: Back-up installen Wiki.js
published: true
date: 2020-04-29T13:12:41.210Z
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
Klik dan op settings.

![github_settings.jpg](/software/git-back-up-wiki/github_settings.jpg){.align-center}

Vervolgens klik je in het side-menu op Deploy keys.

![deploy_keys.jpg](/software/git-back-up-wiki/deploy_keys.jpg){.align-center}

Klik nu rechts van het venster op add deploy keys.
Nu zie je een venster met een tekst lijn en een tekst veld.

![add_deploy_key.jpg](/software/git-back-up-wiki/add_deploy_key.jpg){.align-center}

Vul bij de Title een naam in de van de key, zoals wiki

In het tekst veld kopieer je de inhoud van git,pub.

Zorg dat je Allow write acces aan hebt staan.
klik vervolgens op Add Key.

### Instellingen Wiki.js
