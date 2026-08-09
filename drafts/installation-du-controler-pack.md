---
title: Installation du Controller Pack
description: 
published: false
date: 2026-07-19T14:14:35.372Z
tags: 
editor: markdown
dateCreated: 2026-07-19T14:11:43.831Z
---

# Installation du Controller Pack

Ce guide vous accompagne pas à pas dans l'installation et la configuration des outils nécessaires pour contrôler au sein de la French vACC.

À la fin de ce guide, vous disposerez de :

- EuroScope installé et configuré.
- Du Controller Pack de la French vACC.
- Des derniers `NavData-Packages` des FIR françaises.
- De TrackAudio configuré pour les communications vocales.
- D'un environnement de contrôle entièrement opérationnel, prêt pour l'observation ou le contrôle sur VATSIM.

# EuroScope

**EuroScope** est le client radar utilisé par les contrôleurs sur VATSIM. Il fournit l'ensemble des outils nécessaires à la gestion du trafic aérien : affichage radar, étiquettes de vol, listes de trafic et fonctions de contrôle.

Le **Controller Pack** de la French vACC complète EuroScope en y ajoutant les profils, affichages radar, plugins et paramètres nécessaires pour reproduire l'environnement de contrôle français.

![euroscope_radar_client.png](/euroscope_radar_client.png)

## Prérequis

Avant d'installer EuroScope, vérifiez que votre ordinateur répond aux prérequis suivants :

