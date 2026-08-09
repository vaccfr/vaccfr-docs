---
title: Les handovers et autres changements de contrôleur / position
description: Les handovers et autres changements de contrôleur / position
published: true
date: 2026-07-24T18:29:16.599Z
tags: 
editor: markdown
dateCreated: 2026-07-24T18:11:27.755Z
---

![doc_banner_atc_fr.png](/banners/doc_banner_atc_fr.png)
# Les handovers et autres changements de contrôleur / position

Un **H**and**O**ver ou **H**and**O**ff est le transfert de contrôle et de communication d’un trafic d’un contrôleur à un autre. Cette fiche vous apprendra comment les effectuer, et quelles précautions prendre pour que celui-ci se passe sans implication sur la sûreté des vols.

## Quand effectuer un Handover ?
### Sortie de secteur

Par définition, un secteur est une partie d’espace aérien découpé verticalement et horizontalement délégué à un contrôleur dans lequel il exerce différents services (cf.[Les espaces aériens et les services de la circulation aérienne](/fr/atc/documentation/airspace-and-services)). 


Lorsqu’un trafic sort de cet espace, il doit contacter le contrôleur responsable de l’espace suivant. Le trafic peut sortir de deux façons, expliquées ci-après.

#### Sortie latérale

Lorsque le trafic arrive aux délimitations horizontales du secteur, il est nécessaire de le transférer au secteur adjacent. En règle générale, le transfert doit s’effectuer **3 minutes** avant l’entrée dans le secteur suivant (~20Nm). Cependant, dans certains cas, une position définie par les deux ayant droits tient lieu de point de transfert, celles-ci sont explicitées dans les **LOAs** (**L**etter **O**f **A**greement) :

![loa_example.png](/doc-atc/loa_example.png){.align-center}

La capture ci-dessus est un extrait de la LOA France-Suisse à titre d'exemple.

Ainsi, sur la route **J32**, le transfert de contrôle doit se produire _au plus tard_ à **RONLA**, c’est le **COP** (**C**oordination **P**oint).

#### Sortie verticale

Lorsque le trafic arrive au plafond ou au plancher du secteur, là aussi il faut le transférer. En règle générale, le transfert doit s’effectuer environ **5000ft avant l’atteinte du niveau de sortie de secteur**. Encore une fois, des spécificités de transfert peuvent être coordonnées dans les **LOAs** :
![loa_example_2.png](/doc-atc/loa_example_2.png){.align-center}

On peut observer que pour la route **UN853** le point de coordination est **IRMAR** et que les trafics à destination de **LSGG** par exemple, doivent être descendus en dessous du **FL280**.

### Coordination

Certains transferts requièrent une coordination avec le contrôleur concerné avant de les effectuer.

Dans le cadre où un contrôleur ferme sa position et qu’un autre devient responsable de son espace par service Top-down, alors, le nouveau responsable du secteur doit être prévenu afin de ne pas être pris de court, de plus, les transferts doivent se faire un par un pour éviter la congestion de la nouvelle fréquence par un afflux important de pilotes.

## Comment effectuer un Handover ?
### Précautions à prendre

Avant d’effectuer un handover, il est nécessaire de prendre certaines précautions pour éviter un conflit si le pilote prend plus de temps que prévu à contacter le secteur suivant.

#### Absence de conflits

Il est impossible de transférer un trafic en **situation de conflit immédiat ou imminent**, le trafic nécessitant un minimum de temps pour effectuer le changement de fréquence, celui-ci ne sera pas joignable pendant un court instant, il est donc primordial qu’il ne soit pas conflictuel à court terme.

#### Pas de rattrapage

Lors de transfert de plusieurs trafics se suivant, il est important que ceux-ci ne se rattrapent pas pour les mêmes raisons que vu au-dessus. Pour cela, il peut être nécessaire d’**imposer des vitesses** (cf.[Les notions de vitesse et leur manipulation](/fr/atc/documentation/speed-and-use)).

#### Absence du cockpit

Comme le transfert doit se produire 3 minutes avant la sortie de secteur, il faut veiller à ce que les pilotes soient présents dans leur cockpit à ce moment. Il faut donc rester vigilant vis-à -vis des demandes d'absences proches des zones de transferts.

### Gestion de l'étiquette

Il existe deux façons d’effectuer un handover sur l’étiquette d’un trafic. La première consiste à faire un *TRANSFER* c'est-à-dire à demander au contrôleur suivant de gérer cette étiquette de par une notification, et le *RELEASE* qui consiste à libérer l’étiquette pour qu’elle soit éditable par tous les contrôleurs.

#### Transfer

Le **TRANSFER** est l’option privilégiée pour les positions radars (_APP,_CTR) puisqu’elle offre une meilleure visibilité et notifie le secteur suivant du transfert.

#### Release

Le **RELEASE** est principalement utilisé par les positions vigie, puisque cela permet aux autres contrôleurs de modifier le plan de vol des trafics et que la nécessité d’indications visuelles est moindre pour ces positions.

### Handover avec report d'informations

Lors du transfert, il peut être important d’informer le contrôleur suivant de certains paramètres du trafic, on utilise donc le report d’information par le biais du pilote qui devra les annoncer sur la fréquence suivante au premier contact.

#### Veiller la fréquence

> AFR123, veillez 118.700, au revoir.
> *AFR123, monitor 118.700, bye bye*.

Dans ce cas, le pilote doit changer de fréquence **sans s’annoncer sur la nouvelle**. Le contrôleur l'appellera de son propre gré. _Cette procédure doit être coordonnée avec le contrôleur suivant_.

#### Callsign only

> AFR123, contactez 121.150, indicatif d'appel uniquement, au revoir.
> *AFR123, contact 121.150, callsign only, bye bye*.

Dans ce cas, le pilote doit changer de fréquence et ne s’annoncer sur la nouvelle **qu’avec son indicatif d’appel**. Limitant la congestion de la fréquence. _Cette procédure doit être coordonnée avec le contrôleur suivant_.

#### Report de paramètres

> AFR123, indiquez **** sur 128.100, au revoir.
> *AFR123, report **** on 128.100, bye bye*.

Les différents paramètres pouvant être demandés sont les suivants :
- Vitesse
- Niveau autorisé (CFL)
- Niveau demandé (RFL)
- Cap
- Type d’appareil

Dans ce cas, le pilote doit changer de fréquence et s’annoncer sur la nouvelle **en indiquant le paramètre mentionné**. _Cette procédure est à l’initiative du contrôleur effectuant le transfert_.

