---
title: Le radar sol vSMR
description: 
published: true
date: 2026-07-19T19:37:46.927Z
tags: 
editor: markdown
dateCreated: 2026-03-03T20:42:36.761Z
---

![banner_tools_fr.png](/banners/banner_tools_fr.png)
# Introduction
Le plugin vSMR a été développé par Pierre Ferran, Daniel Lange, Even Rognlien, Juha Holopainen, Lionel Bischof et Wenjun Zhou. Le wiki complet de vSMR est disponible en suivant <a href="https://github.com/pierr3/vSMR/wiki" target="_blank">ce lien</a>. 


Il simule le système NOVA 9000 A-SMGCS sur EuroScope, dans le but de reproduire au mieux le radar sol utilisé sur LFPG en réel. vSMR est installé par défaut dans le pack contrôleur de French vACC, et activable pour les vues sol.

# La barre de menu

## Sélection du terrain observé

La barre de menu de vSMR possède de nombreuses fonctionnalités, mais seulement quelques-unes seront utilisées lors de l'observation. Par défaut elle ressemble à ceci :

![barre_vsmr.png](/doc-atc/barre_vsmr.png)

Le premier élément à gauche correspond à l'aéroport que vous observez, remplacez-le en cliquant simplement sur le code déjà entré, par le code ICAO en question, par exemple LFMN.

## Le menu display

Le menu Display comporte 4 options, nous allons en voir deux d’entre elles : SRW 1 et SRW 2

![menu_display_vsmr.png](/doc-atc/menu_display_vsmr.png)

Chaque option SRW permet de faire apparaître une fenêtre permettant de visionner l'axe d'approche des pistes en services pour l'atterrissage, sans avoir à dézoomer.

![swr1.png](/doc-atc/swr1.png)

Vous pouvez modifier la taille de la fenêtre en cliquant et maintenant le petit carré noir en bas à droite, et la déplacer en maintenant cliqué le partie gris clair en haut de la fenêtre. Les boutons R, F et Z permettent de régler respectivement _la rotation de l'axe de piste_, _l'altitude maximale des appareils affichés_ et _le niveau de zoom de la fenêtre_. La croix sert évidemment à fermer la fenêtre SRW.

## Le menu target

Le menu Target permet de modifier les propriétés d'affichage des plots radar (dans l'ordre : taille de **police**, affichage de **l'historique des positions**, nombre de **positions précédentes affichées** pour les avions au sol et en approche et affichage du **vecteur vitesse**).

![menu_target_vsmr.png](/doc-atc/menu_target_vsmr.png)

Ignorez les fonctions _Acquire_ et _Release_, elles ne sont pas vitales. Les autres fonctions et sous-menus sont très intuitifs.

## Le menu colours

Ici encore, ce menu permet de personnaliser vSMR, en choisissant entre les couleurs Jour et Nuit dans le premier sous-menu, ou de régler les intensités lumineuses des différents éléments dans le second.

![menu_colours_vsmr.png](/doc-atc/menu_colours_vsmr.png)

## Le menu alerts

vSMR simule également le système RIMCAS, visant à alerter le contrôleur en cas d'incursion de piste. Cet outil est très utile lorsque le trafic est important.

Les deux premiers sous-menus permettent de sélectionner les pistes surveillées par le système RIMCAS (elles sont automatiquement importées depuis les pistes actives configurées dans EuroScope, mais peuvent être personnalisées grâce à cette option). 

Le troisième sous-menu : _Runway closed_, permet d'afficher un rectangle rouge sur les pistes fermées lors de l'application d'un NOTAM par exemple. Enfin, _Visibility_ sert à spécifier à vSMR si des procédures LVP sont en service, et donc à diminuer le seuil de tolérance du RIMCAS. 

![menu_alerts_vsmr.png](/doc-atc/menu_alerts_vsmr.png)

# Les étiquettes (TAGs)

## Départs

Les trafics ayant déposé un plan de vol au départ de l'aéroport observé apparaîtront en bleu sur le radar. Le tag est très simple à comprendre: indicatif, type d'appareil, SID et piste assignée.
![dep_tag_vsmr.png](/doc-atc/dep_tag_vsmr.png)

Lorsque que le pilote n'a pas encore rentré le code transpondeur assigné, celui ci apparaîtra en rouge précédé de la lettre A à la place du type d'appareil : 

![transponder_rot_vsmr.png](/doc-atc/transponder_rot_vsmr.png)

## Arrivées


Les trafics ayant déposé un plan de vol à destination de l'aéroport observé apparaîtront en rouge sur le radar. Le tag est très similaire à celui d'un appareil au départ : indicatif, type d'appareil et porte/parking assigné. 
![tag_arrivee_vsmr.png](/doc-atc/tag_arrivee_vsmr.png)

##  Autres
Lorsqu'un trafic n'a pas encore envoyé de plan de vol, il apparaît en gris sur le radar. Ici, il a déjà un code transpondeur assigné, mais normalement le type d'appareil est affiché.

![tag_gris_vsmr.png](/doc-atc/tag_gris_vsmr.png)
