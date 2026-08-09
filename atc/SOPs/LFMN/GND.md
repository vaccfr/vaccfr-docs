---
title: Position Sol
description: SOP - LFMN
published: true
date: 2026-07-15T12:28:56.419Z
tags: 
editor: markdown
dateCreated: 2026-05-14T16:21:37.246Z
---

![doc_banner_sops.png](/banners/doc_banner_sops.png)
# Position Sol
## Terminaux

L'aéroport de Nice se compose de 2 terminaux :
- Le **Terminal 1** : il longe les taxiways S et T
- Le **Terminal 2** : il longe les taxiways C et T

Ainsi que 3 aires supplémentaires :
- Le **parking Kilo** : à l'est du terrain, pour l'aviation générale et affaires
- Le **terminal fret** : au Nord du Terminal 2

> Les **FATOs et stands pour hélicoptères** sont situés au sud du terrain, **en dehors de la zone de responsabilité** du contrôleur Sol.
{.is-info}

![apron-lfmn.png](/doc-atc/apron-lfmn.png =65%x){.align-center}

## Assignation des portes

Le plugin RampAgent contenu dans le pack contrôleur s'occupe de l'assignation des portes pour vous.

## Repoussages

> Certains postes disposent de sens de repoussage publiés. Dans le contexte de VATSIM, la bonne pratique est de **donner systématiquement le sens de repoussage** afin d’éviter toute surprise. **CoFrance vous aide** en vous indiquant la direction appropriée.
{.is-info}

Les stands entre T et U ne nécessitent pas de repoussage, cependant il est possible qu’il soit demandé par les pilotes sur le réseau. Il en est de même pour les stands se trouvant entre S, D et T  à l'exception des stands 7 et 9 (Face Nord) qui doivent repousser sur T et le stand 15 (Face Sud) qui doit repousser sur S.

Ci dessous sont décrits les principaux sens de repoussage publiés :
- C, repoussage face Sud (du stand 40B au stand 48)
- D, repoussage face Sud préférentiel. Face Nord possible en fonction de la situation au sol.
- S, stand 24 inclus à 10B, repoussage face à l'Est pour rouler via T ou D.
- T depuis le T1 ou le T2 repoussage face au points d’attente en service.
- Stand 40A et Cargo (28 et 26), repoussage face Ouest pour rouler sur C. Il est possible de coordonner avec l'équipage un repoussage face au Nord sur C pour rouler à droite sur S.

Pour les stands 62 à 50 au QFU 043, il est préférable de faire repousser face Ouest pour éviter la congestion de C.
![taxi-lfmn.png](/doc-atc/taxi-lfmn.png =65%x){.align-center}

## Roulage

> **Sur VATSIM**, il est conseillé d’utiliser **T pour les trafics au départ et U pour les arrivées**. Ceci est applicable dans les deux configurations de piste.
{.is-info}

Pour fluidifier les mouvements au sol à l’arrivée et éviter de bloquer la piste, il est possible de coordonner avec le contrôleur TWR un roulage initial en sortie de piste.

Aussi, pour donner plus de flexibilité au contrôleur TWR, il est de bonne pratique de proposer aux **trafics Light** un **départ depuis B3** (TORA 2157m) **en 04R**.

**Il n’y a pas de point de roulage intermédiaire à Nice**. il convient donc d’utiliser des clairances selon ce format :

> “Roulez et maintenez avant… / Taxi and hold short of…” 

Ce type de clairance permet de laisser les trafics au départ sortir du terminal avant de faire rouler les arrivées vers leur porte via C, S et D.

Pour les restrictions au roulage, référez-vous à l’AIP (GMC 01, 02, 03, 04 et 05).

## Points d'attente
### QFU 043 en service

La piste 04L dispose de 3 points d'attentes utilisables : A1, B1 et C1.

B1 est le point d'attente privilégié pour les trafics VFR au départ de la piste 04L.

A1 et C1 sont les points d'attente préférentiels.

> A charge élevée, seulement 2 trafics à l'attente sur C1 suffisent à bloquer les taxiways U, C et T, et donc, la plateforme.
{.is-warning}

> L'utilisation de plusieurs points d'attente en simultané n’est pas recommandée ceci afin de limiter les risques de conflits après la traversée de la piste intérieure.
{.is-info}

Lorsque le nombre de mouvements simultanés au sol est faible, C1 reste malgré tout une bonne option pour réduire le temps de roulage. Ce point d'attente est à utiliser si le trafic souhaite partir depuis l'intersection B3 de la piste 04R.

### QFU 223 en service

Les points d'attente H1 et G1 sont utilisés pour traverser la piste 22R.

Une traversée par G1 permet de garder plusieurs avions sur le taxiway Y et stabiliser le taux de départ dans les situations à forte charge.

## Cas particulier ILS 04L
![lfmn-hp-a1.png](/doc-atc/lfmn-hp-a1.png =25%x){.align-right}

Si la météo nécessite d'utiliser la procédure d'ILS en piste 04L, **plusieurs précautions sont nécessaires** :

- il est interdit de faire attendre un trafic sur A1 si un trafic est sur le point de capturer le glideslope
- il est demandé aux équipages de libérer la piste par F1 ou EG/G1

La première contrainte est due à la proximité entre le point d'attente A1 et l'antenne du glideslope (risque de perturbation du signal).

La seconde contrainte est due à un risque de perturbation du signal LOC.
