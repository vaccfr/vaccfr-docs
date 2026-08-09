---
title: Configuration et utilisation du PDC
description: 
published: true
date: 2026-07-19T19:37:25.752Z
tags: 
editor: markdown
dateCreated: 2026-02-28T22:27:37.637Z
---

![banner_tools_fr.png](/banners/banner_tools_fr.png)
# Introduction
Depuis 2016 en France, les équipages ont la possibilité d’utiliser les communications dites par “data-link” dans l’espace aérien français. Il s’agit d’une technologie de communication air-sol qui permet de fournir différents services. Parmi ces services, on peut citer le CPDLC mais aussi le PDC.
Dans ce document, nous allons nous intéresser à **l’utilisation du service PDC** (Pre Departure Clearance) en position prévol pour délivrer des clairances de mise en route par data-link.

# Qu’est-ce que le PDC ?


Le service PDC (Pre Departure Clearance) est simplement la version informatisée d’une clairance de mise en route IFR. Au lieu de la recevoir en voix sur la fréquence prévol, l’équipage la reçoit directement dans le cockpit, par l’intermédiaire de son système data-link. L’équipage devra ensuite accuser réception de la clairance directement depuis le cockpit.

Ce système offre l’avantage de réduire le temps d’occupation de la fréquence et est aujourd’hui massivement utilisé sur des aéroports majeurs, partout dans le monde.


![pdc_onboard.png](/pdc_onboard.png){.align-center}

# Comment activer le PDC sur VATSIM ?

## Demander ses identifiants HOPPIE

**HOPPIE** est le service utilisé pour simuler les communications par data-link sur VATSIM. HOPPIE n’étant pas directement lié au réseau, une création de compte est nécessaire. Vous pouvez créer un compte <a href="https://www.hoppie.nl/acars/system/register.html" target="_blank">ici</a>.

## Configurer Euroscope


1. Initialiser le PDC :
Dans la barre de commande d’Euroscope, exécutez la commande suivante : .smr

Cette fenêtre s'affiche alors sur votre écran : 

![init_pdc.png](/init_pdc.png){.align-center}

Note : Vous pouvez cocher la case “Play sound on clearance request” pour recevoir une notification sonore lors de la réception d’une demande PDC.

>Remarque : VATSIM n’est pas le seul réseau à utiliser HOPPIE, il est possible qu’une personne hors VATSIM utilise le même Logon Code que vous, bloquant votre connexion. Dans cette situation, changez de Logon Code en ajoutant un X à la place de la dernière lettre, par exemple: **LFMX** ou **LFPX**  {.is-warning}

2. Connecter le PDC 
Une fois les champs demandés remplis, validez en cliquant OK puis exécutez la commande suivante : `.smr connect` 
Un message vous confirme alors la réussite de la connexion au système.

![pdc_logged_in.png](/pdc_logged_in.png){.align-center}

Note : Cette commande est nécessaire à chaque ouverture d’Euroscope, sans celle-ci, vous ne recevrez pas les demandes faites par les pilotes.

3. Indiquer aux pilotes :
Afin d’informer les pilotes que l’utilisation du PDC est possible et pour leur transmettre le Logon code, il est nécessaire d’ajouter la mention **“PDC Available LF**”** dans les ATIS INFO lines (fenêtre de connexion Euroscope).

Note : Ne pas oublier de supprimer cette mention si vous n’activez pas le PDC.


# Comment utiliser le PDC

## Réception d’une demande PDC

Lors de la réception d’une demande de mise en route PDC, La lettre  **<span style="color:gold"> R </span>** clignote dans la case PDC de la Departure List :

![pdc_r.png](/pdc_r.png){.align-center}

## Réponse à une demande

our répondre à cette demande, effectuez un clic droit sur le **<span style="color:gold"> R </span>**, pour afficher le menu des réponses possibles. Pour envoyer la clairance, sélectionnez `Confirm` 

![answer_menu_pdc.png](/answer_menu_pdc.png)

Vérifiez que les informations de la clairance correspondent aux procédures actives :
- RWY
- DEPARTURE
- INIT CLB
- SSR
- NEXT FREQ (GND or Higher)
- Puis cliquez SEND

Si vous êtes trop chargé, vous pouvez faire patienter un trafic en appuyant sur `Standby`.
  
Si pour une raison ou une autre vous ne pouvez pas lui envoyer d’autorisation PDC, appuyer sur `Voice`. Le pilote reçoit alors un message lui demandant de vous contacter via la radio.

![pdc_flightplan.png](/pdc_flightplan.png){.align-center}

## Confirmation de réception

Après avoir répondu à la demande, un **<span style="color:gold"> V </span>** s’affichera, ce qui signifie que l’autorisation de mise en route à été envoyée mais le pilote n’a pas encore validé la réception de celle-ci.

![pending_validation.png](/pending_validation.png){.align-center}

Lorsque le pilote accuse réception de la clairance, un **<span style="color:green"> V </span>** apparaît et sert de relecture. 

![validation_pdc.png](/validation_pdc.png){.align-center}

Il ne reste plus qu’à attendre que le trafic vous contacte pour le repoussage et la mise en route. 

