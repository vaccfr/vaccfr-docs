---
title: LFMN - Nice Côte d'Azur - Legacy
description: 
published: true
date: 2026-07-11T12:58:38.776Z
tags: 
editor: markdown
dateCreated: 2026-03-01T10:27:15.159Z
---

# Introduction
Le but de ce document est de poser la théorie nécessaire pour obtenir une accréditation sur les positions DEL, GND, TWR et APP de LFMN. En complément, des sessions pratiques avec un mentor sont nécessaires pour obtenir cette accréditation. **Il n’est pas permis d’ouvrir LFMN sans cette accréditation**.

Ce document a été rédigé en partant du principe que la personne le lisant possède le niveau contrôleur requis pour la position pour laquelle il demande l'accréditation. Certaines notions ne sont pas expliquées en détail car considérées comme acquises.

## Accréditation
L’aéroport de Nice Côte d’Azur étant un “Tier 1 Airport”, y ouvrir une position est soumis à une accréditation, autrement dit l’autorisation d’un mentor ou du département training de French vACC.

Pour de plus amples informations sur l'accréditation, les modalités d’obtention et sa validité, merci de vous référer au [Règlement de formation ATC](/fr/atc) ou au département training de French vACC.

## Cursus
Afin d’obtenir l’accréditation sur les positions vigie de LFMN (DEL, GND et TWR) vous devez :
- Avoir lu ce document (partie vigie correspondante au minimum)
- Avoir suivi le cours théorique et réussi le test théorique
- Faire au minimum 2 sessions avec un mentor (une simulation et une session en tandem)

Pour obtenir l’accréditation sur les positions radars de LFMN vous devez :
- Avoir lu ce document dans son intégralité
- Avoir suivi le cours théorique et réussi le test théorique
- Faire au minimum 2 sessions avec un mentor (une simulation et une session en tandem)

## Disclaimer
Bien que notre objectif soit de fournir un service de contrôle au plus proche de la réalité, certaines pratiques du réel ne sont pas adaptées à l’environnement de simulation en réseau, même sur VATSIM. A ce titre, il est important de savoir s’adapter face : 
- au niveau des pilotes (qui peut varier du débutant au plus expérimenté)
- aux limites propres à chaque simulateur/aéronef (modèle de vol, procédures moindre bruit, etc)
- aux limites de nos outils : même s’il y en a peu, nos radars restent moins performants que nos collègues du réel.

> Rappel : Ce document est à l’usage des contrôleurs sur VATSIM et est donc exclusivement réservé à la simulation.
{.is-warning}

Il convient de vous assurer que vous disposez des connaissances nécessaires pour ouvrir cette plate-forme. Ce manuel est rédigé dans le but de vous apporter des compléments mais ne peut se substituer à l’AIP disponible via le site du <a href="https://www.sia.aviation-civile.gouv.fr" target="_blank">SIA</a>.

# Présentation de l’aéroport
L’aéroport possède 2 pistes, elles sont orientées Nord-Est / Sud-Ouest en fonction de la topographie et non des vents dominants.


L’aéroport se compose de 2 terminaux :
- Le terminal 1, il longe S et T
- Le terminal 2, il longe C et T

Ainsi que 3 aires supplémentaires :
- Le parking Kilo
- Le terminal fret, au Nord du T2
- Les FATOs et stands pour hélicoptères au Sud

![apron-lfmn.png](/doc-atc/apron-lfmn.png)

# La position DEL
## Départs
A Nice, sont utilisés par défaut les départs #A au QFU 043 et #X au  QFU 223.
Tous les départs doivent monter au FL100 sauf dans les 2 cas suivants : 
- Les départs Nord sont clairés au FL130 (PERUS, BODRU, BADOD, OKTET et IRMAR)
- Les avions équipés de turbopropulseurs doivent être clairés au FL70 sur les départs #B (QFU 043) ou #Y (QFU 223). Ces départs n’existent pas pour les départs Nord où la règle précédente s’applique.

Bien que tous les niveaux initiaux soient publiés pour tous les départs, la bonne pratique est de prendre le temps de les donner sur VATSIM afin d’éviter toute surprise.

