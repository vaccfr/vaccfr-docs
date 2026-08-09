---
title: Les situations d'urgence et leur gestion
description: Les situations d'urgence et leur gestion
published: true
date: 2026-07-18T19:24:25.689Z
tags: 
editor: markdown
dateCreated: 2026-07-18T19:24:23.640Z
---

![doc_banner_atc_fr.png](/banners/doc_banner_atc_fr.png)
# Introduction
Le but de ce document est de vous apporter une aide à la gestion de situations d’urgence et de détresse. De par leur caractère peu banal, y faire face sans y être préparé (même sur VATSIM) peut sembler un peu déroutant.

Lorsque l’on parle de gestion des “urgences”, il est bon d’établir la différence entre situation d’urgence et situation de détresse : 

- **L’urgence** : l’intégrité de l’avion, la sécurité à son bord ou celle d’une personne à bord est menacée.

- **La détresse** : danger grave ou imminent à bord **ET** des vies humaines en danger.

> Dès lors que le pilote s’est déclaré en situation d’urgence ou de détresse, il devient prioritaire par rapport aux autres. Il est important que la trajectoire donnée au pilote en péril soit optimale : en termes de temps mais aussi pour éviter les éventuels obstacles de l’environnement (reliefs ou autres aéronefs). {.is-warning}

**RAPPEL : Paragraphe B6, Code of Conduct**

“B6 - No flight may declare itself to have priority over another. Pilots are permitted to declare in-flight emergencies only when under air traffic control. <u> If, for any reason, air traffic control requests the pilot to terminate the emergency, then the pilot must do so IMMEDIATELY or disconnect from the network.</u> Pilots are not permitted to simulate any unlawful act including, but not limited to, declaring a hijack by any method, including entering a transponder code of 7500.”

# L'urgence

Un aéronef est en situation d’urgence lorsque l’intégrité de l’avion, la sécurité à son bord ou celle d’une personne à bord est menacée. Pour signaler cette situation au service de contrôle, le pilote procède comme suit : 


> **PAN PAN PAN** (à prononcer comme le mot français “PANNE”) - **Indicatif du vol** (numéro ou immatriculation) **- Brève description du problème - Position - Intentions du commandant de bord.**


Le pilote annoncera généralement sa situation sur la fréquence de contrôle en cas de vol contrôlé. Si le pilote est en vol non contrôlé, il peut utiliser la fréquence GUARD (121.500) pour déclarer son urgence.

Remarque : La fréquence GUARD ne doit pas être utilisée sur VATSIM. Par exemple, si vous survolez Paris et que vous êtes sous le contrôle de LFFF_CTR, déclarez votre urgence directement au contrôleur en fréquence.

# La détresse
Un aéronef est en situation de détresse lorsqu’il est en proie à un danger grave ou imminent **ET** que des vies humaines sont en danger. Pour signaler cette situation au service de contrôle, le pilote procède comme suit : 

> **MAYDAY MAYDAY MAYDAY - Indicatif du vol** (numéro ou immatriculation) - **Brève description du problème - Position - Intentions du commandant de bord.**


C’est incontestablement le message le plus connu de tous. Sa première utilisation remonte à il y a un peu plus de 100 ans. Un pilote français  traversant la Manche pour se rendre en Angleterre s’est retrouvé en difficulté et a prononcé «venez m’aider» en radio. Son message a été reçu par un opérateur anglais qui l’a compris comme «mayday». Ainsi, c’est quelques années plus tard, en 1929, que le mot “mayday” est devenu le message de détresse officiel.


Par définition, un avion ayant déclaré un mayday est en danger grave ou imminent et doit donc regagner le sol au plus vite. Dans le cas où vous souhaitez gérer l’urgence sur VATSIM, demandez les intentions du pilote s’il ne vous les a pas déjà données : en particulier le terrain sur lequel il souhaite se poser et la nature de l’urgence à minima. 
Une fois l’aéroport de déroutement connu, il faut dégager la piste jusqu'à ce que l’aéronef en situation d’urgence soit posé. Ainsi, aucun décollage ni atterrissage ne peut être autorisé sur le dit terrain.


# Quelques manoeuvres d’urgence

## Les descentes d’urgence

En cas d’avarie ou de situation grave arrivant lorsque l’appareil est en croisière, l’équipage peut décider d’effectuer une descente d’urgence. Elle peut notamment être engagée dans les cas suivants (la liste est non exhaustive) : 

- une dépressurisation de la cabine
- une urgence médicale (dans le cas d’un aéroport de déroutement proche)

L’équipage enclenchera une descente avec un vario d’environ 4000 à 4500 pieds/minute pour rejoindre le FL100 le plus rapidement possible. C’est un niveau pris pour référence car l’air y est encore respirable. Ainsi dans le cas d’une dépressurisation, les masques à oxygène ne seront plus utiles à cette altitude. 




Dans le cas d’une descente d’urgence, utiliser la méthode **ASSIST** :

![assist.png](/assist.png)

Nb : Cette méthode est transposable à tout autre type d’urgence. Gardez-la précieusement.

## Les actions TCAS

Pour rappel, TCAS désigne le Traffic Collision Avoidance System, de l’anglais Système d’alerte de trafic et d’évitement des collisions en vol. C’est un système rendu obligatoire depuis 2003 sur les avions pouvant transporter plus de 19 passagers ou ceux qui vérifient une MTOW (Maximum Takeoff Weight) > 7500 kg.

Le TCAS propose deux types d’alertes, un “avis de trafic” (**T**raffic **A**dvisory) et un “avis de résolution” (**R**esolution **A**dvisory) :

1) **TCAS Advisory (TA)** :

	Indication donnée à l'équipage indiquant qu'un autre aéronef constitue une menace potentielle.

2) **Resolution Advisory (RA)** :

	Indication donnée à l'équipage recommandant :

	- Une manœuvre destinée à assurer la séparation de toutes les menaces 
	- Une restriction de manœuvre destinée à maintenir la séparation existante

En cas de Resolution Advisory, le contrôleur doit laisser le pilote entreprendre la manœuvre d’évitement. Si tel est le cas, le pilote pourrait prévenir le contrôleur de la manière suivante :

AFR001, resolution advisory, descending now FL220.

Nb : Il est aussi important de noter que sur VATSIM les indications données par le TCAS peuvent être légèrement erronées (en fonction de l’Add-on utilisé, etc…).




