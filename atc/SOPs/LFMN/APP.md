---
title: Position Approche
description: SOP - LFMN
published: true
date: 2026-07-15T12:31:10.725Z
tags: 
editor: markdown
dateCreated: 2026-05-15T16:05:53.613Z
---

![doc_banner_sops.png](/banners/doc_banner_sops.png)
# Position Approche
## Secteur

![lfmn-ats.png](/doc-atc/lfmn-ats.png =65%x){.align-center}

## Dégroupages

Lorsque la charge le nécessite, la TMA de Nice peut être dégroupée en 4 secteurs.
<br>

### Nice Approche (LFMN_APP)

Il s'agit du secteur principal (bandbox). La position couvre toute la TMA Nice ainsi que son SIV.

**En présence de l'ITM (LFMN_F_APP)**

Nice Approche (LFMN_APP) prend en charge les trafics arrivant par l'Ouest (*NISAR, XIRBI, PERUS, ABDIL, TUPOX, ABLAK et BIRGO*) jusqu'à l'IAF **MUS**.

> Dans ce cas, Nice Approche est responsable du circuit d'attente sur **MUS** si ouvert.
{.is-info}

Les transferts vers l'ITM se font en cap avant ou après MUS, en coordination avec le contrôleur présent.

> Lorsque l'attente est ouverte, la stratégie privilégiée consiste à faire descendre le trafic au FL80 et de le transférer à l'ITM qui lui fera quitter l'attente.
{.is-info}

**En l'absence de l'ITM (LFMN_F_APP)**

Nice Approche (LFMN_APP) est en charge des trafics jusqu'à l'IF.

**En l'absence de l'Approche Est (LFMN_E_APP)**

Nice Approche est alors responsable des arrivées Est comme décrit dans le paragraphe dédié à LFMN_E_APP.
<br>
### Nice Départ (LFMN_DEP)

Il s'agit du secteur en charge de l'ensemble des départs de la plateforme.

**Conditions d'ouverture**

1) Nice Approche (LFMN_APP) est connectée.
2) Nice Tour (LFMN_TWR) est connectée.

**En l'absence de Mandelieu Tour (LFMD_TWR)**

Nice Départ assure le service top-down sur LFMD.

**Particularités**

> Soyez vigilants à la **montée des départs BASIP en présence d'arrivées BORDI ou VEVAR**. Leur croisement s'effectue à 1000 pieds d'écarts à MIKRU.
{.is-warning}


Les contraintes de STAR permettent de limiter le risque de conflit évoqué ci-dessus en faisant monter les départs au FL100 et en faisant descendre les arrivées au FL110.
<br>

### Nice Approche, secteur Est (LFMN_E_APP)

Il s'agit du secteur en charge des arrivées depuis l'Est (VEVAR, BORDI, OZMIC, KERIT, SODRI et LONSU) jusqu'à l'IAF NERAS.

> Dans ce cas, Nice Approche (LFMN_E_APP) est responsable du circuit d'attente sur **NERAS** si ouvert.
{.is-info}

**Conditions d'ouverture**

1) Nice Approche (LFMN_APP) est connectée.

**Particularités**

> Soyez vigilants aux **clairances de descentes des trafics arrivant par VEVAR et BORDI** qui coupent la trajectoire des départs BASIP.
{.is-warning}

Le risque de conflit illustré ci-dessus peut être réduit en clairant les arrivées au FL110 (en accord avec leur MVA) pour assurer une séparation verticale de 1000 pieds au niveau de MIKRU.

Les transferts vers LFMN_APP ou LFMN_F_APP se font au capa avant ou après NERAS, en coordination avec le contrôleur présent.

> Lorsque l'attente est ouverte, la stratégie privilégiée consiste à faire descendre le trafic au dernier niveau et de le transférer à l'ITM qui lui fera quitter l'attente.
{.is-info}

### Nice Arrivée, ITM (LFMN_F_APP)