- **Système d'exploitation :** Windows XP, Vista, 7, 10 ou 11 (Windows 11 64 bits recommandé).
- **Microsoft .NET :** dernière version du [.NET Framework](https://dotnet.microsoft.com/fr-fr/download).
- **Composants additionnels :** les dépendances nécessaires seront installées automatiquement par l'installateur d'EuroScope.

## Installation d'EuroScope

> La French vACC utilise actuellement **EuroScope 3.2.9**. Bien que des versions plus récentes existent, il s'agit de la version officiellement compatible avec le Controller Pack.
{.is-success}

1. Téléchargez [l'installateur **EuroScope 3.2.9**](https://euroscope.hu/install/EuroScopeSetup.3.2.9.msi).
2. Lancez l'installation.
3. Lorsque le dossier d'installation est demandé, utilisez le répertoire suivant : `C:\Program Files (x86)\EuroScope`

![/euroscope_install.png](/euroscope_install.png)

Nous recommandons d'utiliser le répertoire d'installation par défaut. La majorité des outils développés par la communauté supposent qu'EuroScope est installé à cet emplacement.

## Désactiver le chargement automatique des profils

Avant d'installer le Controller Pack, vous devez désactiver le chargement automatique des profils dans EuroScope.

Si cette option reste activée, EuroScope rouvrira systématiquement le dernier profil utilisé au lieu de vous demander quel profil charger. Les profils du Controller Pack ne pourront alors pas être utilisés correctement.

1. Lancez **EuroScope**.
2. Cliquez sur **OTHER SET**.
3. Décochez **Auto load last profile on startup**.
4. Fermez puis relancez EuroScope.

![euroscope_disable_auto_load_last_prf.png](/euroscope_disable_auto_load_last_prf.png)

Au prochain démarrage, EuroScope vous demandera de sélectionner un **profil** (`.prf`).

Un profil contient tous les éléments nécessaires à un environnement de contrôle donné :

- les affichages radar ;
- les plugins ;
- les paramètres ;
- la configuration propre à une FIR ou à une position de contrôle.

Par exemple :

- **CoFrance LFBB.prf**
- **CoFrance LFMM.prf**
- **EGA Paris.prf**
- **CCA Toulouse.prf**

# Télécharger le Controller Pack

Votre installation d'EuroScope est maintenant prête. L'étape suivante consiste à installer le **Controller Pack** de la French vACC.

Le Controller Pack constitue le cœur de votre environnement de contrôle. Il complète EuroScope en y ajoutant tous les éléments nécessaires pour observer ou contrôler sur le réseau VATSIM, notamment :

- les profils contrôleur (`.prf`) ;
- les affichages radar (`.asr`) ;
- les fichiers de configuration ;
- les plugins.

Le Controller Pack ne contient cependant **aucune donnée de navigation**. Chaque FIR publie son propre **package NavData**, qui doit être téléchargé séparément puis installé avec le Controller Pack.

## Télécharger le Controller Pack Installer

Téléchargez la dernière version du **Controller Pack Installer** depuis la page [**Releases** du repo GitHub](https://github.com/vaccfr/Sector-Files/releases).

Le Controller Pack Installer permet d'installer, de mettre à jour et de maintenir votre environnement de contrôle. Il installe automatiquement le Controller Pack ainsi que les `NavData-Packages` dans la bonne arborescence et peut également configurer vos profils EuroScope avec vos identifiants VATSIM.

## Télécharger les packages NavData

En complément du Controller Pack, vous devrez télécharger le **package NavData** correspondant à chaque FIR sur laquelle vous souhaitez contrôler.

Les derniers packages sont disponibles sur **AeroNav GNG** :

- [**LFBB – Bordeaux**](https://files.aero-nav.com/LFBB)
- [**LFFF + LFEE – Paris + Reims**](https://files.aero-nav.com/LFXXN)
- [**LFMM – Marseille**](https://files.aero-nav.com/LFMM)
- [**LFRR – Brest**](https://files.aero-nav.com/LFRR)

> Les packages NavData contiennent uniquement les données de navigation propres à chaque FIR.
>
> Ils doivent impérativement être installés à l'aide du **Controller Pack Installer**. Ne les décompressez pas et ne les copiez jamais manuellement dans votre installation.
{.is-warning}

# Installer le Controller Pack

Une fois le **Controller Pack Installer** et les **packages NavData** téléchargés, vous êtes prêt à installer votre environnement de contrôle.

Lancez le **Controller Pack Installer**, puis ouvrez l'onglet **Install**.

## Installation

Pour effectuer une première installation :

1. Sélectionnez le dossier dans lequel le Controller Pack sera installé.
2. Ajoutez les packages NavData requis en les faisant glisser dans la fenêtre ou en cliquant sur **Add Files**.
3. Cliquez sur **Install / Update**.

> N'installez jamais le Controller Pack dans le dossier d'installation d'EuroScope.
>
> Nous vous recommandons de l'installer dans un dossier distinct, par exemple :
>
> `C:\French vACC\Controller Pack`
{.is-warning}

![controller_pack_installer_install.png](/controller_pack_installer_install.png)

Avant de lancer l'installation, le programme affiche un récapitulatif des fichiers qui seront installés ou mis à jour, ainsi que la méthode utilisée pour sauvegarder votre configuration actuelle.

Prenez le temps de vérifier ces informations avant de poursuivre.

Une fois l'installation terminée, votre Controller Pack est prêt à être utilisé.

## Configurer vos profils

L'onglet **Profile** permet de renseigner automatiquement vos informations dans tous les profils fournis avec le Controller Pack.

Il vous suffit de saisir vos informations une seule fois pour que l'ensemble des fichiers `.prf` soit configuré automatiquement.

Vous pouvez renseigner les informations suivantes :

- Nom du contrôleur
- CID VATSIM
- Mot de passe VATSIM
- Rating contrôleur
- Activation de Discord Rich Presence

![controller_pack_installer_profile_configurator.png](/controller_pack_installer_profile_configurator.png)

Ces informations sont conservées lors des prochaines mises à jour du Controller Pack. Cette opération n'est donc nécessaire qu'une seule fois.

# Maintenir le Controller Pack à jour

La French vACC publie régulièrement des mises à jour du Controller Pack afin d'intégrer les nouveaux cycles AIRAC, les évolutions des plugins et les corrections de bugs.

On distingue deux types de mises à jour :

- les **mises à jour AIRAC**, publiées tous les 28 jours ;
- les **mises à jour du Controller Pack**, publiées ponctuellement entre deux cycles AIRAC.

## Mises à jour AIRAC

À chaque nouveau cycle AIRAC, vous devrez mettre à jour le Controller Pack ainsi que les packages NavData des FIR que vous utilisez.

La procédure est identique à une première installation :

1. Lancez le **Controller Pack Installer**.
2. Sélectionnez votre dossier d'installation du Controller Pack.
3. Ajoutez les derniers packages NavData.
4. Cliquez sur **Install / Update**.

Votre configuration est conservée autant que possible durant la mise à jour.

## Mises à jour du Controller Pack

Entre deux cycles AIRAC, la French vACC peut publier des mises à jour du Controller Pack.

Ces mises à jour peuvent contenir :

- des corrections de bugs ;
- des mises à jour des plugins ;
- des améliorations des affichages radar ;
- des modifications de configuration.

Dans ce cas, aucun nouveau package NavData n'est nécessaire.

Il suffit de :

1. lancer le **Controller Pack Installer** ;
2. sélectionner votre installation existante ;
3. cliquer sur **Install / Update**.

## Avant de lancer EuroScope

Avant de poursuivre, vérifiez que vous avez bien réalisé les étapes suivantes :

- ✓ EuroScope est installé.
- ✓ Le chargement automatique des profils est désactivé.
- ✓ Le Controller Pack est installé.
- ✓ Les packages NavData nécessaires sont installés.
- ✓ Vos informations contrôleur ont été configurées.

Si tout est prêt, vous pouvez lancer EuroScope pour la première fois.

# Lancer EuroScope

Vous êtes maintenant prêt à lancer EuroScope avec le Controller Pack de la French vACC.

Au démarrage, EuroScope vous demandera de sélectionner un **profil** (`.prf`). Ce comportement est normal : il résulte de la désactivation du chargement automatique des profils effectuée précédemment.

Un profil définit l'environnement de contrôle qui sera chargé dans EuroScope. Il détermine notamment :

- les affichages radar ;
- les cartes ;
- les plugins ;
- les paramètres associés à une FIR ou à une position de contrôle.

Ouvrez le dossier dans lequel vous avez installé le Controller Pack, puis sélectionnez le profil correspondant à la FIR et à la position que vous souhaitez observer ou contrôler.

Par exemple :

- **CoFrance LFBB.prf** — FIR Bordeaux
- **CoFrance LFMM.prf** — FIR Marseille
- **EGA Paris.prf** — Positions d'approche, tour, sol et clairance de Paris-CDG
- **CCA Nice.prf** — Positions d'approche, tour, sol et clairance de Nice

![euroscope_profile_prompt.png](/euroscope_profile_prompt.png)

Une fois le profil chargé, EuroScope ouvre automatiquement l'environnement correspondant à la position sélectionnée.

> Lors du premier lancement, CoFrance peut afficher un message indiquant qu'un fichier **.toml** est introuvable.
>
> Ce comportement est normal. Le fichier est créé automatiquement lors du premier démarrage et ce message ne devrait plus apparaître par la suite.
{.is-info}

## Vérifier votre installation

Si l'installation s'est déroulée correctement, vous devriez constater que :

- le bon affichage radar est chargé ;
- le plugin **CoFrance** est actif ;
- les affichages radar et les AVISOs sont disponibles dans le menu **Recent Files** ;
- aucun fichier n'est signalé comme manquant (à l'exception du message concernant le fichier `.toml` lors du premier lancement).

Si ce n'est pas le cas, vérifiez que :

- le Controller Pack est installé dans un dossier distinct d'EuroScope ;
- les packages NavData correspondant aux FIR souhaitées sont bien installés ;
- vous avez sélectionné le bon profil (`.prf`) au démarrage d'EuroScope.

# CoFrance

**CoFrance** est le principal plugin inclus dans le Controller Pack de la French vACC. Il enrichit EuroScope en proposant des outils avancés, des automatisations et des fonctionnalités spécialement conçus pour reproduire les méthodes de contrôle utilisées dans l'espace aérien français.

Vous entendrez souvent les contrôleurs parler du **« CoFrance Pack »**.

Cette expression désigne simplement l'environnement de contrôle fourni par la French vACC, qui regroupe CoFrance, les profils EuroScope, les affichages radar, les cartes, les plugins et les fichiers de configuration.

CoFrance est développé par la French vACC afin de reproduire, aussi fidèlement que possible, les méthodes de travail utilisées par les contrôleurs français.

Le Controller Pack est entièrement fonctionnel dès son installation. Toutefois, CoFrance propose de nombreuses fonctionnalités avancées que vous découvrirez au fil de votre progression.

Nous vous recommandons vivement de consulter le manuel utilisateur afin de tirer pleinement parti du plugin.

Le manuel utilisateur de CoFrance est disponible depuis le [GitHub](https://github.com/vaccfr/CoFrance-v2/blob/main/CoFranceUserManual.pdf).

![user_manual_thumb.png](/user_manual_thumb.png){.align-center}

# Installer TrackAudio

**TrackAudio** est le client vocal recommandé pour VATSIM. Il permet de communiquer avec les pilotes et les autres contrôleurs pendant vos sessions.

> EuroScope ne dispose pas d'un client vocal intégré. L'installation de TrackAudio est donc indispensable pour utiliser les communications vocales sur VATSIM.
{.is-info}

> **Audio for VATSIM** est progressivement abandonné. La French vACC recommande désormais l'utilisation de **TrackAudio**.
{.is-warning}

## Télécharger et installer

Téléchargez la dernière version de **TrackAudio** depuis la page **Releases** du projet sur GitHub.

Lancez ensuite l'installateur puis ouvrez TrackAudio une fois l'installation terminée.

![track_audio_1.png](/track_audio_1.png){.align-center}

## Configurer TrackAudio

Cliquez sur **Settings** (l'icône en forme d'engrenage) pour ouvrir la fenêtre de configuration.

Renseignez ensuite vos identifiants VATSIM :

- CID
- Mot de passe

![track_audio_2.png](/track_audio_2.png){.align-center}

Sélectionnez ensuite les périphériques audio que vous souhaitez utiliser :

- votre microphone ;
- votre casque ou vos haut-parleurs.

Nous recommandons l'utilisation d'un microphone de bonne qualité afin de garantir des communications claires et intelligibles.

![track_audio_3.png](/track_audio_3.png){.align-center}

## Activer les effets radio

Activez l'option **VHF Radio Effects** afin de reproduire le son caractéristique des communications radio VHF.

![track_audio_4.png](/track_audio_4.png){.align-center}

## Configurer le Push-to-Talk

Choisissez la touche qui servira de **Push-to-Talk (PTT)**.

Pour l'option **Audio Rendering**, nous recommandons le profil **Rockwell Collins**, mais vous pouvez naturellement choisir celui qui vous convient le mieux.

![track_audio_5.png](/track_audio_5.png){.align-center}

Veillez à sélectionner une touche qui n'est utilisée par aucune autre application. Elle servira à transmettre vers les pilotes et les autres contrôleurs.

## Tester votre microphone

Avant de vous connecter au réseau VATSIM, vérifiez le bon fonctionnement de votre microphone.

Cliquez sur **Start mic test**, puis parlez normalement. Si votre microphone est correctement configuré, l'indicateur de niveau doit rester dans la zone verte.

Une fois le test terminé, cliquez sur **Apply**, puis sur **OK**.

# Étapes suivantes

Votre poste de contrôle est maintenant entièrement configuré.

Avant de prendre une position de contrôle, nous vous recommandons de passer quelque temps en observation afin de vous familiariser avec CoFrance, le Controller Pack et les procédures utilisées dans l'espace aérien français.

Notre guide consacré au mode **Observer** vous explique comment rejoindre le réseau VATSIM en toute sécurité avant votre première session de contrôle.

Bon apprentissage et à bientôt sur les fréquences de la French vACC !