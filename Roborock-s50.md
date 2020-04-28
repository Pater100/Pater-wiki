---
title: RoboRock S50 (Valetudo)
description: Beschrijving Flashen van Valetudo op RoboRock S50
published: true
date: 2020-04-28T11:16:08.812Z
tags: 
---

# RoboRock S55 (Rooten)
### Beschrijvig voor het Flashen van de RoboRock S50 met Valetudo en Rooten met Ubuntu.

## Intro
De juiste Software staat al geinstaleerd op de Raspberry pie 3 (Voorheen PaterScreen) benaderbaar [192.168.2.192](192.168.2.191)(Mapt IP)

Firmware is aanwezig op de RPI

## Building firmware
Ga naar [https://builder.dontvacuum.me](https://builder.dontvacuum.me)

Vul de volgende gegevens in:
* Voucher: Rockrobo
* E-mail: Mail adres
* ssh-public Key: Key van iMac te vinden in
* vink aan: Create diff between original and modified image
* vink aan: Replace Xiaomi adbd with generic adbd (enables shell access via USB)
* Vink aan: Preinstall valetudo 0.4.x (is not possible with valetudo 0.3 or RE)
* open tab: Rockrobo S50, S55, S5x, roborock.vacuum.s5
	* vink aan: Gen2 (ver 1886) recommended
  
Create Job, Dit kan een kwartier duren voordat de bestanden gestuurd worden.

## Verbind en verzend bestand
verbind de Raspberry met een scherm en een toetsenbord. doordat je met de stofzuiger zijn wifi verbinding moet maken is het niet mogelijk dit via SSH te doen.
Als je verbinding met de pi hebt gemaakt via SSH, 
Kun je het bestand wat is toegezonden van de vorige stap kopieren naar de homemap met de naam: v11_001886.pkg.

## bereid de stofzuiger voor.
Reset de Stofuigers internet verbinding door de return to charger en spotclean knop voor 5 seconden in gedrukt te houden.

## Root de Stofzuiger
Verbind de Raspberry met de SSID van de stofzuiger: Roborock-vacuum-s5_miap7024
Als de raspberry verbonden is, open je een terminal window.
We moeten nu op zoek naar de Token van stofzuiger. vul hiervoor het volgende comando in:
``` bash
mirobo --debug discover --handshake true
```

Nu wordt de stozuiger gevonden en wordt in de terminal het token weer gegevens. schrijf deze op, deze hebben we nu nodig voor het flashen.
zorg dat je in de map /home/pi/ bent.
``` bash
mirobo --ip 192.168.8.1 --token {verander voor zojuist verkregen token} update-firmware  v11_001886.pkg
```

Nu zal de stofzuiger de firmware downloaden van de raspberry en daarna instaleren dit kan 5 tot 10 minuten duren. de stofzuiger geeft aan als hij klaar is.

## Root testen
We kunnen de root testen door de iMac te verbinden met de SSID van de stofzuiger en dan proberen een SSH verbinding te maken met de stofzuiger die nu op ubuntu draait.
ssh `root@192.168.8.1` doordat we tijdens het maken van de firmware onze public key erin gedaan hebben heb je geen wachtwoord nodig.

## valetudo instaleren
zorg dat je verbonden met de SSID van de Stofzuiger en open het Programma RRCC (RoboRockControlCenter)

Deze zal aangeven een nieuwe niet geconfigureerde stofzuifer te hebben gevonden.
Vul de SSID gegevens in, klik vervolgens op ok. wacht tot de stofzuiger is verbonden met de WiFi. (het lampje op de stozuiger stopt met knipperen)

nu kun je in RRCC klikken op Ok. als deze een foutmelding geeft is dit niet erg.
Je kunt nog een keer proberen om via SSH in te loggen in de stofzuiger,

Laat RRCC zoeken de token. als je die niet kunt vinden kun je ook in de SSH sessie dit comando gebruiken: 
``` bash 
printf $(cat /mnt/data/miio/device.token) | xxd -p
```

in RRCC kun je klikken op Install Valetudo.
Als je hier op klikt zal de software op de stofzuiger in een docker container geinstaleerd worden.

Nu is de stofzuiger benaderbaar op het ip adres waarmee hij verbinding maakt.