## Cas particuliers
A Nice, tous les départs sont RNAV 1 (y compris les départs omnidirectionnels publiés), pour les trafics ne pouvant pas suivre de procédure RNAV 1*, il faudra coordonner avec le départ et la tour un départ omnidirectionnel suivi d’un guidage radar. Le plus souvent, celui-ci sera similaire à la procédure d’API**  en service.

Il existe des limitations de RFL pour les trafics à destination de Genève (LSGG), Zurich (LSZH) et les terrains en Corse.

`LSGG : RFL < FL240 | LSZH : RFL < FL320 | Corse : RFL < FL130`


Pour IRMAR, BADOD et OKTET seulement (nécessite l'accord de l’approche):
- Départs #C : aéronefs avec taux de montée initiale faible, sur demande de l’équipage (QFU 043)
- Départs #Z : aéronefs avec taux de montée initiale faible, sur demande de l’équipage (QFU 223)
- IRMAR #P : QFU 223 seulement, aéronefs très haute performance, sur demande de l'équipage.

*RNAV1: Voir paragraphes 22.4.2.2 et 22.4.3 de l’AIP
**API:  approche interrompue

## Stratégie en événement
Afin de limiter la quantité de trafic sur la fréquence GND (par impossibilité de dégrouper cette fréquence), la bonne pratique consiste à les garder sur la fréquence DEL, jusqu’au moment où le trafic est prêt à repousser. Comme sur toutes les plateformes, l’utilisation du PDC est conseillée.

# La position GND
## Repoussages
Sur la plateforme de Nice les directions de repoussage sont publiées pour tous les stands “Nose-in” à l'exception des stands 19 à 23 inclus. Malgré cela, la direction du repoussage sera toujours précisée par le contrôleur GND pour éviter toute confusion sur le réseau.

Les stands entre T et U ne nécessitent pas de repoussage, cependant il est possible qu’il soit demandé par les pilotes sur le réseau. Il en est de même pour les stands se trouvant entre S, D et T  à l'exception des stands 7 et 9 (Face Nord) qui doivent repousser sur T et le stand 15 (Face Sud) qui doit repousser sur S.

Ci dessous sont décrits les principaux sens de repoussage publiés :
- C, repoussage face Sud (du stand 40B au stand 48)
- D, repoussage face Sud préférentiel. Face Nord possible en fonction de la situation au sol.
- S, stand 24 inclus à 10B, repoussage face à l'Est pour rouler via T ou D.
- T depuis le T1 ou le T2 repoussage face au points d’attente en service.
- Stand 40A et Cargo (28 et 26), repoussage face Ouest pour rouler sur C. Il est possible de coordonner avec l'équipage un repoussage face au Nord sur C pour rouler à droite sur S.

Pour les stands 62 à 50 au QFU 043, il est préférable de faire repousser face Ouest pour éviter la congestion de C.

![taxi-lfmn.png](/doc-atc/taxi-lfmn.png)

## Roulage
De façon générale, il est conseillé d’utiliser T pour les trafics au départ et U pour les arrivées. Ceci est applicable dans les deux configurations de piste. 

Le terminal 2 accueille les avions SkyTeam, EasyJet, Emirates.
Le terminal 1 toutes les autres compagnies. L’aviation générale et d’affaire sera garée au parking K.

Pour fluidifier les mouvements au sol à l’arrivée et éviter de bloquer la piste, il est possible de coordonner avec le contrôleur TWR un roulage initial en sortie de piste. 

Aussi, pour donner plus de flexibilité au contrôleur TWR,  il est de bonne pratique de proposer aux trafics Light un départ depuis B3 (TORA 2157m) en 04R.

Il est important de noter qu’il n’y a pas de point de roulage intermédiaire à Nice, il convient donc d’utiliser des clairances du type “Roulez et maintenez avant… / Taxi and hold short of…”, ce type de clairance est important pour laisser les trafics au départ sortir du terminal avant de faire rouler les arrivées vers leur porte via C, S et D.

Pour les restrictions au roulage, référez-vous à l’AIP (GMC 01, 02, 03, 04 et 05).

## Points d’attente
A Nice, il y a respectivement 2 et 3 points d’attente utilisables :

En QFU 223 H1 ou G1 sont utilisés pour traverser la piste 22R, G1 permet de garder plusieurs avions du côté de la piste de départ sur Y après la traversée et permet ainsi de stabiliser le taux de départ dans les situations de grande charge.

En QFU 043 il existe 3 points d’attente, A1, B1, et C1. Il est préférable de limiter l’utilisation de B1 aux trafics VFR au départ de la piste 04L. 

Il est recommandé d’utiliser soit C1 soit A1 (préférentiel). Il est important de noter qu’en situation de charge élevée, le point d’attente C1 peut très rapidement saturer et bloquer les taxiways U, C et T et ce avec seulement 2 trafics présents.

Pour éviter cette situation (lors d’un événement avec de nombreux départs par exemple) faire rouler les trafics au départ vers A1 permet de parer à toute situation de blocage important.

L’utilisation de plusieurs points d’attentes en simultané n’est pas recommandé afin de limiter les risques de conflits après la traversée de la piste intérieure.

C1 reste néanmoins une bonne option pour réduire et faciliter le roulage au départ lorsque le nombre de mouvements simultanés est faible. Il sera nécessaire de l’utiliser pour les trafic souhaitant partir depuis l’intersection B3.

B1 quant à lui est une bonne option pour les trafics VFR au départ car ils ne gêneront pas les mouvements IFR au sol.

## Cas particulier ILS 04L
Si pour cause météo la procédure d’ILS doit être utilisée en piste 04L il est important de retenir le point suivant.

Il est interdit de faire attendre un trafic au point d’attente A1 lorsque la procédure ILS 04L est en service et qu’un trafic doit s'établir sur le glideslope.
Cette restriction est due à la proximité entre le point d’attente A1 et l’antenne du glideslope de la piste 04L afin de ne pas perturber le signal. 

De plus, il est demandé aux équipages de libérer la piste par F1 ou EG/G1 afin de limiter les perturbations du signal LOC.

![lfmn-hp-a1.png](/doc-atc/lfmn-hp-a1.png)

# La position TWR
## Les pistes
Les 2 pistes de l’aéroport forment un doublet rapproché spécialisé et sont donc interdépendantes. C'est-à-dire qu’il n’est pas possible de faire décoller ou atterrir deux avions en même temps.

La piste Sud est dédiée aux décollages et la piste Nord dédiée aux atterrissages contrairement à la pratique la plus courante qui consiste à utiliser la piste la plus proche des installations.

Le QFU 043 est préférentiel compte tenu des minimas, de la météorologie et de la topographie.
On utilisera le QFU 043 jusqu’à une composante de vent arrière de 6 kts inclue.

La cadence des pistes en fonctionnement normal (atterrissage + décollage) est de 38 à 45 mouvements par heure. Lors d’opérations en piste unique la cadence est réduite entre 30 et 37 mouvements par heure.

## Dégagement et traversée de piste
De par sa conception et la spécialisation du doublet, seuls les trafics au départ nécessitent de traverser la piste intérieure. Les clairances de traversée sont la responsabilité du contrôleur TWR, tout comme le roulage jusqu'à la piste extérieure.

Pour rappel, en France, **il n’est pas possible de donner des clairances conditionnelles de traversée**. Une clairance de traversée peut-être donnée dès que le trafic occupant la piste passe ou a passé le point d’attente à partir duquel se fera la traversée.

Après la traversée au QFU 043, on fera rouler les trafics Medium au point d’attente Q3 et les Heavy en W3. Le sol proposera aux trafics Light (Business Jet notamment) un départ depuis B3 (TORA 2157m) cependant si la charge de trafic ne le permet pas alors ils rouleront au point d’attente Q3.

A cause de la proximité immédiate après la traversée de la piste 04L, il n’est plus possible d’utiliser l’intersection A3 pour le départ ou l’arrivée.

Lors du dégagement et afin de ne pas bloquer la piste et les points d’attente à cause de la proximité du taxiway U en sortie de piste, il est possible de coordonner avec le contrôleur GND un roulage initial après la traversée (cf. [Roulage](#roulage)).

Exemple pour un trafic à l’arrivée en 04L :
**<p align="center">“AFR22RJ, roulez à gauche sur U et contactez le sol sur 121.705, au revoir”</p>**

Il convient de noter qu’il n’existe sur la piste intérieure qu’une seule voie de dégagement rapide, il s’agit de EG en QFU 043. 

## Remises de gaz
Dans le cas d’une remise de gaz, sur VATSIM, sont systématiquement donnés : 
- un cap
- une altitude

Le tout en coordination avec le contrôleur approche.

Il faut savoir que l’API qui doit être suivie n'est pas la même si le trafic suit toujours une approche instrumentale ou si il est engagé sur une VPT. Afin d'éviter toute confusion des pilotes sur le réseau, on évitera les clairances de type “Remettez les gaz comme publié”.
 
Le guidage de remise des gaz est donc à coordonner avec le contrôleur d'approche (LFMN_APP ou LFMN_F_APP). Cela est d’autant plus important au QFU 223 car les procédures APIs publiées ne contiennent pas de cap.

Pour rappel : l’approche doit être informée de toutes les remises de gaz et lorsque c’est possible, le tag doit être mis à jour en fonction (Cap et altitude donnés).

## VFR

![vac-lfmn.png](/doc-atc/vac-lfmn.png)

### Tour de piste
Le circuit de piste est à 1000ft au Sud des installations peu importe la configuration de piste utilisée.

De part la situation très confinée du tour de piste entre les trajectoires de départ et d'arrivée IFR, il est recommandé de ne pas accepter de trafic en tour de piste lorsque la charge de trafic IFR à l'arrivée est importante. Dans cette situation, pour les trafics au départ de Nice, il est préférable de leur proposer un vol local ou une navigation.

### CAG
Il existe à Nice 4 points d’entrée (EW, NA, SB et EC) et 2 transit VFR nommés, ceux-ci se trouvent au Nord (N1) et Nord-Ouest (W1) des installations et font respectivement route depuis NA et WE vers WN (1500ft minimum).

Les intégrations du Nord (via WN) se font sur clairance à 1500ft à la verticale des installations pour rejoindre le circuit de piste au Sud des installations à 1000ft. 

Les arrivées du Sud et du Nord-Est ainsi que les transit côtier se font entre 500ft et 1000ft maximum afin de passer sous les arrivées IFR avant de rejoindre le circuit de piste.

Pour tous les trafics VFR la vitesse est limitée à 160 kts dans l’intégralité de la CTR. Toute évolution à une vitesse supérieure devra faire l’objet d’une demande de clairance spécifique.
Le VFR spécial n’est <u>pas autorisé</u>.

### Hélicoptères
Pour les trafics à voilure tournante, l’altitude de transit sera limitée à 500ft. Il faudra les clairer sur des points d’arrivée (HS ou HE) pour les différentes FATOs. Les FATOs s’utilisent dans le même sens que les pistes (ex. 04L/R = MS pour l'atterrissage et ME pour le décollage).

Pour les hélicoptères au départ ou à l'arrivée de Monaco, il faudra les clairer jusqu’à EC puis leur donner une info trafic si nécessaire
car la CTR de Monaco n’est pas couverte par la tour de Nice.

![fato-lfmn.png](/doc-atc/fato-lfmn.png)

# La position APP
## Secteur

![lfmn-ats.png](/doc-atc/lfmn-ats.png)

## Dégroupage
Lorsque la charge de trafic oblige, la TMA de Nice peut être degroupée en 4 secteurs.

**_APP** : La position standard, couvre en temps normal toute la TMA et le SIV.

Dégroupage, avec l’approche finale (_F_APP) : _APP prend en charge les trafics arrivant par l’Ouest (NISAR, XIRBI, PERUS, ABDIL, TUPOX, ABLAK et BIRGO) et ce jusqu'à MUS, cela inclut le circuit d’attente lorsqu’il est nécessaire.

Les transferts vers _F_APP se font au cap avant ou après MUS. 
Lorsque l’attente est ouverte, la stratégie à privilégier consiste à faire descendre le trafic au FL80 et de le transférer à la finale qui lui fera quitter l’attente.

Dans le cas où le secteur _F_APP n’est pas ouvert _APP sera en charge des trafics jusqu’à l’IF.
Si _E_APP n’est pas ouvert c’est également _APP qui sera en charge des arrivées Est comme décrit ci-dessous. 

**_DEP** : Comme son nom l’indique, le secteur départ est en charge de tous les départs mais aussi du service top-down de la tour de Cannes. Le seul secteur requis pour ouvrir le départ est _APP.
Il faut faire attention à la montée des départs BASIP en présence d’arrivées BORDI ou VEVAR qui se croisent à 1000ft au niveau de MIKRU, de préférence les départs au FL100 et les arrivées au FL110 comme prévu par les contraintes des STARs.

**_E_APP** : Il s’agit du secteur d’approche initiale Est, il est en charge des arrivées depuis l’Est (VEVAR, BORDI, OZMIC, KERIT, SODRI et LONSU) et ce jusqu’à NERAS, cela inclut le circuit d’attente lorsqu'il est nécessaire. Le seul secteur requis pour ouvrir _E_APP est _APP.

Il faut faire attention lors des clairances de descentes des trafics arrivant par VEVAR et BORDI, ces derniers croisent la trajectoire des départs BASIP. Il convient de les clairer vers le FL110 en accord avec les MVA pour assurer une séparation verticale de 1000ft au niveau de MIKRU.

Les transferts vers _APP ou _F_APP se font au cap avant ou après NERAS. 
Lorsque l’attente est ouverte, la stratégie à privilégier consiste à faire descendre le trafic au dernier niveau et de le transférer à la finale qui lui fera quitter l’attente.

**_F_APP** : Il s’agit de l’approche finale, il est en charge de la séquence vers l’IF pour l’approche en service. Il gère les trafics entre MUS et NERAS ainsi que de la sortie des attentes lorsqu’elles sont nécessaires. Pour ouvrir la finale, il faut au minimum que _APP et _TWR soient présents. 

**_I_APP** : Ouvert rarement, ce secteur couvre uniquement le SIV de Nice pour le service d’information en vol en dehors de la TMA (de la surface au plancher de la TMA).

## Altitudes Minimales de Guidage
Les altitudes ci-dessous sont à respecter obligatoirement lorsque les trafics sont en guidage radar ou lorsqu’ils sont en direct vers un point. Comme indiqué, les altitudes sont corrigées pour les faibles températures.

![lfmn-amg.png](/doc-atc/lfmn-amg.png)

Pour les approches initiales en CDO, on donnera la clairance de descente vers l’altitude plateforme de l’approche une fois que le trafic sera dans la zone de la MVA correspondante, il sera en même temps clairé pour l’approche.

## Trajectoires de départ
Les trajectoires des départs Nord passent entre les arrivées de l’Est et de l’Ouest. Les départs Sud passent au centre de la zone de guidage radar.

Verticalement, les départs passent au-dessus des trafics en guidage radar. Les départs BASIP montent au FL100 et passent sous les arrivées VEVAR et BORDI. Les arrivées doivent passer MIKRU au FL110 ou plus. Il faudra donc faire attention aux clairances de montée des départs en présence d’arrivées du Nord-Est.

Les niveaux initiaux sont expliqués dans la partie [Départs](#departs).

Les transferts vers LFMM ou LFMM_E se font au FL140 pour tous les départs sauf les départs Nord qui doivent monter au FL170, les départs BASIP peuvent monter vers le niveau FL160 si non conflictuel (cf. COPX).

Trajectoires détaillées : cf. SID_RWY22L-22R_RNAV et SID_RWY04L-04R_RNAV


## Trajectoires d’arrivée
Les arrivées sont livrées par LFMM ou LFMM_E au FL140 sur AMFOU, KESAK, BIRGO, au FL180 sur GAPDO et FL170 sur BORDI (LFMM ou LIMM). 

Trajectoires détaillées : cf. STAR_EAST_RWY_ALL_RNAV et STAR_WEST_RWY_ALL_RNAV

Vous trouverez dans la section Documentation du site un <a href="https://docs.google.com/drawings/d/10OFXJ6PaY8aUfL3Pki6LQ_u5X8lxPYKWxkKKd0uPIok/view" target="_blank">diagramme de guidage radar</a> des avions à l’arrivée.

## Circuits d’attente

![lfmn-holds.png](/doc-atc/lfmn-holds.png)

## Point Merge
**Config 04**
Lors du guidage radar vers l’IAF (BISBO ou LEMPU ), il est pertinent d’utiliser la technique du point merge. Le réglage optimal est d’utiliser des arcs de 7NM pour BISBO et LEMPU avec des vecteurs de vitesse de 2 minutes.

**Config 22**
Lors du guidage radar vers l’IAF (NANAX), il est pertinent d’utiliser la technique du point merge. Le réglage optimal est d’utiliser des arcs de 8NM avec des vecteurs vitesse de 2 minutes, ce nautique additionnel permet d’augmenter légèrement l’espacement entre les trafics à l'arrivée car il n’existe pas de voie de dégagement rapide au QFU 223.

### Remises de gaz (API)
Sur le réseau, une grande partie des remises de gaz auront lieu sur les VPTs et non sur les approches instrumentales. Pour rappel, l’API qui doit être suivie n’est pas la même si un trafic suit une approche instrumentale ou si il est engagé sur une VPT.

On retiendra donc que : 
- les APIs ILS 04L/R se terminent systématiquement par un guidage radar,
- les APIs RNP se terminent théoriquement à NERAS (sauf RNP Z (AR) 22L/R) mais que dans la pratique ce sera surement un guidage radar,
- les APIs VPT sont des guidages radar.

Complément : cf. [Remises de gaz](#remises-de-gaz)

# Terrains sous la TMA
## LFMD : Cannes Mandelieu
**Départs**
A Cannes, seule la piste 17 est utilisée pour les départs IFR. Les départs montent à 2000ft vers DIMAD puis suivent un guidage radar. Il reste possible d’utiliser la piste 35 pour des départs à vue.

**Arrivées**
Les arrivées Cannes sont similaires à celles de Nice et le transfert depuis LFMM est le même. Les trajectoires passent sous les arrivées de Nice et sont légèrement décalées afin de limiter les interférences. Les STARs se terminent à l'IAF des approches, il faut donc clairer les trafics à l'approche avant NEKIP ou INLOV s’ils ne suivent pas une directe vers un autre point.

**Approches**
Il existe 2 approches préférentielles à Cannes, la LOC A piste 17 suivie de la VPT A 17, et la RNP Y piste 35. Dans le cas de la VPT piste 17, il est possible de clairer un autre trafic sur la VPT seulement si celui-ci rejoint la vent arrière avant que le précédent tourne en finale. Idéalement un espacement suffisant en amont de l’approche LOC permet d'éviter ces situations.

**VFR**
Pour les points suivants, il est bon de se référer à la carte VAC.
Il faut retenir que le circuit de piste diffère (altitude et trajectoire) selon le type avion.
Il existe plusieurs itinéraires de départ et d’arrivée.
Les hélicoptères utilisent de préférence la piste 04/22 via HW et HE (MAX 600ft).
De plus, l’hélistation du Quai du Large (LFTL), se trouve dans la CTR de Cannes, il est donc couvert par la Tour ou MN_APP en top-down.

## LFTZ : La Mole Saint-Tropez
Les trafics IFR à La Mole sont très rares mais existent sur le réseau.

**Départs**
A La Mole, seule la piste 06 est utilisée pour les départs IFR. Les départs montent à 4000ft vers STP puis LERMA, avant de recevoir un guidage radar. Il est possible de donner les clairances de départ mais les trafics devront rappeler passant 3500ft.

**Arrivée**
Les trajectoires d’arrivées sont les mêmes que LFMD et leur gestion est similaire.

**Approche**
Il n’existe qu’une seule approche instrumentale, la VOR A. Les trafics à l’arrivée doivent être clairés en descente jusqu’à 4000ft puis à l’approche. Passant 3500ft, lesdits trafics sortent de l’espace D de la TMA et ne reçoivent par la suite que le service d’information en vol.

**VFR**
Service d’information en vol uniquement, et pour toute info supplémentaire, voir la carte VAC.

## LFTH : Toulon Hyères
Les arrivées LFTH en provenance du Nord traversent le secteur Est de la TMA, il faudra les clairer en descente vers le FL70. L’approche de Nice ne couvrant pas Toulon, il ne faut donc pas donner de clairance d’arrivée ou d’approche.

## SIV
Le SIV de Nice couvre les limites horizontales des TMAs de la surface jusqu’au plancher de la TMA.

Afin d’ajouter une couche de réalisme vous pouvez donner les codes transpondeurs suivant aux hélicoptères évoluant dans le SIV de Nice.

|Transpondeur|5470|5471|5472|5473|5474|5475|5476|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|Destination|Divers|LFTZ : La Mole & Presqu’île de St-Tropez|LFMD : AD Cannes Mandelieu|LFTL : HST Cannes Quai du Large|LFMN : AD Nice Côte d’Azur|LNCM : Héliport Monaco|Vols Panoramiques
