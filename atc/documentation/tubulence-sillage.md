---
title: Les séparations pour turbulences de sillage et l'optimisation des décollages
description: 
published: true
date: 2026-07-18T19:22:04.257Z
tags: 
editor: markdown
dateCreated: 2026-02-27T22:32:40.467Z
---

![doc_banner_atc_fr.png](/banners/doc_banner_atc_fr.png)
# Introduction
Le séquencement des départs est un point clé de la réussite lorsqu’il faut s’occuper d’un important flux de trafic. Les objectifs sont multiples et essentiels : <u> assurer la sécurité entre les trafics au départ</u>, ne <u>pas engorger les points d’attente</u> inutilement, <u>faciliter le travail des contrôleurs départs et en-route</u> pour faire monter les trafics, etc...

# Les séparations au décollage

## Règle générale

Suivant la règle ICAO, il doit y avoir au minimum 1000 pieds ou 5 Nm d’écart entre deux aéronefs. Pour y parvenir lors du décollage, nous aurons un délai minimum à respecter entre 2 avions de même performance, du même point d’attente et dépendant de leur vitesse de montée initiale : 



| Vitesse des 2 avions | Délai     |
|:--------------------:|:---------:|
| 100 kts ou moins     | 4 minutes |
| 101 à 139 kts        | 3 minutes |
| 140 kts ou plus      | 2 minutes |

Remarque: Dans le cas où un SOP ou un Manex donnerait d’autres règles, il faut suivre les règles du dit SOP ou Manex.

## Différence de performance

Si l’aéronef suiveur est beaucoup plus rapide que le premier, il faut appliquer un délai **minimum de 3 minutes**. Exemple : un A320 derrière un TBM9 …
Il n’y a pas de liste exhaustive de cas particuliers, seule votre expérience vous permettra d’estimer la pertinence d’une telle majoration et de la majoration à faire.


## Les séparations pour turbulences de sillage :

Afin d’éviter les <u> dangers liés aux turbulences de sillage </u> laissées derrière un appareil au décollage, un intervalle de temps minimum est requis entre deux départs
Selon l’ICAO, la MTOW (**M**aximum **T**ake-**O**ff **W**eight) permet de catégoriser les turbulences de sillage en 4 groupes : 

| Catégorie    | MTOW              |
|:-------------:|:-----------------:|
| Light (L)    | ≤ 7t              |
| Medium (M)   | 7t < M ≤ 136t     |
| Heavy (H)    | 136t < M ≤ 560t   |
| Super (J)    | 560t <            |

En effet, plus un avion est lourd, <u> plus il aura d’impact sur la masse d’air qu’il traverse</u>. Ainsi ce classement permet d’établir des intervalles de temps minimums de séparation au départ en fonction du type d’avion. 


| N°1/N°2   | S  | H  | M  | L  |
|:----:|----:|----:|----:|----:|
|S| | 2/2 | 3/4 | 3/4 | 
| H | | |2/3 | 2/3 | 
| M |  |  |  | 2/3 |
| L |  |  |  | 2/3 |
Chiffres exprimés en minutes
Format : délai depuis la même bretelle ou en amont / délai depuis une bretelle en aval
Appliquer la règle générale si la case est vide.
Remarque: Le respect de ces minimums est impératif sans instruction contraire.

## En présence d’un contrôleur au dessus de la tour :


Lorsqu’il y a présence d’un contrôleur sur une position au-dessus de la tour, il est possible de coordonner avec ce dernier pour raccourcir les délais entre deux départs.

Remarque: Lors d'événements, des mesures de régulations comme les MDI (Minimum Departure Interval) peuvent être appliquées. Elles stipulent le délai supplémentaire à ajouter pour les trafics suivant leur destination.

## Quelques exemples :


<u> Situation 1 </u> :
- Numéro 1 : A350 *(Heavy)* 
- Numéro 2 : A320 *(Medium)*
- Même bretelle
→ Règle générale indique 2 minutes et la règle des turbulences de sillage en indique 2 aussi   
	donc => **2 minutes**

<u> Situation 2 </u> :
- Numéro 1 : C414 **(Light)** 
- Numéro 2 : C414 **(Light)**
- Même bretelle
→ Règle générale de 3 minutes
	donc => **3 minutes**


<u> Situation 3 </u>:
- Numéro 1 : A388 **(Super)** 
- Numéro 2 : C25C *(Light)**
- Bretelles différentes (le 2 en aval du 1)
→ Règle générale indique 2 minutes mais la règle des turbulences de sillage en indique 4 
donc => **4 minutes**

## Les VFR

Pour faire décoller un VFR entre des trafics IFR, la seule règle à respecter sont les turbulences de sillage puisque ceux-ci disposent de trajectoire différentes des trafics IFR.
Lorsque le VFR effectue son premier virage hors des trajectoires IFR, l’avion suivant peut décoller.
![jaiplusdimspipourlesnoms.png](/jaiplusdimspipourlesnoms.png)

# L’optimisation des décollages

Optimiser la façon dont on fait partir les trafics est essentiel, cela permet : d’une part de fluidifier le trafic au sol en évitant d’encombrer les points d’attentes et d’autre part de faciliter le travail des contrôleurs radar.

Pour réaliser cette tâche, nous nous focaliserons sur deux informations : **la SID et le type d’avion.**

## Un seul point d’attente disponible pour les décollages
Dans ce cas là, il faut essayer de séparer les avions ayant un même départ avec un avion ayant un départ différent s'ils décident de tous partir simultanément. Ainsi, nous pouvons coordonner une réduction du délai de décollage avec le contrôleur au-dessus sur la règle générale ou en cas de performance différente.

![panachage_hp.png](/panachage_hp.png)

**Attention, même si l’approche autorise une réduction du délai entre les décollages, les séparations pour turbulence de sillage doivent être respectées !**

## Plusieurs points d’attentes sont disponibles pour les décollages


Dans ce cas là, nous pouvons ségréguer les avions sur les points d'attente en fonction de leur SID et ainsi pouvoir alterner les départs.
- En fonction de la catégorie de turbulence de sillage (à préférer lorsque les départs sont différents)
- En fonction du départ prévu (à préférer lorsqu'un gros flux de trafic va suivre la même trajectoire, typiquement en event type city-pairing). Dans ce cas, on positionne le flux principal sur un point d'attente afin de libérer les autres points d'attente et d'optimiser la cadence de départ.


Remarque: Le départ d’une bretelle en aval du précédent augmente les délais de séparation pour turbulences de sillage.

![panachage_2_hp.png](/panachage_2_hp.png)

Nb : Deux stratégies concernant l’assignation des point d’attentes existent : 
- Stratégie 1 : Le sol attribue les points d'attente aux trafics puis les transfère à la tour. 
- Stratégie 2 : Le sol transfère les trafics en amont à la tour. C'est celle-ci qui se charge d'assigner les points d'attente. 

# Spécificités et remarques

Certaines plateformes possèdent des règles spécifiques dues à leur configuration modifiant les conditions et délai de départ. (ex: LFKJ lorsque les pistes de départs et d’arrivées sont opposées). Il faut donc étudier les procédures de chaque aéroport.

De plus, certains aéroports possèdent des SID dédiées aux hélices permettant de négliger les différences de performance entre un avion à hélices et un avion à réaction.


![varek7b.png](/varek7b.png)  

Si une séparation ne peut être maintenue, prévenez le plus rapidement possible le contrôleur suivant pour qu’il puisse prendre des mesures pour maintenir la séparation. 
<u> Si vous appliquez les règles évoquées dans cette fiche, ce scénario devrait être exceptionnel.</u>
