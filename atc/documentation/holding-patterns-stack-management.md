---
title: Le principe des attentes et la gestion d'un stack
description: Le principe des attentes et la gestion d'un stack
published: true
date: 2026-07-24T17:20:59.697Z
tags: 
editor: markdown
dateCreated: 2026-07-24T16:51:57.862Z
---

![doc_banner_atc_fr.png](/banners/doc_banner_atc_fr.png)
# Le principe des attentes et la gestion d'un stack

Un circuit d’attente est une trajectoire en hippodrome autour d’un point géographique précis (VOR, NDB, FIX, … ) permettant le maintien d’un appareil dans une certaine zone de l’espace aérien. Cette procédure permet de faire attendre un appareil à un endroit précis.

![schema_hold_fr.png](/doc-atc/schema_hold_fr.png){.align-center}

Un circuit d’attente est donc composé de _deux virages à 180°_ reliés par _deux branches rectilignes_ (une de rapprochement et une d'éloignement). Il possède un sens (**Gauche** ou **Droite**) indiquant le sens du virage sur la section de rapprochement et le un temps de vol ou la distance à parcourir sur les sections rectilignes.

**Exemple :** 

![hold_example_fr.png](/doc-atc/hold_example_fr.png){.align-center}

## Quand les circuits d’attente sont-ils utilisés ?
### Forte affluence de trafic

Dans certaines situations, il advient qu’une très forte charge de trafic ne peut être gérée correctement sans retarder certains trafics. _Il est donc nécessaire de placer les aéronefs dans un hippodrome d’attente_ afin de faciliter la gestion des flux de trafic.

### Urgences, Pannes & Météo

Lorsqu’une urgence est déclarée sur un aéroport possédant une seule piste, aucun autre trafic ne doit se poser sur celle-ci avant l’appareil en détresse. Les autres avions en approche peuvent donc être amenés à attendre.

Aussi, en _présence d’un orage ou d’une météo difficile_ à proximité du terrain, il est possible que les trafics ne puissent temporairement pas s’y poser. Ceux-ci devront par conséquent attendre avant de pouvoir tenter un atterrissage.

### Perte d’altitude

Dans le cadre ou un pilote est bien au-dessus du plan de descente initial, _il est possible pour lui de poursuivre sa descente en toute sécurité dans un circuit d’attente_. Cette alternative permet la perte d’altitude sans avoir à guider l’appareil au radar afin de rallonger son approche.

### Séquencement

Dans certaines situations, notamment sur les terrains où le contrôle aérien n’est assuré que de manière “procédurale”, l’unique solution permettant de séquencer plusieurs trafics demeure l’utilisation de circuits d’attente. 

## Comment gérer un stack
### L'entrée dans l’attente
#### Attente publiée

Les circuits d’attente “publiés” sont ceux indiqués sur les cartes. _Leurs caractéristiques y sont donc spécifiées_. Le pilote doit donc suivre précisément les instructions indiquées par la carte lorsque le contrôleur lui demande d’attendre. En fonction de la charge de ce dernier, il peut aussi indiquer le **temps d’attente estimé ou l’heure d’approche prévue** au pilote.

#### Attente non-publiée

Le contrôleur aérien peut également demander à un trafic d’attendre sur un repère **où aucun circuit n’est publié**. La clairance d’attente doit alors être complétée par les informations qu’on trouverait habituellement sur une carte. Par exemple, la radiale de rapprochement, le sens du circuit, la distance ou le temps de vol sur la radiale d'éloignement. Cette clairance **demande automatiquement une plus grande vigilance sur l'impact et la surveillance des flux** puisque les trafics évoluent dans une zone protégée uniquement par surveillance radar. Ces attentes non-standards ajoutent ainsi une forte charge de travail au contrôleur mais sont _parfois nécessaires si les attentes publiées sont totalement surchargées_.

> Lorsque vous ordonnez des attentes, il est primordial de **faire réduire la vitesse des appareils que vous y placez**. En contrôle d’approche, il est préférable dans cette situation de demander au pilote une “minimum holding speed”, c’est-à-dire une _vitesse dont la valeur est presque équivalente à la vitesse minimale en lisse_.
{.is-info}

#### Les différentes procédures d'entrée

Il existe plusieurs procédures pour entrer dans un circuit d’attente en fonction de la manière dont on arrive sur le repère. Ces procédures sont faites pour que le trafic évolue dans la zone de protection du circuit d’attente tout en se repositionnant dans le bon sens.

##### Entrée directe

L'**entrée directe** est la plus commune. **Elle est utilisée lorsque le trafic arrive dans le même axe que la radiale de rapprochement**. Elle consiste simplement à suivre le premier virage de l’hippodrome.

![hold_direct_entry_fr.png](/doc-atc/hold_direct_entry_fr.png){.align-center}

##### Entrée parallèle

L'**entrée parallèle** est utilisée lorsque le trafic **arrive face au repère et du côté de l’attente**. Le trafic passe alors à la verticale du repère, vole en éloignement sur la course de l’axe de rapprochement avant de faire un demi tour pour retourner sur le repère et commencer l’attente.

![hold_parallel_entry_fr.png](/doc-atc/hold_parallel_entry_fr.png){.align-center}

##### Entrée décalée

L'**entrée décalée** est utilisée lorsque le trafic **arrive face au repère et du côté opposé de l’attente**. Il passe alors verticale du repère puis continue sur la course d'éloignement avant de suivre le virage de l’attente pour revenir sur le repère et débuter celle-ci.

![hold_offset_entry_fr.png](/doc-atc/hold_offset_entry_fr.png){.align-center}

### La descente dans l'attente

Les attentes se situent dans l’espace RVSM (ou en dessous du niveau 290 s’il ne s’agit pas d’attentes en-route), les trafics peuvent donc y évoluer avec **1000ft de séparation verticale au minimum**. Cependant il faut veiller au maintien de cette séparation lorsqu’ils sont en évolution verticale dans l’attente. Il est recommandé lorsque le temps en fréquence est limité de faire descendre un trafic seulement lorsque le niveau d’en dessous est libéré.

**Exemples :**

![holding_example1.png](/doc-atc/holding_example1.png){.align-center}

Dans l'exemple ci-dessus, le trafic au niveau 80 peut être autorisé à descendre au niveau 70 puisque le trafic situé en dessous se trouve au niveau 60. 

![holding_example2.png](/doc-atc/holding_example2.png){.align-center}

Dans l'exemple ci-dessus, le trafic au niveau 80 **ne peut pas** être autorisé à descendre au niveau 70 puisque le niveau 70 est toujours occupé par le trafic précédent.

![holding_example3.png](/doc-atc/holding_example3.png){.align-center}

Pour gagner du temps dans la descente des trafics il est également possible de leur assigner un taux de descente fixe permettant de maintenir la séparation verticale.

### La sortie de l'attente
#### Sortie immédiate
![hold_immediate_exit.png](/doc-atc/hold_immediate_exit.png){.align-center}

Cette clairance est donnée par l'intermédiaire d’un cap ou d’un direct et implique que le trafic **suive immédiatement les nouvelles instructions** peu importe sa position dans le circuit d’attente. 

#### Sortie anticipée

![hold_anticipated_exit.png](/doc-atc/hold_anticipated_exit.png){.align-center}

Contrairement à la sortie immédiate, cette clairance implique que le trafic finisse l’hippodrome dans lequel il se trouve et qu’il ne **quitte le circuit seulement au prochain passage sur le repère**. Passant le repère, le trafic suivra les instructions données par le contrôle, si l’attente se situe sur un IAF / IF avec une trajectoire publiée vers l’approche, alors cette clairance peut être agrémentée d'une autorisation d’approche.

#### Coordination entre contrôleurs

Dans le cas de la mise en service d’attentes en limite de secteur (ex : APP/F_APP), il est nécessaire de se coordonner sur la stratégie de livraison des trafics, pour assurer un flux fluide et sécurisé. 

Il existe **deux stratégies** :
- L’approche initiale (en charge du stack) fait sortir les trafics de l’attente avec un cap et    éventuellement une descente puis les shoot à l’ITM.
- Le trafic le plus bas du stack est shooté à l’ITM qui se chargera de la sortie de celui-ci.