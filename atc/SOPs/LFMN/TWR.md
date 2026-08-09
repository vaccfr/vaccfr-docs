---
title: Position Tour
description: SOP - LFMN
published: true
date: 2026-07-15T12:30:08.945Z
tags: 
editor: markdown
dateCreated: 2026-05-14T20:31:54.391Z
---

![doc_banner_sops.png](/banners/doc_banner_sops.png)
# Position Tour

La CTR de Nice est un espace aérien de **classe D** s'étendant de la **surface jusqu'à 3500 pieds**. Elle est voisine de la CTR de Mandelieu située à l'Ouest. Les autres espaces en bordure de la CTR de Nice sont gérés par Nice Approche.

## Pistes
### Informations générales

> La piste **04L/22R** est utilisée pour les **atterrissages**.
{.is-info}

La piste 04L/22R peut être utilisée pour les départs VFR ou avions légers.

> La piste **04R/22L** est utilisée pour les **décollages**.
{.is-info}

En effet, la piste la plus à l'extérieur est utilisée pour les départs, contrairement à la pratique courante. C'est ce qui fait l'une des particularités de Nice et cela est dû aux nuisances sonores.


Ces deux **pistes** forment un doublet rapproché spécialisé et sont donc **interdépendantes**. C'est-à-dire qu'**il n'est pas possible de faire décoller ou atterrir deux avions en même temps**.

### Limites

Le **QFU 043** est **préférentiel** compte tenu des minimas d'approche, de la météorologie et de la topographie du terrain.

> Le QFU 043 est utilisé jusqu'à une composante de vent arrière de 6 noeuds (inclus).
{.is-info}

### Cadence

En fonctionnement normal (pistes utilisées tel que décrit plus haut), la cadence est de 38 à 45 mouvements par heure.

Lors d’opérations en piste unique, la cadence est réduite entre 30 et 37 mouvements par heure.

## Dégagement et traversée de piste

De part sa conception et la spécialisation du doublet, seuls les trafics au départ doivent traverser la piste intérieure. **Les clairances de traversée sont sous la responsabilité du contrôleur Tour**, y compris les opérations de roulage entre les deux pistes.

> **Il n’est pas possible de donner des clairances conditionnelles de traversée**. Une clairance de traversée peut-être donnée dès que le trafic occupant la piste passe ou a passé le point d’attente à partir duquel se fera la traversée.
{.is-danger}

### Attribution des points d'attente

- Les trafics Medium roulent au point d'attente Q3
- Les trafics Heavy roulent au point d'attente W3

> Par défaut, le contrôleur Sol proposera un départ depuis B3 pour les trafics Light (business jets notamment). La TORA est de 2157m. Pensez à coordonner un départ au point d'attente Q3 si la charge devient incompatible à l'utilisation de B3.
{.is-warning}

> **L'intersection A3 n'est pas utilisable** et est fermée à cause de la proximité immédiate après la traversée de la piste 04L.
{.is-danger}

### Trafics à l'arrivée

Lors du dégagement, et pour éviter de bloquer la piste ou les points d’attente en raison de la proximité du taxiway U, il est possible de coordonner avec le contrôleur GND un roulage initial après la traversée.

Voici un exemple pour un trafic à l'arrivée en 04L :

> **AFR22RJ, roulez à gauche sur U, contactez le sol 121.705, au revoir.**

En QFU 043, la piste intérieure ne dispose que d'une seule voie de dégagement rapide : il s'agit de EG.

## Remise de gaz

Sur VATSIM, à Nice, dans le cadre d'une remise de gaz sont systématiquement donnés :
- un cap
- une altitude

> Ces deux paramètres sont à coordonner au préalable avec le contrôleur Approche si présent (LFMN_F_APP ou LFMN_APP si le premier est absent).
{.is-warning}

> Dans le cas de Nice et pour éviter toute confusion, **la mention "remettez les gaz comme publié" est à proscrire**.
{.is-danger}

L'API[^1] qui doit être suivie n'est pas la même si le trafic suit toujours une approche instrumentale ou si il est engagé sur une VPT.

> Informez le contrôleur approche de la remise de gaz et mettez à jour le tag en conséquence dans la mesure du possible.
{.is-info}


[^1]: API : Approche interrompue

## Gestion des appareils VFR

![vac-lfmn.png](/doc-atc/vac-lfmn.png =65%x){.align-center}

### Circuit de piste

Le circuit de piste est à 1000 pieds au sud des installations peu importe la configuration de piste utilisée.

> En raison de la proximité du circuit de piste avec les trajectoires IFR de départ et d’arrivée, **il est conseillé de ne pas accepter de trafic en tour de piste lorsque la charge d'arrivée est élevée**. Dans ce cas, il vaut mieux proposer aux départs de Nice un vol local ou une navigation.
{.is-info}

### Circulation aérienne générale

La CTR de Nice comporte 4 points d’entrée (EW, NA, SB et EC) et 2 transit VFR nommés. Ceux-ci se trouvent au Nord (N1) et Nord-Ouest (W1) des installations et font respectivement route depuis NA et WE vers WN (1500ft minimum).

Les intégrations du Nord (via WN) se font sur clairance à 1500ft à la verticale des installations pour rejoindre le circuit de piste au Sud des installations à 1000ft.

Les arrivées du Sud et du Nord-Est ainsi que les transit côtier se font entre 500ft et 1000ft maximum afin de passer sous les arrivées IFR avant de rejoindre le circuit de piste.

Pour tous les trafics VFR la vitesse est limitée à 160 kts dans l’intégralité de la CTR. Toute évolution à une vitesse supérieure devra faire l’objet d’une demande de clairance spécifique.

> Le VFR spécial n’est pas autorisé.
{.is-danger}

### Hélicoptères

Pour les trafics à voilure tournante, l’altitude de transit est limitée à 500ft. Il faut les clairer sur des points d’arrivée (HS ou HE) pour les différentes FATOs. 

Les FATOs s’utilisent dans le même sens que les pistes (ex. 04L/R = MS pour l'atterrissage et ME pour le décollage).

Pour les hélicoptères au départ ou à l'arrivée de Monaco, il faut les clairer jusqu’à EC puis leur donner une info trafic si nécessaire car **la CTR de Monaco n’est pas couverte par la tour de Nice**.

![fato-lfmn.png](/doc-atc/fato-lfmn.png =65%x){.align-center}