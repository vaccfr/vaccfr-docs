---
title: SOP - LFPO Approche
description: 
published: true
date: 2026-03-16T12:58:26.974Z
tags: 
editor: markdown
dateCreated: 2026-03-16T12:20:08.378Z
---

# Introduction
Ce manuel vous permet de vous familiariser avec les différentes positions radar de Paris Orly. En cas de doute, n’hésitez pas à vous rapprocher de l’équipe de formation.

## Disclaimer
Bien que notre objectif soit de fournir un service de contrôle au plus proche de la réalité, certaines pratiques du réel ne sont pas adaptées à l’environnement de simulation en réseau, même sur VATSIM. A ce titre, il est important de savoir s’adapter face : 
- au niveau des pilotes (qui peut varier du débutant au plus expérimenté)
- aux limites propres à chaque simulateur/aéronef (modèle de vol, procédures moindre bruit, etc)
- aux limites de nos outils : même s’il y en a peu, nos radars restent moins performants que nos collègues du réel.

> Rappel : Ce document est à l’usage des contrôleurs sur VATSIM et est donc exclusivement réservé à la simulation.
{.is-warning}

Il convient de vous assurer que vous disposez des connaissances nécessaires pour ouvrir cette plate-forme. Ce manuel est rédigé dans le but de vous apporter des compléments mais ne peut se substituer à l’AIP disponible via le site du <a href="https://www.sia.aviation-civile.gouv.fr" target="_blank">SIA</a>.

# Généralités
La TMA de Paris Orly a un plafond au FL145 et couvre LFPO et LFPN en top down et les approches des aéroports environnant tel que LFPV (militaire).

Voici les diagrammes qui montrent les trajectoires et les restrictions de niveau pour les arrivées et les départs, ainsi que des instructions pour les guidages radars et les vitesses usuelles.

Si les avions suivent les trajectoires et les niveaux publiées (SID, transition, STAR), les conflits et zones interdites seront majoritairement évités.

> Tous les diagrames sont disponibles [ici](/fr/atc/SOPs/LFPO).
{.is-info}

Ce document ne remplace pas l’AIP, il est conseillé de passer en revue l’AIP pour les informations complémentaires.

# Départ
C’est le départ qui s’assure de la séparation entre les avions à l’arrivée et les avions au départ.

Les départs Nord, transitant par le départ de LFPG, ne peuvent pas être raccourcis par une directe sans coordination avec LFPG.

Les avions à hélices sont à séparer verticalement ou avec une directe stratégique.

En cas de grosse charge de trafic sur un même flux, il faut limiter les vitesses sur ce flux (par exemple 280 kts au-dessus du FL100) pour éviter les rattrapages et mettre en difficulté l’ATC suivant.
Donner un cap de séparation entre 2 départs doit être le dernier recours.

Les trafics doivent être envoyés à Paris Contrôle (LFFF) avec la séparation enroute requise (8 Nm sur le même départ s’ils ne sont pas limités en altitude et avec 5 Nm ou 1000ft d’écart minimum avec les autres trafics).

## VPE
Les départs sont soumis à un Volume de Protection Environnemental qui définit une zone dans laquelle le vol doit être contenu pour des raisons de nuisances sonores. Les limites latérales des VPE sont dessinées sur Euroscope et visibles sur les cartes AIP, leur plafond est le FL60.
On peut donner un guidage raccourci à un trafic au départ soit en passant le FL60 en montée, soit après la sortie du VPE le long de la SID.

## Configuration Ouest
Les départs passent en dessous des arrivées Orly.
Les départs vers le Nord sont transférés au départ de LFPG au FL80 sauf coordination contraire.

## Configuration Est
Les départs vers le Nord sont transférés au départ de LFPG au FL130 sauf coordination contraire.

## Départ non-RNAV
Les aéronefs non-RNAV peuvent bénéficier d’un départ en montée dans l’axe avec le niveau initial correspondant à la direction de leur sortie de zone.
Il est recommandé d’effectuer le guidage radar à proximité des SID équivalentes.

