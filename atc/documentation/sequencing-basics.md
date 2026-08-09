---
title: Principes de séquencement
description: Principes de séquencement
published: true
date: 2026-07-19T18:54:44.084Z
tags: 
editor: markdown
dateCreated: 2026-07-18T19:53:50.510Z
---

![doc_banner_atc_fr.png](/banners/doc_banner_atc_fr.png)
# Principes de séquencement
## Introduction

Les arrivées peuvent venir des “quatres coins du monde”, cependant il faut pouvoir organiser ces flux pour leur permettre d'atterrir en toute sécurité et sur une même piste. 

On dit ainsi qu’il faut créer la _séquence d’approche_, c'est-à-dire parvenir à un **flux régulier d’arrivées à partir de différents flux d’arrivées**. Le séquencement est un travail d’équipe entre contrôleurs d’approche et en-route absolument nécessaire à la réussite de la gestion des arrivées.  

## Planifier son plan de séquence

Afin de produire une séquence la plus efficace possible, réfléchir et prévoir à l’avance la situation est absolument nécessaire. 

### Heure estimée au passage d’un point

Il est possible, sur EuroScope, d’afficher, pour un trafic, une estimation de l’heure d’arrivée sur un point. Pour cela, il suffit d’effectuer un clic gauche sur son altitude actuelle.

![eta_waypoint.png](/doc-atc/eta_waypoint.png){.align-center}

_**Exemple:**_ Grâce à cet outil, nous pouvons déterminer que **HES005** passera à la verticale de **RUBIT à 14:17z**, et avec cette information, nous pouvons donc décider s'il passera avant ou après un autre trafic.

### Positionnement des range rings

Les range rings sont un second outil permettant d’aider à définir les priorités. Comme leur nom l’indique, il s’agit de cercles de distances autour d’un centre donné.

> Ils s’activent à l'aide de la commande .rings [centre] [distance] [nombre]
{.is-info}

- **[centre]** : Tous les points définis dans le fichier secteur (Aéroport, Fix, VOR, NDB, …) ou des coordonnées si écrites dans le bon format.
- **[distance]** : Nombre arrondi au dixième près de la distance entre chaque cercle.
- **[nombre]** : Nombre entier précisant le nombre de cercles à faire apparaître

_**Exemple:**_ **.rings BISBO 8 5**  (5 cercles espacés de 8 Nm avec comme centre BISBO)

La présence de deux trafics sur le même cercle indique qu’il sont a la même distance du centre, il ne sont donc pas séparés, et une action doit être entreprise pour la créer.

### Catégorie des appareils

Afin d'éviter les surprises, il est important de vérifier les types d'appareils. En effet, les séparations minimales entre deux aéronefs varient en fonction du tonnage de ceux-ci.

De plus, la catégorie de l’appareil est un bon indicateur de la vitesse finale d’approche du trafic. Quand un **HEAVY** peut avoir une vitesse d’approche de 140 kts, un léger peut en avoir une inférieure à 100 kts. Ces différences de vitesse pouvant réduire une séparation très rapidement (**rappel : une différence de 60 kts équivaut à la perte d’1nm de séparation toutes les minutes**) il est donc nécessaire de prendre ces informations en considération.

### Vitesse des trafics

La vitesse instantanée des trafics joue un rôle primordial dans la planification de la séquence. En effet, bien qu’un trafic soit plus proche de l’approche, si il possède une vitesse nettement inférieure à un second trafic un peu plus éloigné _il peut être préférable de faire passer le trafic plus rapide en premier_.

![speed_sequence.png](/doc-atc/speed_sequence.png){.align-center}

> Dans ce type de situation, l’utilisation de vecteurs vitesse est primordiale afin d’aider à la visualisation.
{.is-info}

## Ajuster la séquence
### Méthodes de séquencement
#### Le guidage simple

Le guidage radar peut être utilisé pour diminuer ou augmenter la distance que le trafic doit parcourir. Avec un bonne maîtrise de celui-ci vous pouvez arriver à intercaler des trafics entre d’autres permettant de regrouper les flux. 

**_Exemple 1_ :**
![guidage_simple_1_1.png](/doc-atc/guidage_simple_1_1.png){.align-center}
![guidage_simple_1_1.png](/doc-atc/guidage_simple_1_2.png){.align-center}
**_Exemple 2_ :**
![guidage_simple_1_3.png](/doc-atc/guidage_simple_1_3.png){.align-center}
![guidage_simple_1_3.png](/doc-atc/guidage_simple_1_4.png){.align-center}

#### Le point merge

Une autre technique extrêmement fiable et efficace est le “**point merge**”. Cette technique prend tout son sens avec l’utilisation conjointe des range rings, lorsque les deux trafic sont séparés par un cercle alors, il peuvent être mis en direct sur le point de séquencement.

[point_merge_demo_fr.mp4](/doc-atc/point_merge_demo_fr.mp4)

### Gestion des vitesses

Enfin, la création et le maintien d’une séquence nécessite obligatoirement la gestion de la vitesse des trafics concernés. 

Pour rappel, l’unité de vitesse nœud est le rapport entre le nombre de nautique en fonction du temps. Il est donc possible de calculer le nombre de nautiques parcourues en fonction du temps et de la vitesse : **Kts = Nm / Heure**

- **250kts** → 250 Nm/H soit 4.2 Nm / Min
- **220kts** → 220 Nm/H soit 3.7 Nm / Min
- **180kts** → 180 Nm/H soit 3 Nm / Min

De plus, une différence de **30 kts** équivaut au gain/perte d’**1 Nm toutes les 2 minutes**, et une différence de **60 kts** à la perte/gain d’1 Nm toutes les minutes. 

> Pour plus d'informations, consultez la fiche sur [les notions de vitesse et leur manipulation](https://doc.vatsim.fr/fr/atc/documentation/speed-and-use).
{.is-info}



