---
title:  Edition | LFPG - Paris Charles de Gaulle
description: 
published: true
date: 2026-03-27T13:30:22.347Z
tags: 
editor: markdown
dateCreated: 2026-03-01T11:44:32.628Z
---

# Introduction
Le but de ce document est de poser la théorie nécessaire pour obtenir une accréditation sur les positions DEL, GND et TWR de LFPG. 

Ce document a été rédigé en partant du principe que la personne le lisant possède un niveau contrôleur S2 ou plus. Certaines notions ne sont pas expliquées en détail car considérées comme acquises.

## Accréditation

Paris Charles De Gaulle étant un “Tier 1 Airport”, y ouvrir une position est **soumis à une accréditation**, autrement dit une autorisation d’un mentor ou du département training de la French vACC.

Pour de plus amples informations sur l'accréditation, les modalités d’obtention et sa validité, merci de vous référer au [**Règlement de formation ATC**](https://doc.vatsim.fr/fr/atc/documentation/reglement-atc) ou au département Formation ATC de French vACC.

## Cursus 

Afin d’obtenir l’accréditation sur les positions LFPG_DEL/GND/TWR vous devez :
- Avoir lu ce document 
- Avoir suivi le cours théorique et réussi le test théorique
- Faire au minimum 2 sessions avec un mentor (une simulation et une session en tandem)

## Disclaimer

Bien que notre objectif soit de fournir un service de contrôle au plus proche de la réalité, certaines pratiques du réel ne sont pas adaptées à l’environnement de simulation en réseau, même sur VATSIM. A ce titre, il est important de savoir s’adapter face : 

- au niveau des pilotes (VATSIM est utilisé par des utilisateurs avec une grande amplitude de niveau de pilotage)
- aux limites propres à chaque simulateur/aéronef (modèle de vol, procédures moindre bruit, etc)
- aux limites de nos outils : même s’il y en a peu, nos radars restent moins performants que nos collègues du réel.

> Rappel : Ce document est à l’usage des contrôleurs en formation sur VATSIM et est donc exclusivement réservé à la simulation.
{.is-warning}

