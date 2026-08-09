---
title: LFBO - Toulouse Blagnac
description: 
published: true
date: 2026-07-11T12:29:26.079Z
tags: 
editor: markdown
dateCreated: 2026-03-01T08:50:00.461Z
---

# Introduction
Ce manuel vous permet de vous familiariser avec les différentes positions de Toulouse Blagnac : DEL, GND, TWR et APP. En cas de doute, n’hésitez pas à vous rapprocher de l’équipe de formation.

## Disclaimer
Bien que notre objectif soit de fournir un service de contrôle au plus proche de la réalité, certaines pratiques du réel ne sont pas adaptées à l’environnement de simulation en réseau, même sur VATSIM. A ce titre, il est important de savoir s’adapter face : 
- au niveau des pilotes (qui peut varier du débutant au plus expérimenté)
- aux limites propres à chaque simulateur/aéronef (modèle de vol, procédures moindre bruit, etc)
- aux limites de nos outils : même s’il y en a peu, nos radars restent moins performants que nos collègues du réel.

> Rappel : Ce document est à l’usage des contrôleurs sur VATSIM et est donc exclusivement réservé à la simulation.
{.is-warning}

Il convient de vous assurer que vous disposez des connaissances nécessaires pour ouvrir cette plate-forme. Ce manuel est rédigé dans le but de vous apporter des compléments mais ne peut se substituer à l’AIP disponible via le site du <a href="https://www.sia.aviation-civile.gouv.fr" target="_blank">SIA</a>.

## Mise en garde concernant la zone Airbus
L'implantation du constructeur Airbus peut amener un “effet de foule” à la sortie d’un add-on relatif au constructeur. Il convient donc d’apporter une attention particulière aux pilotes souhaitant simuler des procédures en vol hors des sentiers battus, celles-ci n’étant pas publiées. De plus, cela peut engendrer des perturbations, notamment si le pilote ne maîtrise pas bien l’avion qu’il utilise pour la première fois. La courtoisie doit rester de mise et un rappel vers le Code of Conduct peut être suggéré si un pilote n’est pas en mesure de suivre les instructions du contrôleur.

# Généralité
L'aéroport possède 2 pistes orientées Nord-Ouest / Sud-Est.

La plateforme est divisée en trois parties comme suit : 
- la zone “civile” : zone <span style="color:forestgreen">verte</span> est composée de plusieurs terminaux et aires de trafic. Elle reçoit le trafic commercial (T2A, 2B, 2C et D), cargo (Apron A et B), d’aviation générale (Apron G) et d'affaires (Apron C et D).
- les zones “Airbus” : zone <span style="color:royalblue">bleue</span> et <span style="color:purple">violette</span> sont normalement sous AFIS mais sa fréquence n’est pas simulée.

![zones-lfbo.png](/doc-atc/zones-lfbo.png)


# Utilisation du CDM

L’utilisation du CDM (Collaborative Decision Making) est permise sur LFBO. Avant d’ouvrir une position sur Toulouse Blagnac, nous vous recommandons vivement de consulter le MANEX dédié dans la section Documentation du site de French vACC.

# Positions de contrôle
## Synthèse
|Position|Split (if applicable)|Frequency|Callsign|
|:-:|:-:|:-:|:-:|
|LFBO_DEL| |121.705|Blagnac Prévol<br>*Blagnac Delivery*|
|LFBO_GND| |121.900|Blagnac Sol<br>*Blagnac Ground*|
|LFBO_TWR| |118.100|Blagnac Tour<br>*Blagnac Tower*|
|LFBO_APP| |129.305|Toulouse Approache<br>*Toulouse Approach*|
| |LFBO_W_APP|121.105|Toulouse Approache<br>*Toulouse Approach*|
| |LFBO_E_APP|125.180|Toulouse Approache<br>*Toulouse Approach*|

> La fréquence correcte reste celle indiqué par Euroscope.
Elles sont fournies ici à titre informatif.
{.is-info}

# Position Prévol
## Départs
En QFU 14, les procédures de départ attribuées sont celles se terminant avec le suffixe #A ou #H en fonction du type d’appareil : 
un départ en #H pour les avions à hélice
un départ en #A pour les turboréacteurs
En QFU 32, les SID attribuées doivent se terminer avec le suffixe #B. 
Tous les départs montent initialement au FL70.

