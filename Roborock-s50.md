---
title: RoboRock S50 (Valetudo)
description: Beschrijving Flashen van Valetudo op RoboRock S50
published: true
date: 2020-03-15T10:34:42.650Z
tags: 
---

# RoboRock S55 (Rooten)
### Beschrijvig voor het Flashen van de RoboRock S50 met Valetudo en Rooten met Ubuntu.

## Intro
De juiste Software staat al geinstaleerd op de Raspberry pie 3 (Voorheen PaterScreen) benaderbaar [192.168.2.83](192.168.2.83)

Firmware is aanwezig op de RPI

## Building firmware
Ga naar [https://builder.dontvacuum.me](https://builder.dontvacuum.me)

Vul de volgende gegevens in:
* Voucher: Rockrobo
* E-mail: Patrick@paternet.nl
* ssh-public Key: Key van iMac te vinden in
* vink aan: Create diff between original and modified image
* vink aan: Replace Xiaomi adbd with generic adbd (enables shell access via USB)
* Vink aan: Preinstall valetudo 0.4.x (is not possible with valetudo 0.3 or RE)
* open tab: Rockrobo S50, S55, S5x, roborock.vacuum.s5
	* vink aan: Gen2 (ver 1886) recommended
  
Create Job, Dit kan een kwartier duren voordat de bestanden gestuurd worden.