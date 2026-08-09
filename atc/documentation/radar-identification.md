---
title: L'identification radar et le fonctionnement du radar
description: L'identification radar et le fonctionnement du radar
published: true
date: 2026-07-24T18:03:38.299Z
tags: 
editor: markdown
dateCreated: 2026-07-24T17:46:43.866Z
---

![doc_banner_atc_fr.png](/banners/doc_banner_atc_fr.png)
# L'identification radar et le fonctionnement du radar
## L’identification radar

L’identification radar est une opération qui consiste à s’assurer que l’appareil appelant est bien celui que le contrôleur observe au radar. En d’autres termes, c’est une opération simple qui vise à obtenir une _corrélation_ entre l’image radar et la position réelle de l’avion.

**Cette procédure est nécessaire avant de débuter tout service radar avec le dit avion**.

Avant de comprendre comment cette opération est mise en place de manière concrète, regardons brièvement le fonctionnement d’un radar.

## La corrélation

Un radar ne sert qu'à afficher la position de l’avion. Il n’a pas connaissance des autres informations de l’avion (plan de vol etc..) La corrélation est l’acte de faire correspondre l’information retournée par des antennes radar (primaire et secondaire) avec les informations informatiques connues sur un appareil (plan de vol). En fonction du transpondeur de l’appareil on pourra mettre en relation le bon plan de vol au bon plot radar.

## Le radar d’un contrôleur : comment ça marche ?

Avant de parler d’un radar avion, prenons l’exemple d’un radar de contrôle de vitesse sur autoroute. D’un point de vue physique, une onde électromagnétique est envoyée du radar vers la voiture qui est ici la cible. L’onde est ensuite “réfléchie” et revient au radar. Le principe physique au cœur de ce processus est l'**effet Doppler**.

![radar_principle_schema.png](/doc-atc/radar_principle_schema.png){.align-center}

Le radar du contrôleur aérien est basé sur le même principe physique. Il convient juste de faire la différence entre 2 types de radar : le _radar primaire_ et le _radar secondaire_.

### Radar primaire (Primary Surveillance Radar)

C’est le radar qui est basé sur le principe que nous venons de voir. Il est facilement repérable avec son antenne de couleur rouge et son balayage rapide à 360°.

![radar_primaire.png](/doc-atc/radar_primaire.png){.align-center}

### Radar secondaire (Secondary Surveillance Radar)

L’origine du SSR remonte à la Seconde Guerre mondiale. Il a été développé par les Alliés selon le principe d’identification “ami ou ennemi” (**I**dentification **F**riend or **F**oe). Grandement amélioré depuis, le radar secondaire est aujourd’hui toujours utilisé. C’est d’ailleurs grâce à ce radar que sont nées les familles de transpondeur.

Le radar secondaire, lui, émet une demande d'interrogation. Lorsqu’elle est reçue par le transpondeur de l’appareil, celui-ci y répond en retournant différentes informations en fonction de son type de transpondeur. 

Si le transpondeur de l’appareil est éteint, il ne répondra pas à l'interrogation et le contrôleur ne le verra donc pas sur son écran radar. Les paramètres restants sont calculés par le radar par traitement électronique pour pouvoir ensuite être visualisés sur l’écran du contrôleur.

![radar_primaire.png](/doc-atc/radar_app_lfpg.png){.align-center}

Ci dessus la vue radar de LFPG_APP (Crédits : AirTeamImages).

> Pour plus d'informations sur le transpondeur, consultez la fiche dédiée : [le transpondeur](/fr/atc/documentation/transpondeur).
{.is-info}

## Méthodes d'identification

> L’identification radar est une procédure utilisée par les positions de contrôle “Approche” (APP) et “Centre” (CTR).  Dans la vie réelle, vous entendrez parfois des positions "Tour" (TWR) faire de l’identification : ce sont des cas bien particuliers. **Considérez que sur VATSIM, en France, seules les positions APP et CTR sont concernées par l’identification radar**.
{.is-warning}

Sur VATSIM, il existe deux méthodes d’identification radar, on distingue :
- L’identification au transpondeur
- L'utilisation du principe de report de position

### L’identification au transpondeur
#### A partir de l'étiquette de l'appareil

Lorsque le trafic émet sur votre fréquence au premier contact, vous avez plusieurs actions à réaliser :
- Assurez-vous que l’indicatif d’appel annoncé par le pilote correspond à celui sur l’étiquette.
- Vérifiez l’altitude ou le niveau de vol actuel de l’avion.
- Vérifiez qu’il n’y a pas d’alerte au niveau du transpondeur (DUPE ou autre code)
- Vérifiez le cap actuel ou le prochain point de route du trafic.

Si tous ces éléments sont cohérents, l’appareil est identifié.

**Exemple d’un trafic identifié correctement :**

![correctly_identified_acft.png](/doc-atc/correctly_identified_acft.png){.align-center}

Dans l'exemple ci-dessus, on identifie de "Ryanair 26", altitude 3000 pieds, cap 350° assigné.

Si l’un des 4 paramètres précédent n’est pas cohérent, vous devez en tant que contrôleur vous assurer que ce que vous montre le radar est bien le reflet de la réalité (voir partie suivante - **Utilisation du report de position**).

**Exemple d’un trafic non identifié:**

![incorrectly_identified_acft.png](/doc-atc/incorrectly_identified_acft.png){.align-center}

Dans l'exemple ci-dessus "Alpine 642" a besoin d'un nouveau code transpondeur.

#### En demandant au pilote d'afficher "IDENT"

S’il n’est pas possible d’identifier l'avion de manière certaine, vous pouvez demander au pilote d’utiliser la fonction “**IDENT**” du transpondeur. L’étiquette devrait alors clignoter et il vous sera plus facile d’identifier l’appareil.

### L’utilisation du report de position

Dans le cas où l’un des paramètres d’identification n’est pas cohérent, il peut être judicieux d’utiliser le report de position afin de s’assurer de la cohérence de l’image radar. Cette solution permet aussi indirectement de s’assurer que le pilote suit l'itinéraire demandé dans la configuration adéquate.

> **AFR1580 :** Nice Approche bonjour, AFR1580, niveau 250, route ABLAK.

Le pilote apparaît au niveau 275 sur le radar : le niveau de vol n’est pas cohérent. Le pilote n’a probablement pas le QNH sur “Standard” (STD).

> **LFMN_APP :** AFR1580, Nice Approche bonjour, confirmez niveau 250 au QNH standard 1013 hPa ?

Attendre quelques secondes avant que l’image radar devienne cohérente

> **LFMN_APP** : AFR1580, Nice Approche, identifié niveau 250