Il convient de vous assurer que vous disposez des connaissances nécessaires pour ouvrir cette plate-forme. Ce manuel est rédigé dans le but de vous apporter des compléments mais ne peut se substituer à l’AIP disponible via le site du [SIA](https://www.sia.aviation-civile.gouv.fr/).

# Généralité 

L’aéroport possède 4 pistes : 
- 2 au nord appelées “doublet nord", les pistes 09L/27R et 09R/27L.
- 2 au sud appelées “doublet sud”, les pistes 08R/26L et 08L/26R.

> Sur chaque doublet, la piste extérieure est utilisée pour les atterrissages, la piste intérieure pour les décollages. 
> 
> {.is-info}
> 
{.is-info}

L’aéroport possède 3 terminaux principaux :
- Le terminal 1
- Le terminal 2 (le plus grand)
- Le terminal 3

Ainsi que plusieurs aires pour le cargo :
- L’aire I pour Fedex
- Les aires M, N et P pour le cargo

L’aéroport possède également des parkings et des hangars pour la maintenance Air France, ainsi qu’une aire et une piste pour hélicoptère.


![lfpg_presentation](/doc-atc/lfpg_presentation.png)

# La position Prévol (DEL)

> La position DEL de LFPG est particulièrement stratégique. Une lecture attentive et une bonne compréhension de cette partie du MANEX est donc nécessaire.
{.is-warning}

## Configuration de l'aéroport 

Roissy-CDG et Orly ont des pistes globalement orientées Est-Ouest. Par conséquent, selon le vent, on dit de ces aéroports qu’ils sont en configuration “face à l’Est” ou “face à l’Ouest”.

Dans la très grande majorité des cas, les 2 aéroports adoptent la même configuration, le vent étant sensiblement le même, ou très peu contraignant. On parle alors de configuration “Est liée” ou “Ouest liée”.

Plus rarement, le vent diffère suffisamment sur les 2 terrains pour que chacun opère dans un sens différent. On parle alors de configuration “inverse”.

<div align="center">
  
**Ouest Lié (WL)**
QFU LFPG = 26 et 27
QFU LFPO = 24 et 25
**Est Lié (EL)**
QFU LFPG = 08 et 09
QFU LFPO = 06 et 07
**Ouest Inverse (WI)**
QFU LFPG = 26 et 27
QFU LFPO = 06 et 07
**Est Inverse (EI)**
QFU LFPG = 08 et 09
QFU LFPO = 24 et 25
</div>

La tour de CDG détermine le sens des départs à LFPG tandis que la tour d’Orly détermine le sens des départs à LFPO. Dans le cas où la tour d’Orly n’est pas présente, ce sera l’approche d’Orly ou l’approche de CDG ou encore Paris Contrôle qui déterminera le sens des départs à LFPO.

> N.B. : LFPB suit systématiquement la configuration de LFPG; LFPN et LFPV systématiquement celle de LFPO.
{.is-info}

## Les SID 

Toutes les informations sont sur le [diagramme des départs](https://docs.google.com/drawings/d/172W9ZwUn3SCECGKxHIm4hyMI1-lQix9soZXAL3OscYk/edit?usp=sharing). Lisez-le attentivement et surtout, **utilisez-le lors de vos sessions de contrôle !** Toutes les SID sont RNAV.

Les départs #Z, en configuration face à l’Ouest, ne sont attribués qu’aux avions ne pouvant pas respecter la pente ATC minimum de 6.5%, ou aux éventuels avions trop bruyants (CONC, B742, T154). Vous ne les rencontrerez que rarement sur VATSIM.

De part les interactions entre les départs et les arrivées, les niveaux de montée initiaux seront **à communiquer et à respecter scrupuleusement.**

## Configuration de roulage 

L’aéroport possédant deux pistes de décollage, <u>l'attribution de la piste</u> au pilote n’est pas un choix anodin et là encore <u>très stratégique</u>. En effet, il existe deux façons de choisir la piste. 

### Croisement en l'air 

La première méthode, la plus simple, est d’attribuer **la piste la plus proche de l’avion**. Un départ du doublet nord peut voler vers le sud et croiser un départ doublet sud qui vole vers le nord, d’où le nom “croisement en l’air” 

- Les avions à l’aire Fedex et aux terminaux 1 et 3 iront sur le doublet nord.
- Les avions au terminal 2 et à l’aire cargo iront sur le doublet sud.

Les trafics vont se croiser en vol s'ils ont des départs opposés. Exemple : 
<div style="text-align:center;">
  
![lfpg_croisement_air.png](/doc-atc/croisement_air.png)

</div>

Nous pouvons voir que le départ sur le <span style="color:#5e9bf7;">**doublet sud**</span> va croiser le départ sur le <span style="color:#ea506a;">**doublet nord**</span>.

Cette situation est gérable lorsque **le trafic est faible**. Dans le cas où le trafic s’intensifie, il est convenu d’utiliser la deuxième méthode, dite du croisement au sol.

### Croisement au sol 

Comme son nom l’indique, cette stratégie permet d’éviter le croisement en vol mais de le réaliser au sol. Pour ce faire, tous les avions qui suivent un <span style="color:#ea506a;">**départ vers le nord**</span> partiront du <span style="color:#ea506a;">**doublet nord**</span> et tous les avions qui suivent un <span style="color:#5e9bf7;">**départ vers le sud**</span> partiront du <span style="color:#5e9bf7;">**doublet sud**</span> et ce peu importe le terminal où se trouve l’avion.

Sur le diagramme des départs, la ligne en pointillé rouge sépare les départs nord des départs sud.

### Adaptatif / Sur mesure

Suivant la situation, il peut être pertinent de combiner les deux stratégies précédentes. 
Par exemple, si nous sommes en “croisement en l’air” et que nous avons un group flight qui part vers Amsterdam via NURMO, nous pouvons rester en “croisement en l’air” mais en mettant tous les départs NURMO sur le doublet nord.

Autre exemple, nous sommes en croisement au sol et le doublet nord est très chargé. Nous pouvons coordonner les départs ELCOB (Ouest) sur le doublet sud.

Lors d'événements, nous pouvons coordonner une attribution de piste sur mesure. 

### Letter Of Agreement (LOA)

La DEL est responsable de faire respecter la LoA French vACC-Belux vACC, qui impose des limites verticales au citypairs suivants : 
- Vers EBBR : FL240 max
- Vers EDDF : FL240 max
- Vers EDDK : FL240 max
- Vers EDDL : FL240 max
- Vers EHAM : FL300 max

# Les positions RMP 

Les positions RMP sont responsables des mises en route, repoussages et roulage sur plusieurs aires de stationnement. 

Contrairement à une position GND, la vigie Trafic **ne fournit pas de service de contrôle** à proprement parler. La responsabilité de la séparation au sol retombe sur l’équipage de l’avion. 

Il existe 6 fréquences RMP à Charles de Gaulle : 
- 1 fréquences qui gère les aires I (Fedex)
- 5 fréquences qui gèrent le Terminal 2 ainsi que les stands J au large du taxiway E

> Une attention particulière est à tenir au sens de roulage ([section AD 2 LFPG AD 2.24 de l’AIP, cartes GMC1 et GMC2](https://www.sia.aviation-civile.gouv.fr/)), qui sont à respecter scrupuleusement en la présence d'une position adjacente. Des instructions de roulage qui diffèrent des chemins publiés restent bien évidemment possible, à condition de se coordonner. 
{.is-warning}

l'aéroport est doté de **PAI (Point d'Attente Intermédiaire)** marqués par des traits discontinues sur les cartes. Une phraséologie particulière est à utiliser : 

> "DAL123, taxi via R **stop TE1**"


## La Vigie Fedex

<div style="text-align:center;">
  
![lfpg_fdx](/doc-atc/lfpg_fdx.png)
  
</div>

Les <span style="color:#ED9B3E;">**arrivées entrent via M**</span> et les <span style="color:#387BC7;">**départs sortent via B**</span> dans les deux configurations. 

Les transferts vers et depuis le Sol Nord s’effectuent aux **points d’attentes intermédiaires B et M**. 

## La Vigie Trafic du Terminal 2 : 

### La Vigie Trafic des terminaux 2A, 2C et 2E : 

Cette position est responsable des stands A, C et E. 

<div style="text-align:center;">

![lfpg_t2ace](/doc-atc/lfpg_t2ace.png)
  
</div>

Trois postes capables d'acceuillir l'Airbus A380 sont disponibles : CFE, CFW et CF9. L'entrée et la sortie de cette appareil devra <u>obligatoirement</u> s'effectuer via TA2 et TA3. 


<div style="display:flex; align-items:center; gap:20px;">

<div>

Le taxiway P3 est doté de 2 lignes de couleur supplémentaires : une <span style="color:#ED9B3E;">**ligne orange**</span> et une <span style="color:#387BC7;">**ligne bleue**</span> en plus de la <span style="color:#EDCF15;">**ligne centrale jaune**</span>. Ces deux lignes de couleur permettent de faire rouler simultanément deux avions **d’envergure max 36m**, typiquement deux A320 par exemple. Si un avion lourd type B77W doit rejoindre un stand via P3, il doit obligatoirement utiliser la ligne centrale jaune.  

Avant de les utiliser, <u>demandez aux pilotes s’ils les ont sur leur scène</u>.
  
</div>

<img src="/doc-atc/lfpg_t2_couleur.png" style="width:300px;">

</div>

<div style="clear:right;"></div>

### La Vigie Trafic des terminaux 2B et 2D : 

Cette position est responsable des stands B et D : 

<div style="text-align:center;">
  
![lfpg_t2bd](/doc-atc/lfpg_t2bd.png)
  
</div>

Les taxiway G3 et TB2 sont aussi dotés de lignes <span style="color:#ED9B3E;">**orange**</span> et <span style="color:#387BC7;">**bleue**</span>, et une **interconnexion** existe avec le terminal 2F qui permet de circuler entre les deux sans passer par E. 

Deux points d’attentes intermédiaires séparent les deux terminaux : **G3 EAST** et **G3 WEST**. Les transferts entre les fréquences trafic doivent s’effectuer au plus tard à ces points d’attentes, et tout mouvement via G3 doit **obligatoirement être coordonné** entre les deux contrôleurs. 

> Cette position ne gère par l'aire G, cette dernière est géré par le Sol Sud. 
{.is-info}

### La Vigie Trafic du terminal 2F : 

Cette position est responsable des stands F : 

<div style="text-align:center;">
  
![lfpg_t2f](/doc-atc/lfpg_t2f.png)
  
</div>

Les taxiway G4 est aussi doté de lignes <span style="color:#ED9B3E;">**orange**</span> et <span style="color:#387BC7;">**bleue**</span>, et une **interconnexion** existe avec les terminaux 2B et 2D qui permet de circuler entre les deux sans passer par E. (plus de détails [ici]())

### La Vigie Trafic des satellites K et L : 

<div style="display:flex; align-items:center; gap:20px;">

<div>


Cette position est responsable des stands K et L. Vous verrez presque exclusivement des Wide-Body, et la majorité des stands capables d'accueillir l’A380 se trouvent ici. 

Les taxiways E5 et E6 sont <u>unidirectionnels vers le nord</u>, mais le contrôleur Trafic se verra coordonner des repoussages vers le sud pour réduire la distance de roulage vers le doublet Sud. 
  
Les avions ne peuvent pas circuler entre les voies E5 et E6, les autorisations du type **Swing over** qu'on peut entendre dans d'autres pays sont <u>strictements interdites</u>. 
  
</div>

<img src="/doc-atc/lfpg_t2kl.png" style="width:350px;">

</div>

<div style="clear:right;"></div>


### La Vigie Trafic du Terminal 2J et des stands remote J : 

<div style="display:flex; align-items:center; gap:20px;">

<div>



Cette position est responsable de tous les stands J. **Les arrivées entrent via P5** et **les départs sortent par P4** pour rejoindre E ou G. 

Les stands J14, J16 et J37 sont accessibles depuis le taxiway P5 **sans passer par P4**. 

Les stands J01, J02, et J03 peuvent être sacrifiés pour laisser la place à deux baies de dégivrage  supplémentaire : <span style="color:#ED9B3E;">**J South et J North**</span>.  Les avions peuvent rejoindre les deux baies en sortant du terminal via P4 seulement. 
  
</div>

<img src="/doc-atc/lfpg_t2g.png" style="width:300px;">

</div>

<div style="clear:right;"></div>


# Les positions Sols (GND)

Cette postion est responsable du roulage à l'extérieure des aires de manoeuvres controlées par la Vigie Trafic ainsi que les Terminaux 1 et 3 et les aires de manoeuvres restantes. 

## Le Terminal 1 

Constitué de plusieurs satellites et de Remote Stands, sa gestion est un mélange de repoussage et de départ autonomne. Ces caractéristiques le rendent fortement différent du Terminal 2.

### Les postes du  Terminal 1

Tout les postes du satellite U imposent un repoussage obligatoire. 

Sur les satellites autonomes W, X, Y et Z les postes 1,2 et 6,7 ne nécessitent pas de repoussage. 

Une courte voie de roulage, **Link W**, permet d'accéder aux postes W06/07/08 et X04. 
> Attention, certains postes sont accessibles via A3 et d'autres via A mais pas les deux. 
{.is-warning}

  
Il existe deux sens de roulage et de repoussage sur les voies A3 et A : <span style="color:#fe4d3e;">**RED**</span> et <span style="color:#91ce6b;">**GREEN**</span>. La phraséologie suivante est à utiliser dans cette situation : 

> "DLH123, push and start approuved, **Red/Green push**, QNH1013"

<div style="display:flex; align-items:center; gap:20px;">

<div>

Ce tableau décrit les procédures particulières sur certains postes  : 
 
<table border="1" style="text-align: center;">
    <tr>
        <th>Postes</th>
        <th>Procédures</th>
    </tr>
    <tr>
        <td>U10</td>
      <td>Pas d'entrée via A si <strong>envergure < 36 m </strong></td>
    </tr>
    <tr>
        <td>U16</td>
      <td><span style="color:#fe4d3e;"><strong>Red Push</strong></span>  bloque la voie B</td>
    </tr>
    <tr>
        <td>U17</td>
      <td>Repoussage bloque la voie B dans les deux sens</td>
    </tr>
    <tr>
        <td>W06/07/08 et X04</td>
      <td>Entrée via <strong>Link W</strong>, <span style="color:#91ce6b;"><strong>Green Push</strong></span> obligatoire</td>
    </tr>
    <tr>
        <td>X01, X02</td>
        <td>Sortie <span style="color:#91ce6b;"><strong>Green </strong></span> obligatoire </td>
    </tr>
    <tr>
        <td>X05</td>
        <td> <span style="color:#91ce6b;"><strong>Green Push</strong></span> bloque la voie B</td>
    </tr>
    <tr>
        <td>Z06, Z07</td>
        <td> Sortie autonome <span style="color:#91ce6b;"><strong>Green </strong></span> obligatoire</td>
    </tr> 
</table>

Gardez à l'esprit que nous sommes sur Vatsim, si le pilote ne comprend pas donner la direction cardinal et passer à autre chose. 

  
</div>

<img src="/doc-atc/lfpg_t1.png" style="width:600px;">

</div>

<div style="clear:right;"></div>

### La circulation au Terminal 1
Le terminal 1 est entouré de **7 PAI(TU1 à TU7)** qui délimitent l'aire de manoeuvre et l'aire de trafic. 2 autres PAI, **appellés A1 et A2** délimitent les sevitudes des voies DA1 et B.  

Les PAI TUx sont ausis les **points de transferts silencieux entre les deux sols** (SOL Parking et Sol Taxiway). Une seule position existe sur Vatsim, mais cette situation est vouée à changer, nous vous invitons donc à prendre en compte cette partie pendant l'apprentissage des procédures. 


Les sens de roulages sont identiques au sens de repoussages, mais certaines restrictions sont à connaitre : 

- La voie A3 est limitée à 61 m d'envergure max.
- Les deux virages entre la voie A3 et le pont de la voie A est limitée à 36 m d'envergure max. Si un avion plus large est stationné sur un stand qui impose la sortie via A3 il doit obligatoirement rouler sur l'autre section de la voie A. 
- Le virage entre la sortie DA1 et la voie A est limité à 36 m d'envergure max.


> Attention, certains postes sont accessibles via A3 et d'autres via A mais pas les deux. Il est strictement interdit de circuler entre les satellites pour passer d'un taxiway à l'autre.
{.is-warning}

## Le Cargo Sud 

Constitué de plusieurs batiments et aires de stationnement, nous y retrouverons tout les appareils Cargo autre que Fedex et ASL Belgium. 


Le service RampAgent se chargera de l'assignation des postes en fonction du transporteur. 

Deux PAI se trouvent à l'intersection entre U/C et N : **CARGO1** et **CARGO2**. Ils seront souvent utilisés pour fluidifier les mouvements vers et depuis le Cargo Sud. 

## Le roulage

### Sens de roulage : 

En fonction de la configuration, les sens de roulage sur les voies principales ainsi que les entrées/sorties des aires de manoeuvres changent. Ces sens sont visibles sur [les cartes GMC1 et GMC2](https://www.sia.aviation-civile.gouv.fr/). 

Nous recommandons de respecter strictement ces sens sur les taxiways principaux (E, N, F, R, T, B, Q …) et de vous adapter en fonction du trafic sur le sens des taxiways secondaires. 
 
### A380, B747-8, A124, A225 et C5

Ces avions ne peuvent pas emprunter tous les taxiways de l’aéroport pour des raisons d'envergure et de masse. Ces taxiways interdits sont représentés sur [les cartes GMC_07 et GMC_08](https://www.sia.aviation-civile.gouv.fr/).

[La section Vigie Trafic du Terminal 2](#la-vigie-trafic-du-terminal-2) précise les stands capables d'acceuilir l'A380. 

## Attribution des points d'attentes des pistes :

### Suivant la catégorie : 

Le schéma ci-dessous indique les points d'attente (pour chaque catégorie) pour lesquels il n’est pas nécessaire de demander au pilote sa capacité à décoller depuis ceux-ci : 

<div style="text-align:center;">
  
![lfpg_panord](/doc-atc/lfpg_panord.png)
![lfpg_wtc](/doc-atc/lfpg_wtc.png)
![lfpg_panord](/doc-atc/lfpg_pasud.png)
</div>

### Suivant le trafic : 

Les points d’attente peuvent être attribués en fonction du trafic tout en respectant la catégorie de l’avion.
Dans une situation avec plusieurs avions avec un même départ, il peut être pertinent de les envoyer sur le même point d’attente afin d’optimiser les délais entre les décollages.

<div style="text-align:center;">
  
![lfpg_panord](/doc-atc/lfpg_suivant.png)
  
</div>

L’attribution des points d’attente peut aussi permettre d’éviter les croisements au sol entre deux ou plusieurs avions se dirigeant vers la même piste.

Exemple: 

Afin d’éviter ce croisement, il peut être judicieux de donner T11 au trafic rouge, le tout en passant par P afin d’éviter le croisement. Nous préconisons d’utiliser cette stratégie quand la charge de trafic est très importante.

## Roulage progressif : 

La plateforme étant grande, les instructions de roulage peuvent rapidement devenir compliquées. Pour faciliter la vie du pilote et éviter les erreurs, il est préférable d’utiliser des clairances de roulage progressif, c'est-à-dire des clairances qui ne contiennent que 3 à 4 taxiways maximum. 

Si le pilote semble perdu ou incertain,  ne pas hésiter à le guider pas à pas.

Attention, en anglais, “next right” signifie “deuxième à droite”, et pas “prochaine”. On préférera l’utilisation de “first” ou “second”.

## Dégivrage : 

L’aéroport possède des baies de dégivrage pour dégivrer les avions avant le décollage.
Il y a 4 baies à chaque seuil de piste de décollage, 2 baies dans les aires R et 2 autres dans les aires J.

Les baies de dégivrage sont visibles sur les cartes ADC_01 et ADC_02 ainsi que sur les cartes GMC_04 à GMC_06. Attention, les baies ont un sens !

Lorsqu’un avion demande le dégivrage, nous le ferons rouler jusqu’à la baie la plus proche de sa piste. Dans la réalité, ces baies sont équipées de barres d’arrêt lumineuses devant lesquelles les avions doivent attendre leur tour.

Dans notre cas et étant donné que ces barres d'arrêt ne sont pas modélisées pour tout le monde (voir pas du tout), nous demanderons aux avions d’attendre devant la baie de dégivrage. Dans le cas où il y a la queue, nous les ferons attendre sur le taxi avant les baies de dégivrage. 
Une fois l’avion proche des baies de dégivrage et si sa baie est libre, nous l’autorisons à entrer sur la baie et nous lui demandons de nous rappeler après le dégivrage pour l’autoriser à rouler vers la piste.

Exemple : 
> “EZY123, **request deicing**”
> “EZY123, Taxi to deicing pad NE1 via G3, N and B. **Hold on B before the deicing pad**.”
> …
> “EZY123, **Enter deicing pad NE1**, report ready to taxi.”

## Transfert entre Sol et Vigie : 

Les transferts entre Sol et Vigie s'effecturont aux PAI dans les deux sens. Par exemple, un avion qui souhaite quitter le Terminal 2B devra rouler au PAI TB1. 

Comme précisé dans [la section les positions RMP](#les-positions-rmp), respecter le sens de roulage est très important dans cette situation. 

## Transfert entre Sol Nord et Sol Sud : 

Deux fréquences Sol sont utilisables sur Vatsim : 
- le **Sol Nord** qui gère les terminaux 1 et 3, les stands H ainsi que l'aire Fedex en l'absence de la position Vigie Fedex et toutes les voies de roulage adjacentes. 
- le **Sol Sud** qui gère le reste.  

Les interfaces entre ces deux positions sont les **PAI MIDDLE1/2/3/4**. Les pilotes circulant entre les deux receveront l'instruction de s'y arreter en attente d'instructions de la part du prochain controleur. 

Cependant, nous éviterons autant que possible les transferts tardives pour fluidifier les mouvements.  


> "AFR123, roulez via N **stop MIDDLE1**"

Notez qu'à cause du manque de scène potable, beaucoup de pilotes n'auront pas ces PAI. Il est convenu dans cette situation de faire maintenir la voie principale suivante. Par exemple, si le pilote ne trouve pas MIDDLE1 en remontant N il faut lui demander de maintenir avant A. 

## Transfert entre Sol et Tour : 

A la réception d’un trafic à l’arrivée, la Tour fait traverser la piste intérieure. Pour fluidifier le roulage, la Tour peut lui donner une indication sur le prochain taxiway à suivre : 

Exemple : 

> “AFR654, via S6, traversez piste 08L, après la traversée, à gauche sur R”

# La position Tour (TWR)

Cette position est responsable des mouvements dans la CTR de Paris ainsi que sur les pistes de l'aéroport Charles de Gaulle. 

## Les pistes : 

Les deux doublets de l’aéroport sont indépendants. C'est-à-dire que nous pouvons faire décoller ou atterrir deux avions en même temps, un sur chaque doublet, indépendament de se qui se passe de l'autre coté de l'aéroport.

Sur chaque doublet, les deux pistes sont indépendantes pour des mouvements différents (atterrissage ou décollage), cela veut dire que même si un avion est en courte finale, nous pouvons faire décoller un avion sur l’autre piste du doublet.

La cadence des pistes en fonctionnement normal (atterrissage + décollage) est de 30 à 38 décollages et 30 à 36 atterrissages par heure et par doublet. 

## Alignement des avions 

La clairance d’alignement contient systématiquement la piste **ET** la bretelle utilisée :
> “BCS193, **from T12**, line up runway 26R and wait”.

Nous pouvons aligner jusqu’à deux avions sur une même piste depuis deux bretelles adjacentes (et uniquement s’ils sont sur deux bretelles adjacentes).

Lors de l’instruction d'alignement, nous devons indiquer le numéro dans la séquence. 

> “EZY123, from Q3, line up runway 27L.”
> “AAL987 Heavy,  from Q4, line up runway 27L and wait, **number 2**”

Attention, il n’est pas recommandé d’aligner un 3ème avion devant le 2ème, celà n’est envisageable que si le numéro 2 a un problème et ne peut pas partir immédiatement.

## Décollage 

### Règle Générale 

Réglementairement, l’aéronef n°2 est autorisé au décollage **au plus tôt** lorsque l’aéronef n°1 franchit l’extrémité de piste, ou a amorcé un virage. Dans la quasi-totalité des cas, le respect de cette règle permet de s’assurer qu’il y ait **au moins** 3Nm et/ou 1000’ d’écart à l’envol du n°2.

<u>S’il n’y pas de contrôleur au-dessus de la tour</u>, on va espacer les départs qui vont dans **la même direction** de 2 minutes. Les directions sont Nord, Ouest, Sud et Est.

### Turbulence de sillage 

Le tableau suivant récapitule le délai minimal entre 2 départs successifs de la même piste, en fonction des catégories de turbulence de sillage et des bretelles utilisées. Le décompte commence **dès que le n°1 commence la course au décollage**.

<table style="border-collapse: collapse; width: 100%; table-layout: fixed;">
  <tr>
    <th style="border: 1px solid black; text-align: center;">N°1 \ N°2</th>
    <th style="border: 1px solid black; text-align: center;">J</th>
    <th style="border: 1px solid black; text-align: center;">H</th>
    <th style="border: 1px solid black; text-align: center;">M</th>
    <th style="border: 1px solid black; text-align: center;">L</th>
  </tr>

  <tr>
    <td style="border: 1px solid black; text-align: center;">J</td>
    <td style="border: 1px solid black; text-align: center;">-</td>
    <td style="border: 1px solid black; text-align: center;">2/2</td>
    <td style="border: 1px solid black; text-align: center;">3/4</td>
    <td style="border: 1px solid black; text-align: center;">3/4</td>
  </tr>

  <tr>
    <td style="border: 1px solid black; text-align: center;">H</td>
    <td style="border: 1px solid black; text-align: center;">-</td>
    <td style="border: 1px solid black; text-align: center;">-</td>
    <td style="border: 1px solid black; text-align: center;">2/3</td>
    <td style="border: 1px solid black; text-align: center;">2/3</td>
  </tr>

  <tr>
    <td style="border: 1px solid black; text-align: center;">M</td>
    <td style="border: 1px solid black; text-align: center;">-</td>
    <td style="border: 1px solid black; text-align: center;">-</td>
    <td style="border: 1px solid black; text-align: center;">-</td>
    <td style="border: 1px solid black; text-align: center;">2/3</td>
  </tr>

  <tr>
    <td style="border: 1px solid black; text-align: center;">L</td>
    <td style="border: 1px solid black; text-align: center;">-</td>
    <td style="border: 1px solid black; text-align: center;">-</td>
    <td style="border: 1px solid black; text-align: center;">-</td>
    <td style="border: 1px solid black; text-align: center;">2/3</td>
  </tr>

  <tr>
    <td colspan="5" style="border: 1px solid black; text-align: center; padding:10px;">
      Chiffres exprimés en minutes<br>
      Format : délai depuis la même bretelle ou en amont / délai depuis une bretelle en aval<br>
      Case vide = appliquer la règle générale
    </td>
  </tr>
</table>

### Performance : 

Si l’aéronef n°2 est plus rapide que le n°1 (de façon significative), appliquer un délai minimum de 2 minutes.

**Exemples :** 777 derrière A340, A321 derrière A318, A320 derrière BAe146/Avro Jet.

Il n’y a pas de liste exhaustive de cas particuliers, seule votre expérience vous permettra d’estimer la pertinence d’une telle majoration.

### SIDs et interdépendance des doublets

Au départ d’une même piste, le respect de la règle générale ainsi que le panachage des SIDs garantit normalement un séquencement adéquat pour le secteur DEP.

Dans le cas particulier d’une séquence soutenue de départs sur une même SID (événement réseau, vol de groupe), cette règle de base peut ne pas suffire. Dans ce cas, il convient d’espacer les départs afin de faciliter le travail du DEP, en coordination avec ce dernier : par exemple, augmenter temporairement la cadence à 1’30 voire 2’ entre 2 départs successifs sur la même SID.

Ponctuellement ou en operation [Croisement en l'air](#configuration-de-roulage), des départs peuvent être amenés sur 2 pistes différentes et prévus soit sur la même SID, soit sur 2 SIDs qui se croisent :

Quelle que soit la situation, en cas de SIDs interférant au départ des 2 doublets :

- si l’avion n°1 est au départ de la 27L ou de la 08L, alors respectivement, on peut autoriser le n°2 à décoller de la 26R ou de la 09R **lorsque le n°1 passe l’extrémité de sa piste de décollage**

- Si l'avion n°1 est au départ de la 09R ou de la 26R, alors respectivement, on peut autoriser le n°2 à décoller de la 08L ou de la 27L **lorsque le n°1 passe 2Nm après l’extrémité de sa piste de décollage.**

Si le délai n’a pas pu être respecté, **prévenir impérativement le DEP**, qui pourra décider des mesures de précaution (stopper l’un des 2 à un FL inférieur par exemple) afin d’aider à effectuer le croisement. Cette situation doit rester exceptionnelle car elle augmente considérablement la complexité du travail du secteur suivant.

<u>S’il n’y pas de contrôleur au-dessus de la tour</u>, il convient d’espacer les départs croisés de minimum 3 minutes.

### Départ omnidirectionnel 

À LFPG, des départs omnidirectionnels sont possibles de jour à l'usage des aéronefs à hélices avec accord de l’approche/départ. Ces départs libèrent l'axe de piste plus rapidement et font accélérer l'aéronef vers une vitesse en palier plus compatible avec la vitesse de montée d'un réacteur. Il est ainsi possible de laisser partir le n°2 sans attendre aussi longtemps que si le n°1 restait sur la trajectoire publiée.

Dès que nécessaire, la tour coordonne le départ et le cap avec l’approche/départ et donne la clairance modifiée à l'avion ou la fait donner par le sol s'il est encore au roulage.

Sur le doublet Nord :
- A 800 ft, virage vers le Nord en montée initiale à 3000 pieds.
Sur le doublet Sud :
- A 800 ft, virage vers le Sud en montée initiale à 3000 pieds.

Attention à la pertinence de l'utilisation de cette technique : donner un cap 330 à un ATR au départ 27L vers OPALE suivi d'un A320 vers RANUX engendrera un nouveau croisement peu après l'envol. De même, donner un cap 330 à un appareil hélice en sortie LGL n'est pas idéal en termes de qualité de service rendu. 

Enfin, cette procédure est à utiliser avec précaution au départ du doublet Sud du fait de la proximité de la P23 (Paris), du Bourget, et des espaces et trajectoires d'Orly. 
Dans tous les cas, **ne pas donner de départ omnidirectionnel s'il n'y a pas de secteur DEP ou APP disponible pour assurer le guidage radar.**

## Atterrissage 

À LFPG, les **clairances d'atterrissages anticipées** nous permettent d'autoriser 4 avions à atterrir sur la meme piste et <u>une phraséologie particulière</u> est à utiliser. 

Il faut indiquer le **numéro dans la séquence** et **la distance avec le précédent** à l’atterrissage. <u>Au-delà du numéro 4</u>, nous demanderons à l’avion de poursuivre l’approche jusqu’à ce que le numéro 1 ait dégagé la piste.

> “EZY123, **number 1**, wind 250 degrees 12 knots, runway 27R, clear to land.”
> “AAL456, **number 2, 6 Nautical miles behind an Airbus 320**, wind 250 degrees 12 knots, runway 27R, clear to land.”
> “AFR987, **numéro 3, 7 nautique derrière un Boeing 777**, vent 250 degré 12 noeuds, autorisé atterrissage piste 27R”

## Remise de gaz 

Les remises de gaz publiées font monter l’avion dans l’axe à l’altitude d’interception de l’ILS.
- 4000 ft pour les pistes 26L et 09L
- 5000 ft pour les pistes 27R et 08R

Il est possible de <u>coordonner un cap</u> pour dégager rapidement l’axe de piste en cas de conflit avec les départs.

Il faut donc **s’assurer de la séparation** entre le départ et la remise de gaz en : 

- Arrêtant le décollage s’il n’a pas commencé à rouler.
- Limitant la montée du départ sous l’altitude de la remise de gaz (et au-dessus de 1500ft).
- Donnant un cap à la remise de gaz si possible.

> Il est essentiel d'intervenir <u>avant de transférer l'avion</u> à la prochaine fréquence, il ne faut pas envoyer une patate chaude et encore moins sans prévenir. 
{.is-warning}

Le transfert de l’avion se fait par défault au départ, mais on va essayer dans la mesure du possible de **coordonner un transfert à l'ITM** (approche finale) directement. 

## VFR

[La CTR de Paris](https://www.sia.aviation-civile.gouv.fr/media/dvd/eAIP_19_FEB_2026/Atlas-VAC/PDF_AIPparSSection/VAC/AD/AD-2.LFPG.pdf) est une CTR de classe D. C'est-à-dire que le VFR est possible mais sur autorisation. Cependant, la CTR de Paris se trouve dans une zone R (la zone R275) qui interdit le VFR <u>sauf pour les hélicoptères</u>. 

Au dessus de la CTR, la TMA de Paris est en classe A et donc <u>interdit strictement le VFR</u>.

Pour gérer au mieux les hélicoptères venant sur la plateforme, nous vous invitons à lire la carte AD-3 de Paris Charles De Gaulle.

## Transfert aux DEPs 

Le DEP s’occupe de gérer les avions qui décollent de LFPG.

- Le <span style="color:#ea506a;">**DEP Nord**</span> s’occupe des avions qui <span style="color:#ea506a;">**partent vers le nord**</span>, <u>peu importe la piste de décollage</u>. 
- Le <span style="color:#5e9bf7;">**DEP Sud**</span> s’occupe des avions qui <span style="color:#5e9bf7;">**partent vers le sud**</span>, <u>peu importe la piste de décollage</u>. 

# Dégroupage 

Sur VATSIM, il est convenu de dégrouper les positions comme suit : 

- LFPG_DEL
- LFPG_RMP en 5 fréquences différentes
- LFPG_GND en LFPG_GND (Nord) + LFPG_S_GND (Sud) + LFPG_RMP (Trafic) + LFPG_FDX_RMP (vigie Fedex)
- LFPG_TWR en LFPG_TWR (Nord) + LFPG_S_TWR (Sud)

Dans certains cas et <u>avec accord des autres contrôleurs et du coordinateur s'il y en a un</u>, LFPG_DEL et LFPG_RMP peuvent **fusionner**. Dans ce cas, la position sera LFPG_DEL mais gérera le rôle de LFPG_RMP en plus du sien.

## Diagramme de dégroupage 

## Ordre de dégroupage

Le diagramme ci-dessus se lit de la manière suivante  : 
- Pour ouvrir LFPG_S_GND, il est nécessaire que LFPG_GND et LFPG_DEL soient connectés.
- Pour ouvrir la vigie Fedex, il est nécessaire que LFPG_DEL et LFPG_GND soient connectés. 
- Pour ouvrir la tour Sud, il est nécessaire que LFPG_GND et LFPG_TWR soient connectés


# Procédures Low Visibility (LVP)

## Conditions 

- Plafond suppérieur ou égal à 200ft;  
- ou RVR supérieur ou égale à 600m

## Position GND

Pour permettre la protection et l'intégrité du signal ILS, aucun avion ne doit pénétrer dans l'**ILS Critical Area** pendant l'approche d'un autre avion. Cette zone est protegée par **les points d'attentes CATIII**. 

Ils sont visibles sur [la carte ADC_02](https://www.sia.aviation-civile.gouv.fr/media/dvd/eAIP_19_FEB_2026/FRANCE/AIRAC-2026-02-19/html/eAIP/Cartes/LFPG/AD_2_LFPG_ADC_02.pdf). Nous spécifions que le point d’attente est un CAT III dans l’instruction donnée au pilote.

> "AFR123, roulez **point d'attente CATIII** piste 08L via N et T3"

## Position TWR

Les procédures suivantes sont à appliquer : 

- Lorsqu’un avion est à 2 Nm de la piste d'atterrissage, il ne faut qu’aucun avion ne survole l’antenne LOC jusqu’à ce que l’avion soit au sol.
- Les clairances d'atterrissages anticipées sont <u>interdites</u>. 
- L'approche espacera les arrivées de <u>150 à 180 secondes</u>.

# Spécificités 
## Concorde 

Concorde aura la priorité au roulage vers le décollage uniquement et au décollage. Il doit passer le moins de temps possible à l'arrêt et au roulage. 

Concorde sera généralement garé au terminal 2A (historiquement, porte A12 et A20). 

## POGO
Un POGO désigne un vol IFR de très courte distance **entre deux aéroports voisins** situés dans la même région de contrôle. 

Pour LFPG, il existe un itinéraire POGO avec LFPO. Nous vous invitons à lire les cartes SID POGO. 

La mise en route sur un cette itinéraire nécessite une **autorisation explicite** de la part des radaristes de LFPG et LFPO. <u>Il n'y a pas de délégation de mise en route vers Orly</u>. 