## Particularités
Il existe des procédures de départ conventionnelles dont les aéronefs non-RNAV peuvent bénéficier en alternative au départ omnidirectionnel publié (cf. cartes en vigueur).

Des restrictions de niveau s’appliquent vers certains aéroports comme décrit ci-dessous :

`LEDA & LESU ≤ FL250` et `LEZH & LEHC ≤ FL270`


Pour plus d’informations, référez-vous aux lettres d’accord (LoA) disponibles dans la section [LoA](/fr/atc/LoA) du site.

## Stratégie en événement
Afin de limiter la quantité de trafic sur la fréquence GND (par impossibilité de dégrouper cette fréquence), la bonne pratique consiste à les garder sur la fréquence DEL, jusqu’au moment où le trafic est prêt à repousser. Cela permet de ne pas saturer la fréquence de la position sol.

# Position Sol
## Repoussages
Une stratégie particulière est utilisée pour les repoussages. Un code couleur associé est reflété en ce sens sur l’AVISO de Blagnac :

![aviso-lfbo.png](/doc-atc/aviso-lfbo.png)

Voici la signification des différentes couleurs : 
- <span style="color:blue">bleu</span> : repoussage face au nord
- <span style="color:orange">orange</span> : repoussage face au sud
- <span style="color:purple">violet</span> (V10/V12/U42): repoussage sur l’aire R (aéronef d’envergure ≤36 m) si celle-ci est libre
- <span style="color:gold">jaune</span> : pas de contrainte particulière

## Roulage
Au roulage, il est préférable de donner la priorité aux trafics sortant de l’aire de trafic en les faisant rejoindre de la manière la plus directe le taxiway P.
Au départ il existe un risque d’incursion de piste depuis les postes E, F et K en utilisant le taxiway T40 dans le cas où le pilote n’arrive pas à identifier clairement les taxiways P20 et P40 ainsi que depuis les postes U et E dans le cas où le pilote n’arrive pas à identifier clairement les taxiways P55 et P60.

Les portes **E** accueillent les avions de compagnies dites régulières (ex. AFR / ACA / CCM / KLM…).
Le terminal **D** (portes U et V) accueille les arrivées non Schengen.
Les portes **F** accueillent les compagnies low-cost.
Les postes **K** au large en face du T2A accueillent les avions régionaux (le plus souvent turbo-prop).
Les aires **A** et **B** accueillent le cargo; les aires **C** et **D** l’aviation d’affaire; l’aire **G**, l’aviation générale.
Les aires au sud de la plateforme sont **réservées au constructeur Airbus**.

Le Gate Assigner vous simplifie ce travail en attribuant des postes libres et cohérents.

Pour les postes **A**, **B** et **C**, une attention particulière doit être apportée. En effet, certains sont autonomes et d’autres empêchent le repoussage sur les emplacements voisins.

## Points d'attente
Au départ, le roulage s’effectue de manière générale vers les points d'attente en bout de piste si le pilote ne s’est pas annoncé preneur d’une intersection. Pour des raisons de réductions des nuisances sonores sur le créneau 2200-0600LT, les restrictions ci-contre s’appliquent.

|QFU|Départs|Arrivées|
|:-:|:-:|:-:|
|14|2200-0000LT : M10 ou S10<br>0000-0600LT : Bout de piste|14R uniquement|
|32|Bout de piste|32L uniquement|
|En situation de vent faible (<5 kts).<br>Le QFU 14 est utilisé jusque peu avant 0600LT.|||

En situation de LVP, la piste 14R est la seule piste utilisable, les départs se font depuis les points d’attente S11 et M11 uniquement.
La piste 14L/32R n’est pas dotée d’approche Cat II ou III, elle est donc mise hors d’exploitation.

# Position Tour
## Configuration préférentielle
Pour des questions de nuisances sonores, la piste la plus proche du terminal civil (14L/32R) est recommandée pour les décollages. La seconde (14R/32L) est quant à elle privilégiée pour les atterrissages.
Il n’y a pas de QFU préférentiel. Cependant, en raison de l’environnement (de la ville de Toulouse notamment), le QFU 32 est davantage utilisé, en particulier par vent faible.

