---
title: Les principes de base en altimétrie
description: 
published: true
date: 2026-07-18T19:15:36.038Z
tags: 
editor: markdown
dateCreated: 2026-02-27T22:25:27.278Z
---

![doc_banner_atc_fr.png](/banners/doc_banner_atc_fr.png)
# Intoduction 
Dans le monde de l’aérien, on utilise habituellement un altimètre comme outil de mesure de l’altitude d’un aéronef. Cet instrument utilise, en général, deux paramètres lui permettant de déterminer l’altitude de l’avion : la pression atmosphérique extérieure ainsi qu’une valeur de référence. Cette valeur de référence est usuellement appelée : calage. Il s’agit de la valeur par rapport à laquelle l'altimètre indique l’altitude de l’aéronef. 


# Les différents calages altimétriques
Durant un vol, l’altimètre d’un avion peut être réglé selon trois <u> calages </u> différents :

| **Terme**              | **Explication**                                                                                                                       |
|:-----------------------:|:----------------------------------------------------------------------------------------------------------------------------------------:|
| **QFE**                | Un altimètre calé au QFE indique 0ft quand l’aéronef est au sol. Lorsqu'un aéronef est calé au QFE, on parle de hauteur par rapport au sol. |
| **QNH**                | Un altimètre calé au QNH indique l’altitude de l’aéroport quand l’aéronef est au sol. On parle alors d’altitude par rapport au niveau moyen de la mer. |
| **QNH STANDARD**       | Un altimètre calé au QNH STANDARD indique l’altitude par rapport au niveau de mer en atmosphère standard. On parle alors de niveau de vol. |
| **Valeur mesurée**     | Hauteur, Altitude, Niveau de vol.                                                                                                        |
| **Référence**          | Sol, Mer, Surface moyenne.                                                                                                               |

![calage.png](/calage.png)

# Les changements de calages altimétriques 

Lors du décollage d’un aérodrome, le pilote règle son altimètre au **QNH**. Il peut donc lire sur son altimètre l’altitude à laquelle il se trouve par rapport au niveau de la mer. Lorsque l’avion est au sol, cela correspond à l’altitude du terrain.

## Au cours de la montée :

On passe du **QNH** au **QNH STANDARD** (1013,25 hPa) lors du franchissement de l'altitude de transition (TA). En France, dans un espace contrôlé, celle-ci est généralement de 5000ft AMSL (Above Main Sea Level) sauf mention contraire. Hors espace contrôlé, elle est de 3000 ft ASFC (Above Surface).

La TA est constamment indiquée sur les cartes d’un aérodrome :
![carte_calage.png](/carte_calage.png)

## Au cours de la descente :

On passe du **QNH STANDARD** au **QNH** lors du franchissement du niveau de transition (TFL). Ce dernier est le premier niveau de vol utilisable, à 500 ft au-moins au-dessus de l’altitude de transition. En espace aérien contrôlé, le TL est calculé par le contrôleur. Le contrôleur d'approche à l’obligation de rappeler au trafic le QNH local lorsqu’il ordonne une descente en dessous du TFL. 

# Le calcul du niveau de transition

La méthode exacte de calcul du niveau de transition étant longue et complexe, elle ne peut être détaillée ici. Cependant, nous appliquerons ici une méthode plus simple et, à quelques exceptions près, valable dans la plupart des cas. 

| Condition           | Formula                |
|:-------------------:|:----------------------:|
| QNH < 1013 hPa      | TFL = TA + 2000 ft     |
| QNH ≥ 1013 hPa      | TFL = TA + 1000 ft     |
