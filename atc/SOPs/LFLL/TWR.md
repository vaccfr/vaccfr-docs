---
title: Saint-Exupéry Tour
description: 
published: true
date: 2026-07-15T10:38:27.178Z
tags: 
editor: markdown
dateCreated: 2026-06-14T14:19:49.346Z
---

![doc_banner_sops.png](/banners/doc_banner_sops.png)
# Position Tour
## Configuration préférentielle
Le QFU 35 est préférentiel pour cause de procédures instrumentales.

Pour garantir la meilleure capacité terrain, les pistes sont exploitées de la manière suivante : 
- piste extérieure (35R/17L) de manière préférentielle pour les atterrissages.
- piste intérieure (35L/17R) de manière préférentielle pour les décollages.

## Cadences départs/arrivées
La capacité maximale est de 48 mouvements par heure soit ~1m15s entre chaque mouvement, arrivée et départ confondu.
La plateforme étant un terrain A-CDM, la cadence maximale du CDM est de 34 départs par heure.

### Transfert au départ
Il n’existe pas de position départ à Lyon, la gestion des départs est séparée entre les deux INIs comme suit:

- Les départs vers l’Est (GEMLA, ASLEG, RISOR, BELUS) sont gérés par LFLL_E_APP
- Les départs vers l’Ouest (BELEP, MADOT, RESPI, PIMAK, MURRO,VEROT) sont gérés par LFLL_W_APP
- Les départs vers le nord (BUSIL, ALORA, MOKIP, MABES) sont gérés par : 
  - LFLL_E_APP en QFU 17
  - LFLL_W_APP en QFU 35
- Les départs vers le sud (ROMAM, LUKUM, MTL) sont gérés par : 
  - LFLL_W_APP en QFU 17
  - LFLL_E_APP en QFU 35 

## Gestion des mouvements simultanés
Il existe deux façons d'opérer le doublet, celles-ci dépendent des conditions météorologiques.

- En IMC, les pistes sont considérées <u>inter</u>dépendantes.
- En VMC[^1], les pistes sont considérées indépendantes sauf exceptions suivantes :
  - Remise de gaz causée par trop fort vent de travers (reprise 10min après la dernière occurrence)
  - Cisaillement de vent reporté (même condition de reprise)
  - RCC[^2] d'une piste ≤ 4 (reprise à RCC ≥ 5 sur les 2 pistes), ce point est donné à titre informatif mais n'est pas applicable sur VATSIM
  - Arrivée en procédure VOR/DME ou LOC

[^1]: Rappel des minimas VMC : visibilité ≥5000m & plafond ≥1500ft.
[^2]: RCC : Runway Condition Code.

## VFR
Le circuit de piste se fait à 1800ft à l’est de la plateforme peu importe le QFU utilisé.
Attention à la proximité entre les pistes et la branche de vent arrière.
Des itinéraires de départ et d'arrivée sont publiés, voir la carte VAC pour toutes les informations.

## LVP
La plateforme de St-Exupéry dispose de procédures **LVP** (Low Visiblity Procedures).
Elles doivent être en vigueur au plus tard quand : **RVR = 550m ou plafond = 200ft**.

Seules les pistes 35R et 35L sont dotées d’approche CAT II & III et homologuées pour les décollages par faible visibilité.
Restrictions d’utilisation : 
- dégagement RWY 35L par bretelles A3 ou A4,
- dégagement RWY 35R par bretelles B3, B4 ou V4; dégagement par V5 interdit.

## Remise de gaz
Les remises de gaz doivent être données comme publiées ou coordonnées avec l’approche.