## Gestion des mouvements simultanés
Il existe différentes façons d'opérer le doublet, celles-ci dépendent des conditions météorologiques actuelles. Elles sont décrites ci-dessous : 

- En VMC* : Les pistes sont considérées indépendantes si les rafales <25 kts et pas de cisaillement.
- En IMC : Les pistes sont considérées <u>inter</u>dépendantes.

*Rappel des minimas VMC : visibilité ≥5000m & plafond ≥1500ft.

## Cadences départs/arrivées
Voici les capacités de Toulouse-Blagnac connues et applicables sur VATSIM : 
- Départs : Un départ chaque 2m 30s en moyenne.
- Arrivées : Une arrivée chaque 2m 30s en moyenne (6NM à 180kts).
- En LVO : 
  - Arrivées consécutives &rarr; 4m30s de séparation (14NM à 180kts).
  - Arrivées non consécutives &rarr; 6m de séparation (18NM à 180kts).

Référez-vous à l’AIP pour consulter les fréquences associées aux radiobalises d’approches.

## Gestion globale
La tour est responsable des mouvements de Toulouse Blagnac mais également du trafic de Toulouse Francazal (LFBF). S’agissant d’une position AFIS (service d’information et d’alerte uniquement), il est recommandé de se familiariser avec les procédures de l’aérodrome.

Blagnac dispose de procédures de faible visibilité activées lorsque le RVR < 550 mètres et/ou plafond < 200 pieds. Les arrivées doivent dégager par M2 ou S2 en extrémité de piste.
En conditions LVP, il faut ajouter la mention “LVP in force” dans l’ATIS.

## Bretelles interpiste
De par la proximité des pistes, il est nécessaire de privilégier les trafics dégageant la piste pour ne pas congestionner les points d’attente inter-pistes (Il y a ~120 m entre deux points d’attente).

Afin de fluidifier les traversées de piste, la clairance suivante peut être utilisée : 

<p align="center">“Air France 123, traversez piste 32R. De l’autre côté, contactez le sol...”<br>
“Air France 123, cross runway 32R, after crossing contact ground…”</p>

## Gestion du trafic VFR
La carte VAC précise le sens du circuit. Il convient de rester flexible si les contraintes opérationnelles le justifient.

Des itinéraires VFR publiés existent. Se référer à la carte VAC pour plus d’informations.

# Position Approche
## Dégroupage
L’approche est dégroupable en deux positions INI (_W_APP et _E_APP) et un ITM (la position par défaut _APP)

Plusieurs aéroports dotés de procédures IFR sont sous la responsabilité de Toulouse Approche :
<p align="center">Castres, Albi, Cahors, Pamiers, Carcassonne, Muret et Francazal</p>

En ce qui concerne la gestion du trafic VFR, un SIV couvre la région de la surface du sol jusqu’au niveau de vol 145.

L’approche INI livre les trafics à l’ITM au plus tôt en vent-arrière ou équivalent si possible, les trafics doivent être en descente vers 5000ft, limités à 220 kts et non conflictuels.

## STAR

|QFU|STAR|IAF|
|:-:|:-:|:-:|
|14|#S|AGN, SURAS, ADIMO et FUZAP|
|32|#N|OGRIL, SULIT, AGENO, ADIMO, FUZAP|

Les pilotes doivent toujours être au-dessus ou au niveau de vol FL80 lorsqu’ils arrivent sur les IAF; ceci afin de les espacer avec les départs clairés initialement au FL70.

## Remise de gaz
Par simplicité, la remise de gaz est donnée dans l’axe de piste. 
Dans le cas où la manœuvre mène à une perte de séparation si aucune autre action n’est prise, le contrôleur Tour doit immédiatement chercher une solution pour récupérer la séparation <u>en coordination avec le contrôleur Approche</u>.

## Transit IFR au sein de la TMA
En cas de navigation entre deux localités situées dans la TMA de Toulouse, un itinéraire RNAV contournant la TMA 2 de Toulouse est défini dans les 2 sens par les points `GAI-MONIX-RAPES-ADSER-DODOM-AGN-LACOU-GOSAD-GAI` pour permettre les transits entre les aérodromes d’Agen, Albi, Castres, Carcassonne, Muret et Pamiers. Les transits se font obligatoirement en desous du FL75.
