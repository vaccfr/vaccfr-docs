---
title: Edition | LFLL - Lyon Saint-Exupéry
description: SOP LFLL
published: true
date: 2026-03-16T16:03:27.896Z
tags: 
editor: markdown
dateCreated: 2026-03-16T16:03:25.727Z
---

# Introduction
Ce manuel vous permet de vous familiariser avec les différentes positions de Lyon Saint-Exupéry : DEL, GND, TWR et APP. En cas de doute, n’hésitez pas à vous rapprocher de l’équipe de formation.

## Disclaimer
Bien que notre objectif soit de fournir un service de contrôle au plus proche de la réalité, certaines pratiques du réel ne sont pas adaptées à l’environnement de simulation en réseau, même sur VATSIM. A ce titre, il est important de savoir s’adapter face : 
- au niveau des pilotes (qui peut varier du débutant au plus expérimenté)
- aux limites propres à chaque simulateur/aéronef (modèle de vol, procédures moindre bruit, etc)
- aux limites de nos outils : même s’il y en a peu, nos radars restent moins performants que nos collègues du réel.

> Rappel : Ce document est à l’usage des contrôleurs sur VATSIM et est donc exclusivement réservé à la simulation.
{.is-warning}

Il convient de vous assurer que vous disposez des connaissances nécessaires pour ouvrir cette plate-forme. Ce manuel est rédigé dans le but de vous apporter des compléments mais ne peut se substituer à l’AIP disponible via le site du <a href="https://www.sia.aviation-civile.gouv.fr" target="_blank">SIA</a>.

# Généralités
L'aéroport possède 2 pistes orientées Nord / Sud.

La plateforme se compose de 3 terminaux et 3 aprons :
- Le terminal 1 rond au sud,
- Le terminal 2 en forme de vague et dont la partie satellite au nord est fermée,
- Le terminal 3 au large entre les voies TL et TJ,
- Cargo & aviation générale / d’affaire : <br> Apron M (Cargo, hors format etc.) / N (Affaire) / G (CAG).

![lfll-adc01.png](/doc-atc/lfll-adc01.png)

# Utilisation du CDM
L’utilisation du CDM (Collaborative Decision Making) est permise sur LFLL.
Avant d’ouvrir une position sur Lyon Saint-Exupéry, nous vous recommandons vivement de consulter le MANEX dédié dans la section Documentation du site de French vACC.

# Positions de contrôle
## Synthèse

|Indicatif|Découpe|Fréquence|Indicatif d'appel|
|:-:|:-:|:-:|:-:|
|LFLL_DEL| |121.655|Saint-Ex Prévol<br>*Saint-Ex Delivery*|
|LFLL_GND| |121.830|Saint-Ex Sol<br>*Saint-Ex Ground*|
|LFLL_TWR| |120.450|Saint-Ex Tour<br>*Saint-Ex Tower*|
|LFLL_DEP| |131.315|Lyon Départ<br>*Lyon Departure*|
|LFLL_APP| |120.230|Lyon Approche<br>*Lyon Approach*|
| |LFLL_E_APP|136.075|Lyon Approche<br>*Lyon Approach*|

## Position Prévol
### Départs

Les procédures de départ sont attribuées comme suit :

|QFU|17|35|
|:-:|:-:|:-:|
|SID (RNAV)|#S|#N|
|Niveau Initial|FL70 (sauf props)||

Les départs omnidirectionnels sont publiés et à coordonner avec l’APP.

### Particularités
Les départs ASLEG, GEMLA, LUKUM, MADOT, MTL, PIMAK et VEROT sont réservés aux props et interdits dans le créneau 2200-0600 LT*. Ces départs montent initialement à 5000ft.

*Cette restriction ne peut pas être imposée aux pilotes sur VATSIM et n’est donc pas obligatoire.

### Stratégie en évènement
Afin de limiter la quantité de trafic sur la fréquence GND (par impossibilité de dégrouper cette fréquence), la bonne pratique consiste à les garder sur la fréquence DEL, jusqu’au moment où le trafic est prêt à repousser. Cela permet de ne pas saturer la fréquence de la position sol.

## Position Sol
### Roulage
Il est préférable de donner la priorité aux trafics sortant de l’aire de trafic en les faisant rejoindre de la manière la plus directe le taxiway T. Il vaut mieux maintenir un seul sens de circulation sur T.

Voici la répartition des parkings en fonction du type avion et / ou de la compagnie : 

|Parkings|Type avion|Remarque(s)|
|:-:|:-:|:-:|
|B, C et D|gros porteurs|Terminant par B sauf B12|
|L et J|compagnie low-cost|Transavia, EasyJet, etc|
|M, J11 à J19|cargo|ASL, DHL, etc|

Quelques précisions : 
- Les postes E, G, N, M12, C19, A30 et A31 sont autonomes.
- Les postes N1# sont accessibles via TN1, N2# et N3# via TN2 et N4# via TN3.
- Les trafics de catégorie F (AN124, A380, B748,...) accèdent à l’apron via TJ et TL uniquement. 