## Départs à RFL bas vers le sud
Les départs à RFL bas (OLZOM, MONOT et DORDI) depuis LFPG et LFPB ne restent pas avec LFPG_APP sur l’entièreté de la procédure. En effet, le profil vertical oblige un passage dans les TMA d’Orly.

Voici la stratégie recommandée : LFPG_APP (ou DEP si présent) assure la montée jusqu’à 3000 pieds. Un raccourci vers OXCEL en montée au niveau 70 est possible en coordination avec LFPO_APP (ou DEP si présent). Une attention particulière est portée sur la performance de l’aéronef suiveur pour éviter tout rattrapage. En effet, les départs à RFL bas sont davantage appropriés pour les avions hélices ou peu performants.

LFPG_APP transfère le trafic à LFPO_APP travers Paris.

## Les directes
Une fois le travail de séquencement sur une même sortie réalisé, il est possible de raccourcir le trafic avec une directe vers les points appropriés (cf. Euroscope). 

Attention, donner une directe va déplacer les lieux de croisement avec les autres flux, bien s’assurer que les nouveaux croisements ne créent pas de conflit.

Les départs Nord transitant par les espaces de LFPG, une coordination est nécessaire en sa présence si un direct s’avère pertinent.

# Approche Initiale
Les avions arrivent pré-séquencés sur chaque IAF par LFFF à minimum 8 NM sans rattrapage.

La clairance d’approche initiale doit contenir le nom de la procédure à suivre (parfois appelée transition). Si le pilote annonce un ATIS expiré ou aucune information, le message initial lui annonce la lettre de l’ATIS en cours.

Exemple : “EZY12P bonjour, cleared ODILO 6W approach, vectors ILR runway 25 (, information A)”


L’approche #A est une approche dite CDO (Continuous Descent Approach). Il est donc convenable de l’utiliser par faible trafic.

Compte tenu de la complexité de l’espace et des trajectoires, une attention particulière sera portée sur le suivi de la trajectoire après l’IAF, notamment afin de détecter une éventuelle erreur de saisie de l’approche dans l’avionique.

## Configuration Ouest
### ODILO#W
Le passage par VASOL est **obligatoire** afin de ne pas générer de conflits avec les montées Orly.

Toutefois, si le trafic le permet, il peut être pertinent de coordonner un direct PO615 depuis ODILO. Assurez-vous que cela est possible en vous coordonnant avec les contrôleurs APP, DEP (et éventuellement CTR) si connectés. 

### MOLBA#W
Il peut être intéressant de donner une directe PO610 depuis OKRIX. Veillez toutefois que le trafic bénéficiant de ce raccourci reste bien sous les départs vers l’Est depuis Orly.

### VEBEK#W
Les arrivées depuis VEBEK sont gérées par l’approche de LFPG et sont livrées en descente au FL80 vers VALPO.
Lorsqu’il n’y a pas de séquencement à faire sur les approches de LFPO, il peut être pertinent de coordonner un cap avec LFPG_S_APP depuis CTL pour intercepter l’ILS par le Nord.
Pour plus d’information sur l'interception de l’ILS par le Nord, voir le point [Interception ILS](#incerception-ils).

## Configuration Est
### ODILO#E
Depuis ODILO, il est possible de donner un cap pour intercepter l’ILS sans suivre l’approche.

### MOLBA#E
Il peut être intéressant de donner une directe PO621 depuis OKRIX. Veillez toutefois que le trafic bénéficiant de ce raccourci reste bien au-dessus des départs DORDI et en dessous de tous les autres départs.

### VEBEK#E
Les arrivées depuis VEBEK sont gérées par l’approche de LFPG et sont livrées après ASVOK sur un track 180 en descente au FL70.
N’hésitez pas à coordonner un cap plus favorable après ASVOK avec LFPG_APP.

### VEBEK#Y
Utilisé uniquement en configuration Est Inverse (LFPG en configuration Ouest), les arrivées depuis VEBEK sont gérées par l’approche de LFPG.
Les trafics sont livrés en descente au FL80 vers VALPO.


