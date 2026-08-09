---
title: Les notions de vitesse et leur manipulation
description: Les notions de vitesse et leur manipulation
published: true
date: 2026-07-19T18:51:18.025Z
tags: 
editor: markdown
dateCreated: 2026-07-19T18:17:06.179Z
---

![doc_banner_atc_fr.png](/banners/doc_banner_atc_fr.png)
# Les notions de vitesse et leur manipulation
## Les différentes unités de vitesse
### La vitesse indiquée (IAS)

La vitesse indiquée (ou **I**ndicated **A**ir **S**peed) est **la vitesse affichée sur les instruments à bord de l’avion**. Cette valeur est obtenue par les sondes installées sur l’appareil. Les mesures effectuées par ces sondes sont retransmises aux instruments.

### La vitesse propre (TAS)

La vitesse propre (ou **T**rue **A**ir **S**peed) est la vitesse à laquelle l’appareil se déplace dans la masse d’air, peu importe sa densité. Cette dernière augmente naturellement au cours de la montée en raison d'une diminution de la résistance à l'air. En effet, plus on monte, plus la pression diminue ; ainsi, en fournissant la même poussée un aéronef aura une plus grande vitesse propre à haute altitude que dans les basses couches.  

Elle est souvent indiquée par les instruments des appareils disposant d’ordinateurs de bord. Néanmoins, on peut simplement en déterminer une **valeur approchée** de la façon suivante :
<br>
<center><b>TAS = IAS + (FL / 2)</b></center>

_**Exemple**_ : Un avion qui vole avec le vent dans le dos aura une GS > à sa TAS ; un avion qui vole face au vent aura une GS < à sa TAS ; un avion qui vole avec le vent en plein travers aura une GS = à sa TAS.

### La vitesse Mach

Le nombre de Mach est la vitesse propre d’un aéronef exprimée sous la forme d’un pourcentage de la vitesse du son. Celle-ci n’est utilisée qu’en contrôle en-route. A partir du niveau 260 (environ) elle peut être calculée grâce à la relation suivante :
<br>
<center><b>MACH = TAS / 600</b></center>

![abbaque_vitesse.png](/doc-atc/abbaque_vitesse.png){.align-center}

_**Exemple**_ : Un avion qui vole au FL360 avec une TAS de 450kts aura une une vitesse mach de 450/600 = 0,75. On dira qu’il vole au mach point  75.

## Les vitesses de référence en approche
### La vitesse minimale en lisse

La vitesse minimale en lisse (ou minimum clean speed) est la vitesse la plus basse à laquelle un appareil peut évoluer sans le déploiement d’équipements hypersustentateurs (volets, …). Elle permet ainsi d’indiquer des réductions de vitesse indiquée autour des 220 nœuds sans pour autant pénaliser l'équipage avec la sortie d'équipements introduisant de la traînée.

_**Exemple**_ : La vitesse minimale en lisse peut notamment être utilisée lorsqu’un trafic est placé dans un hippodrome d’attente.

### La vitesse minimale d'approche

La vitesse minimale d’approche (ou minimum approach speed) est la vitesse avec laquelle un aéronef vole en approche finale. Elle correspond généralement à 130% de la vitesse de décrochage de l’appareil : **(vAPP = 1,3 x vDÉCROCHAGE)**. Elle dépend donc du type d’appareil.

## Les vitesses de croisière
### Les vitesses de montée / descente

Comme vu précédemment, différentes unités de vitesse changent en fonction de l'altitude.
Afin de maintenir une vitesse constante, il est nécessaire d’effectuer une conversion de vitesse. 

L’altitude à laquelle cette conversion s’effectue s’appelle “**altitude de conjonction**” et dépend notamment des conditions météorologiques : elle se trouve généralement entre le FL260 et le FL290.

Sous ces niveaux, l’appareil maintiendra une vitesse indiquée alors qu’au-dessus, il maintiendra un nombre de Mach.

### La vitesse de croisière

En croisière, sans prendre en compte le vent, pour deux appareils maintenant le même nombre de Mach, celui se trouvant le plus bas sera le plus rapide à raison de ~2kts pour 1000ft.

_**Exemple**_ : à M.80, au FL260 -> 467kts ; au FL360 -> 447kts). Pour deux appareils qui maintiennent la même vitesse indiquée, celui qui se trouve le plus haut sera le plus rapide.

## La manipulation des différentes vitesses
### En contrôle d'approche
#### Restriction de vitesse

Les restrictions de vitesses permettent au contrôleur d’approche de maintenir ou de ralentir un appareil à une certaine vitesse afin d’atteindre divers objectifs (maintien de séparation, séquencement, …). Les vitesses principalement utilisées ici seront généralement comprises entre 280kts et 180 kts.


> La vitesse maximum pour l’interception d’une procédure d’approche est généralement de 220kts.
{.is-info}


> En contrôle d’approche, **l'utilisation des vitesses ne permet pas de créer de séparation entre deux aéronefs**. Pour cela, on privilégie davantage l’utilisation d’un guidage. Les vitesses n’ont que vocation à permettre le maintien d’une séparation déjà existante.
{.is-warning}


> On note que généralement, une réduction standard nécessite environ 1 nm pour perdre une dizaine de nœuds.
{.is-info}


Un aéronef peut difficilement perdre de l'altitude et de la vitesse en même temps, il est donc nécessaire de structurer votre guidage afin de ne pas avoir besoin qu’un avion réduise fortement alors qu’il doit aussi descendre. 

Par ailleurs, **une autorisation à l’approche supprime toutes restrictions préalables si celles-ci ne sont pas spécifiées dans la même clairance**

_**Exemple**_ : …maintenez 180kts jusqu'à 6 nautiques finale…

#### Régulation en approche finale

Afin d’éviter tout rattrapage et / ou perte de séparation en approche finale, des restrictions de vitesses associées à des distances peuvent être utilisées. Elles servent à ce qu’un avion réduise sa vitesse pour ne pas rattraper le précédent mais également à maintenir un trafic à une vitesse élevée pour éviter que le suivant ne le rattrape. 

> Les restrictions les plus communément utilisées sont 200kts jusqu’à 8nm, **180kts jusqu’à 6nm**, **160kts jusqu’à 4nm** et 140kts jusqu’à 2nm.
{.is-info}

### En contrôle en-route
#### Régulation en vitesse Mach

En contrôle en-route, afin de préserver une séparation ou pour réguler un flux, le contrôleur peut restreindre les aéronefs en utilisant des vitesses Mach. Dans certains cas, la restriction de vitesse permet ici également la création de séparation.

> Une différence d’un point de Mach correspond à une différence d’environ 6kts pour la vitesse propre de deux appareils au même niveau. De plus, on sait qu’une différence de 6kts correspond au gain ou la perte de 1 nm en 10 minutes.
{.is-info}

#### Conversion de vitesse en montée / descente

Comme indiqué précédemment dans le document, les trafics en évolution verticale subissent une conversion de vitesse, il est donc nécessaire d’adapter la restriction en fonction. Dans ce cas, le contrôleur peut indiquer une restriction en ajoutant, dans la clairance, le notion de “**conversion**” indiquant le maintien de la nouvelle restriction à partir de l’altitude de conjonction.
![perfo_avion.png](/doc-atc/perfo_avion.png){.align-center}