### Points d'attentes
Au départ, les décollages piste 35L s’effectuent depuis le point d’attente A9 en bout de piste ou depuis A8 sur demande du pilote ou si cela représente un avantage opérationnel.
En cas de forte charge, il est préférable d’utiliser A9.
Sur la piste 17R l’alignement se fait par défaut depuis l’intersection A3 sauf sur demande du pilote.

En condition LVP, seuls les points d’attente CAT II/III suivant sont utilisables : 
- A9 et A8 pour l’alignement en 35L
- B9 pour l’alignement en 35R
- B4 et B3 pour traverser la 35L après l'atterrissage en 35R.

## Position Tour
### Configuration préférentielle
Le QFU 35 est préférentiel pour cause de procédures instrumentales.

Pour garantir la meilleure capacité terrain, les pistes sont exploitées de la manière suivante : 
- pistes 35R/17L de manière préférentielle pour les atterrissages.
- pistes 35L/17R de manière préférentielle pour les décollages.

### Cadences départs/arrivées
La capacité maximale est de 48 mouvements par heure soit ~1m15s entre chaque mouvement, arrivée et départ confondu.
La plateforme étant un terrain A-CDM, la cadence maximale du CDM est de 6 départs chaque 10 minutes.

### Gestion des mouvements simultanés
Il existe deux façons d'opérer le doublet, celles-ci dépendent des conditions météorologiques.

- En IMC, les pistes sont considérées <u>inter</u>dépendantes.
- En VMC*, les pistes sont considérées indépendantes sauf exceptions suivantes :
  - Remise de gaz causée par trop fort vent de travers (reprise 10min après la dernière occurrence)
  - Cisaillement de vent reporté (même condition de reprise)
  - RCC** d'une piste ≤ 4 (reprise à RCC ≥ 5 sur les 2 pistes)
  - Arrivée en procédure VOR/DME ou LOC

*Rappel des minimas VMC : visibilité ≥5000m & plafond ≥1500ft.
**RCC : Runway Condition Code

### VFR
Le circuit de piste se fait à 1800ft à l’est de la plateforme peu importe le QFU utilisé.
Attention à la proximité entre pistes et de la branche de vent arrière.
Des itinéraires de départ et d'arrivée sont publiés, voir la carte VAC pour toutes les informations.

### Gestion globale
La plateforme de St-Exupéry dispose de procédures **LVP**.
Elles doivent être en vigueur au plus tard quand : **RVR = 550m ou plafond = 200ft**.

Seules les pistes 35R et 35L sont dotées d’approche CAT II & III et homologuées pour les décollages par faible visibilité.
Restrictions d’utilisation : 
- dégagement RWY 35L par bretelles A3 ou A4,
- dégagement RWY 35R par bretelles B3, B4 ou V4; dégagement par V5 interdit.

## Position Approche
### Dégroupage	
L’approche peut se dégrouper avec une position supplémentaire (_E_APP) qui ouvre la partie Est de la TMA (ci-contre) et un départ (_DEP).

L’approche Ouest (_APP)  s’occupe des arrivées via TALAR & ARBON et des interceptions sur l’ILS. L’approche Est (_E_APP) s’occupe des départs (si _DEP n’est pas présent) et des arrivées via RIPTU et GOMET.

Le transfert vers l’approche Ouest (_APP) se fait au plus tôt en vent-arrière ou équivalent si possible, les trafics doivent être en descente vers 5000ft, limités à 220 kts et non conflictuels.

Les aéroports suivants sont dotés de procédures IFR et sont sous la responsabilité de l’approche : 

|ICAO|Nom du terrain|Responsabilité||
|:-:|:-:|:-:|:-:|
|LFLY|Lyon Bron|Tout temps||
|LFLS|Grenoble Isère|Tout temps||
|LFLB|Chambéry|Voir ci dessous||
| | |LFLB_APP|Transfert avant GOVNA|
| | |LFMM_CTR|Sur coordination|
| | |UNICOM|Si charge incompatible topdown|

En ce qui concerne la gestion du trafic VFR, un SIV couvre la région de la surface jusqu’au niveau de vol 115 (SIV 2 et 3). Une partie du SIV est au-dessus des TMA/SIV voisin(e)s.
Certains planchers diffèrent: le SIV 1 a pour plancher le niveau 85 (côté Clermont) et les SIV 4,5 le niveau 95 (côté Chambéry).

### STAR
Les STARs sont données par l’en-route comme suit : S au QFU 17, N au QFU 35.
Les IAFs sont communs aux deux QFU.

|QFU|17|35|
|:-:|:-:|:-:|
|STAR / APP INI|S|N|
|IAF|TALAR, RIPTU, ARBON, GOMET||

### Réduction de la séparation radar en finale
La séparation minimale radar de 3 NM peut être réduite à 2,5 NM entre deux aéronefs en approche finale 17L ou 35R lorsque l’aéronef qui précède appartient à une catégorie de turbulence de sillage inférieure ou égale à la catégorie de l’aéronef qui suit.
Cette réduction ne doit pas être systématique, elle permet plutôt d'éviter une remise de gaz autrement nécessaire.

### Remise de gaz
Les remises de gaz doivent être données comme publiées ou coordonnées avec l’approche.