# Approche Finale
Le séquencement entre toutes les transitions se fait lors du guidage radar. L’approche finale gère les trafics comme elle le souhaite dans sa zone de contrôle.

Sur l’approche finale, les avions seront espacés de 3 NM minimum. 
Il est possible de réduire cette distance à 2.5 NM en suivant les indications du point 22.3.7 de l’AIP. Attention, cependant : les limitations de VATSIM et de la simulation font que cette réduction n’est pas viable la majeure partie du temps.

## Interception ILS
En configuration Ouest, l’interception ILS se fait à 4000ft sur le chevron (13Nm) mais peut se faire à 3000ft sur le chevron en pointillé (10.5Nm) si nécessaire.
En configuration Est, l’interception ILS se fait à 4000ft.

L’interception ILS se fait toujours par le Sud à l’exception des arrivées depuis VEBEK#W lorsqu’il n’y a aucun séquencement à faire. La zone au Nord de l’ILS est trop étroite pour permettre du séquencement. La vitesse recommandée à l’interception de l’axe est de 220 kts.

Il est déconseillé de viser un angle trop faible (inférieur à 15°). A l’inverse, l’angle maximum d’interception (règle OACI) reste de 45°. Par ailleurs, il existe une règle exigeant qu’un équipage approchant un axe d’approche sous un angle de moins de 70° l’intercepte en l’absence d'instruction contraire : il s’agit d’une mesure de sécurité, et en aucun cas d’une méthode de travail de l’ATC.

## Remise de gaz
La remise des gaz en 06 se fait généralement dans l’axe de la piste et en montée vers 2000 pieds.
La remise des gaz en 24 tourne très vite vers le Sud et en montée vers 2000 pieds (cf. AIP).
L’avion sera en guidage radar afin d’effectuer une nouvelle approche.

## LVP
En LVP, les atterrissages sont espacés de 150 à 180 secondes.
Les pistes ne sont plus indépendantes.

# VFR 
Toutes les infos se trouvent sur les cartes VAC des aéroports dans la TMA de Paris Orly et dans les cartes VAC hélistations de Paris.
Les hélicoptères sont tenus au strict respect des itinéraires publiés.

# POGO
Toutes les informations (altitude, trajectoire …) sont sur les cartes AIP POGO de LFPO et LFPG.

## Vers LFPO
Le trafic sera transféré à la finale de LFPO. L’approche finale dirige l’avion en guidage radar vers l’ILS de la piste en service.

## Depuis LFPO
Le trafic se gère comme un départ standard et sera transféré à la finale de LFPG.

# Configuration inverse
La configuration inverse étant rare, nous ne détaillerons pas les informations ici. Cependant, respecter les trajectoires et les niveaux permettra d’éviter les mauvaises surprises.

Pour VEBEK, nous utiliserons l’approche Y en configuration Ouest Inverse à LFPO. Voir le point [VEBEK#Y](#vebek#y).

# LFPN & LFPV
Voici le diagramme des départs pour LFPN : 
[Diagramme des départs - Toussus-le-noble](https://docs.google.com/drawings/d/192eFROIemca_fBA8Sa6Eczv7NoLsNiRKYJPZB9pSe5E/view)
Voici les diagrammes d’approches pour LFPN : 
[Diagramme des approches - Tousus-le-noble - EL](https://docs.google.com/drawings/d/1NPr4_rDtkM98sNc_GEDljwdVwTExNfePGCDUWvCCR90/view)
[Diagramme des approches - Tousus-le-noble - WL](https://docs.google.com/drawings/d/1_dNvUrHTdTPV-DMdIgO6wLV5rQt5czikPrJU4DF8jVM/view)

Les départs omnidirectionnels sont transférés au départ de LFPG avec une trajectoire et une altitude coordonnées avec LFPG.

Les approches VEBEK (E, W & Y) sont gérées de la même manière que pour Orly.
Nous utiliserons les transitions F et X pour les avions RNAV et les transitions C et D pour les non-RNAV.

De manière générale, ces arrivées passeront sous les arrivées LFPO.
Attention, en configuration Ouest, les arrivées LFPN/LFPV passent au-dessus de l’ILS de LFPO.
