---
title: Les procédures LVP et l’utilisation des RVR
description: 
published: true
date: 2026-07-18T19:16:45.027Z
tags: 
editor: markdown
dateCreated: 2026-02-28T12:13:56.407Z
---

![doc_banner_atc_fr.png](/banners/doc_banner_atc_fr.png)
# Introduction
Aujourd’hui, le <u>brouillard</u> est l’un des phénomènes météorologiques les plus impactants pour l’aviation. Si le progrès technologique a permis au fil du temps de repousser toujours plus les limites, il n’est pas encore tout à fait possible de décoller et d’atterrir par tout temps, du moins, quelque soit la visibilité. 

Dans un objectif de sécurité accrue, il a fallu mettre en place des procédures qui régissent l’utilisation des infrastructures aéroportuaires par faible visibilité : ce sont les **L**ow **V**isibility **P**rocedures (LVP).

Cette fiche vous permettra de voir en quoi elles consistent, comment elles sont mises en place et quel est votre rôle en tant que contrôleur lorsque ces procédures de faible visibilité sont enclenchées. Nous verrons également les outils qui sont à votre disposition, notamment la “**portée visuelle de piste**”, ou **RVR** (Runway Visual Range).

![seuil_brouillard.png](/seuil_brouillard.png)


# Que sont les LVP ?


**LVP** est l’acronyme de Low Visibility Procedures. Ces procédures sont appliquées sur un aérodrome en vue d'assurer la sécurité des opérations lors des approches et des décollages par faible visibilité.

L’exploitation normale d’un aérodrome, avec des points d’attente relativement proches de la piste ou des départs et arrivées indépendants sur un doublet, peut engendrer des **perturbations du signal du localizer** de l’ILS. Cependant, en conditions météorologiques standard, à **200ft sol au plus tard**, l’équipage est en pilotage manuel avec les références visuelles nécessaires. Ces perturbations ne sont alors pas un problème de sécurité en soi. En revanche, lorsque les conditions se dégradent, **la conduite de l’approche et de l’atterrissage requiert davantage de précautions côté ATC**.

## Approches et décollages par faible visibilité

Si une approche **CAT I** ou **CAT II** s’effectue manuellement, l’approche **CAT III** est entièrement automatique jusqu’à l’atterrissage (compris). Dans ces conditions, il est critique de **garantir l’intégrité du signal, y compris pendant la phase de décélération.**

En effet, la présence d’obstacles dans les aires sensibles de l’ILS est susceptible de provoquer une déviation du localizer, suffisamment lente pour ne pas être détectée par les automatismes à bord, mais d’une amplitude de nature à provoquer une sortie de piste <a href="https://skybrary.aero/accidents-and-incidents/b773-munich-germany-2011" target="_blank">(comme par exemple à Munich en 2011 : B773, Munich Germany, 2011 | SKYbrary Aviation Safety)</a>. 

Il arrive que la visibilité soit telle que même les décollages nécessitent l’utilisation d’un localizer pour suivre l’axe de piste. Dans ces cas-là encore, il faut appliquer les procédures garantissant un signal ILS fiable.

## Mise en place des LVP

Lorsque la visibilité se dégrade, <u> on commence à utiliser la RVR </u>, ou Portée Visuelle de Piste en français. Il s’agit d’une visibilité instrumentale, mesurée à l’aide d’appareils dédiés (transmissomètres ou diffusomètres) placés le long de chaque piste, à chaque tiers de sa longueur. En effet, la valeur pouvant varier de façon significative d’un endroit à un autre du terrain, il est important d’avoir une <u> valeur précise le long de chaque piste </u>.

Dans le cas général, une approche CAT I ne peut s’effectuer si la RVR au toucher est inférieure à **600m**. Par conséquent, les LVP sont mises en place, au plus tard, dès que les RVR sont inférieures ou égales à cette valeur.

Nb : Sur VATSIM, les valeurs utilisées pour la portée visuelle de piste (RVR) sont celles présentes directement dans le metar du terrain en question. 


## Procédures et phraséologie associée

Dès lors que les procédures faible visibilité sont mises en place, les mesures prises par l’ATC sont notamment :

- <u> Maintien des aéronefs </u> aux **points d’attente CAT III**, c’est-à-dire à au moins 150 m de l’axe de piste.

- Utilisation de barres d’arrêt commandables (pour les bretelles d’alignement et de traversée) et permanentes (pour les bretelles non utilisables à l’alignement, bretelles intermédiaires le plus souvent).

- <u> Surveillance accrue des aires sensibles du localizer </u> (150m de part et d’autre de l’axe de piste). Elles doivent être dégagées au plus tard lorsque l’aéronef à l’arrivée passe 2 nm en finale. Dans ce même laps de temps, s’il s’agit d’un doublet de pistes, aucun aéronef ne peut survoler le travers des antennes du localizer de la piste d’arrivée.

- <u> Mise en place de cadences adaptées </u>, prenant notamment en compte un **dégagement de piste plus lent et plus long** (à titre d’information, 150s sur un doublet et de 210 à 240s sur une piste banalisée à CDG).

- <u> Pas de clairance anticipée d’atterrissage, ni de multi-alignement </u>.

- Communication des RVR dès leur apparition.

- Arrêt de l’utilisation des doubles axes en vigie trafic à CDG.

Au simulateur, les performances de l’ILS ne sont jamais dégradées, le verrou à 2 nm finale n’est donc pas pertinent en soi. Nous garderons néanmoins les précautions suivantes :

- Piste entièrement dégagée (jusqu’aux 150m) **lorsque l’aéronef suivant arrive en courte finale** [à définir] ou <u> avant la clairance de décollage du suivant</u>.

- Sur piste banalisée comme sur un doublet, <u> clairance de décollage au plus tard quand l’avion à l’arrivée passe 4 nm finale </u> (ce qui suppose que l’alignement ait été donné plus tôt). Ainsi, en cas d’approche interrompue, cela évite d’avoir 2 aéronefs évoluant sans séparation radar et sans références visuelles. 


<u> La phraséologie est légèrement modifiée </u>:

- Au premier contact avec l’approche, <u> donner les RVR de la piste vers laquelle est guidée le vol.</u>

- Au premier contact avec la tour,**le message type est “poursuivez l’approche piste XX, vent YYY@YY kts, RVR ZZ1, ZZ2, ZZ3”** (sauf si l’aéronef est n°1 sans décollage devant, auquel cas on peut bien sûr donner la clairance d’atterrissage directement, toujours avec les RVR).

- Au sol et à la tour (dans le cas de traversée de piste), ajouter la mention “CAT III” au nom du point d’attente.

- A l’ATIS, passer le message “LVP in operation”.


Nb : Enfin, au-delà des pistes, n’oublions pas que les aéronefs rouleront plus lentement et ne verront les autres aéronefs ou les intersections de taxiways que très tardivement. Plutôt qu’une priorité par rapport à un autre aéronef, mieux vaut parfois une instruction avec un arrêt à un endroit facilement identifiable.