Il s'agit du secteur d'approche finale, en charge de la séquence vers l'IF pour l'approche en service. 

**Conditions d'ouverture**

1) Nice Approche (LFMN_APP) est connectée.
2) Nice Tour (LFMN_TWR) est connectée

**Particularités**

Le secteur gère les trafics entre **MUS** et **NERAS** ainsi que la sortie des attentes lorsqu'elles sont ouvertes.


### Nice Information, secteur d'info de vol (LFMN_I_APP)

Ce secteur couvre uniquement le SIV de Nice pour le service d'information de vol en dehors de la TMA.

## Altitudes minimales de guidage

Les altitudes ci-dessous sont à respecter scrupuleusement lorsque les trafics sont en guidage radar ou en directe vers un point.

![lfmn-amg.png](/doc-atc/lfmn-amg.png =65%x){.align-center}

Pour les approches initiales en CDO (Continuous Descent Operations), il convient de donner la clairance de descente vers l'altitude plateforme de l'approche une fois que le trafic sera dans la zone de la MVA correspondante. Le trafic sera en même temps clairé pour l'approche.

## Trajectoires de départ

Les trajectoires des départs Nord passent entre les arrivées de l’Est et de l’Ouest. Les départs Sud passent au centre de la zone de guidage radar.

Verticalement, les départs passent au-dessus des trafics en guidage radar. Les départs BASIP montent au FL100 et passent sous les arrivées VEVAR et BORDI. Les arrivées doivent passer MIKRU au FL110 ou plus. Il faudra donc faire attention aux clairances de montée des départs en présence d’arrivées du Nord-Est.

> Pour les niveaux initiaux, référez-vous à la section Départs du briefing pour la position Prévol.
{.is-info}

Les transferts vers Marseille Contrôle se font au FL140 pour tous les départs sauf les départs Nord qui doivent monter au FL170, les départs BASIP peuvent monter vers le niveau FL160 si non conflictuels (cf. COPX).

> Pour les trajectoires détaillées, référez-vous aux cartes SID_RWY22L-22R_RNAV et SID_RWY04L-04R_RNAV
{.is-info}

## Trajectoires d'arrivée

Les arrivées sont livrées par Marseille Contrôle au FL140 sur AMFOU, KESAK, BIRGO au FL180 sur GAPDO et FL170 sur BORDI.

> Pour les trajectoires détaillées, référez-vous aux cartes STAR_EAST_RWY_ALL_RNAV et STAR_WEST_RWY_ALL_RNAV
{.is-info}

Vous trouverez aussi sur la plateforme de Documentation un [diagramme de guidage radar](/fr/atc/SOPs/LFMN/diagrams) des avions à l'arrivée.

## Circuits d'attente

![lfmn-holds.png](/doc-atc/lfmn-holds.png =80%x){.align-center}

## Point Merge
**Config 04**
Lors du guidage radar vers l’IAF (BISBO ou LEMPU), il est pertinent d’utiliser la technique du point merge. 

> Le réglage optimal est d’utiliser des arcs de 7NM pour BISBO et LEMPU avec des vecteurs de vitesse réglé à 2 minutes.
{.is-success}


**Config 22**
Lors du guidage radar vers l’IAF (NANAX), il est pertinent d’utiliser la technique du point merge. 

> Le réglage optimal est d’utiliser des arcs de 8NM avec des vecteurs vitesse de 2 minutes.
{.is-success}

Ce nautique additionnel permet d’augmenter légèrement l’espacement entre les trafics à l'arrivée car il n’existe pas de voie de dégagement rapide au QFU 223.


### Remises de gaz (API)
Sur le réseau, une grande partie des remises de gaz auront lieu sur les VPTs et non sur les approches instrumentales. 

> L’API qui doit être suivie n’est pas la même si un trafic suit une approche instrumentale ou si il est engagé sur une VPT.
{.is-warning}


