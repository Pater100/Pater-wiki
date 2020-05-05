---
title: Werken met hoekvariabelen
description: Werken met hoekvariabelen
published: true
date: 2020-05-05T18:43:43.761Z
tags: 
---

# Werken met hoek variabelen
hieronder een uitwerking van de Hoekvariabelen

## Stof KhanAcadamy
https://youtu.be/garegCgMxxg

## Booglengte (hoekverdraaiing)
Booglengte is de lengte van de verplaatsing langs de circel boog. en vervangt de liniare positie X(totaal)

Booglengte wordt aangegeven met het teken:
$$
\theta {\text{ -->Theta}}
$$

Theta wordt altijd aangegeven in Radialen [rad]
Eigenlijk is Theta de verplaatste hoek in radialen gezien vanaf het begin punt θ~i~
$$
Δθ = θ_f - θ_i
$$
## Boog Snelheid
Boog snelheid is de snelheid waarin iets beweegd aan de buitenkant van de radius. Boogsnelheid word aangegeven in Omega.
$$
\omega {\text{ -->Omega}}
$$

Omega vervangt de linaiare Snelheid V in Radialen per seconden.
$$
{radialen \over Seconden} = {rad \over s}
$$

$$
\omega ={\Delta \theta \over \Delta T}
$$

## Boog Versnelling
Boog versnelling is de Versnelling waarin de Snelheid (v) Toeneemt. Boog Versnelling wordt aangegeven in Alpha
$$
\alpha {\text{ -->Alpha}}
$$
Alpha vervangt de liniare versnelling a in Radiale per Seconden per seconden
$$
{radialen / seconden \over seconden} = {rad/s \over s}
$$

$$
\alpha ={\Delta \omega \over \Delta T}
$$


## Omtrek
De omtrek van een Cirkel is:
$$
2*\pi*r
$$

### omtrek snelheid
Om de omtrek snelheid te berekenen van een rond object.
$$
v=\omega*r
$$
hierin is v de snelheid in m/s, Omega de Boog/baan snelheid in rad/s en r is de radius van het draaiend object in meters.

## Omwentelingen
Omwentelingen omrekenen naar radialen is vrij simpel door het aantal omwentelingen te vermenigdvuldigen met 2. dit omdat er in iedere cirkel 2 keer pi zit.
$$
Omwentelingen *2*\pi = \text{ radialen in [rad]}
$$

## Pi
Omdat de helft van 180, 90 is, ziet dat hetzelfde eruit
$$
{180 \over 2} = 90\degree 
$$
een kwart Cirkel zoals 90 graden is dan gelijk aan:
$$
90\degree={\pi \over 2} 
$$


Een halve cirkel is gelijk aan:
$$
180\degree=\pi
$$

Een hele cirkel is gelijk aan:

$$
1 omwenteling=360\degree=2\pi
$$

## RPM naar Radialen per seconden
Om van Revolutions per Minute, naar Radialen per seconden te gaan gebruik je de volgende Formule:
$$
rpm*2*\pi \over 60 seconds
$$
RPM staat voor de gegeven waarde revolutions per minute. omdat pi maar een halve Cirkel is staat moet dat dus vermenigdvuldigd worden met de aantal seconden in een minuut. 

### voorbeeld
Wiel draaid 1500 rpm
$$
\omega={1500*2*\pi \over 60}
$$
$$
\omega=157,09[rad/s]
$$

## Formules
Hieronder de te gebruiken formules:
### Hoekverdraaiing
$$
\theta(t)=\theta_0+\omega*t+{1\over2}*\alpha*t^2
$$

### Hoeksnelheid
$$
\omega(t)=\omega_0+\alpha*t
$$

### Hoekverdraaiing, -snelheid, -versnelling
$$
\omega^2=\omega^2_0+2*\alpha*\Delta \theta
$$
#### Voorbeeld
Hoe groot is de eenparige hoekversnelling van een platenspeler als deze vanuit stilstand in 1,50 omwentelingen zijn afspeelsnelheid van 33 rpm bereikt?

Om van omwentelingen naar radialen te gaan:
$$
1,5*2*\pi
$$

Om van RPM naar radialen/seconden te gaan:
$$
33*2*\pi \over 60
$$

Rekenmodel:
$$
\omega^2=\omega^2_0+2*\alpha*\Delta \theta
$$

Ingevulde Formule:
$$
({33*2*\pi \over 60})^2=0^2+2*(1,5*2*\pi)*\alpha
$$

$$
\alpha={({33*2*\pi \over 60})^2\over 2*(1,5*2*\pi}
$$

$$
\alpha=0,63 [rad/s^2]
$$