On retiendra donc que : 
- les APIs ILS 04L/R se terminent systématiquement par un guidage radar,
- les APIs RNP se terminent théoriquement à NERAS (sauf RNP Z (AR) 22L/R) mais que dans la pratique ce sera surement un guidage radar,
- les APIs VPT sont des guidages radar.

# Terrains sous la TMA
## LFMD : Cannes Mandelieu
**Départs**
A Cannes, seule la piste 17 est utilisée pour les départs IFR. 

Les départs montent à 2000ft vers DIMAD puis suivent un guidage radar.
Il reste possible d’utiliser la piste 35 pour des départs à vue.

**Arrivées**
Les arrivées Cannes sont similaires à celles de Nice et le transfert depuis LFMM est le même. Les trajectoires passent sous les arrivées de Nice et sont légèrement décalées afin de limiter les interférences. 

Les STARs se terminent à l'IAF des approches, il faut donc clairer les trafics à l'approche avant **NEKIP** ou **INLOV** s’ils ne suivent pas une directe vers un autre point.

**Approches**
Il existe 2 approches préférentielles à Cannes, la LOC A piste 17 suivie de la VPT A 17, et la RNP Y piste 35. 

Dans le cas de la VPT piste 17, il est possible de clairer un autre trafic sur la VPT seulement si celui-ci rejoint la vent arrière avant que le précédent tourne en finale. Idéalement un espacement suffisant en amont de l’approche LOC permet d'éviter ces situations.

**VFR**
Pour les points suivants, il est bon de se référer à la carte VAC.

Il faut retenir que le circuit de piste diffère (altitude et trajectoire) selon le type avion.
Il existe plusieurs itinéraires de départ et d’arrivée.

Les hélicoptères utilisent de préférence la piste 04/22 via HW et HE (MAX 600ft).

De plus, l’hélistation du Quai du Large (LFTL), se trouve dans la CTR de Cannes, il est donc couvert par la Tour ou LFMN_APP/LFMN_DEP en top-down.

## LFTZ : La Mole Saint-Tropez
Les trafics IFR à La Mole sont très rares mais existent sur le réseau.

**Départs**
A La Mole, seule la piste 06 est utilisée pour les départs IFR. Les départs montent à 4000ft vers **STP** puis **LERMA**, avant de recevoir un guidage radar. Il est possible de donner les clairances de départ mais les trafics devront rappeler passant 3500ft.

**Arrivée**
Les trajectoires d’arrivées sont les mêmes que LFMD et leur gestion est similaire.

**Approche**
Il n’existe qu’une seule approche instrumentale, la VOR A. Les trafics à l’arrivée doivent être clairés en descente jusqu’à 4000ft puis à l’approche. 

> Passant 3500ft, lesdits trafics sortent de l’espace D de la TMA et ne reçoivent par la suite que le service d’information en vol.
{.is-warning}


**VFR**
Service d’information en vol uniquement, et pour toute info supplémentaire, voir la carte VAC.

## LFTH : Toulon Hyères
Les arrivées LFTH en provenance du Nord traversent le secteur Est de la TMA, il faudra les clairer en descente vers le FL70.

> L’approche de Nice ne couvrant pas Toulon, il ne faut donc pas donner de clairance d’arrivée ou d’approche.
{.is-warning}


## SIV
Le SIV de Nice couvre les limites horizontales des TMAs de la surface jusqu’au plancher de la TMA.

Afin d’ajouter une couche de réalisme vous pouvez donner les codes transpondeurs suivant aux hélicoptères évoluant dans le SIV de Nice.

|Transpondeur|5470|5471|5472|5473|5474|5475|5476|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|Destination|Divers|LFTZ : La Mole & Presqu’île de St-Tropez|LFMD : AD Cannes Mandelieu|LFTL : HST Cannes Quai du Large|LFMN : AD Nice Côte d’Azur|LNCM : Héliport Monaco|Vols Panoramiques


