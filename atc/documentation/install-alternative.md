---
title: Installations alternatives du pack contrôleur
description: 
published: true
date: 2026-07-19T19:38:17.390Z
tags: 
editor: markdown
dateCreated: 2026-03-03T22:20:51.116Z
---

![banner_tools_fr.png](/banners/banner_tools_fr.png)
# Préambule et objectifs


<a href="https://www.sia.aviation-civile.gouv.fr" target="_blank">SIA</a>

L’objectif de cette fiche est de vous partager les solutions alternatives pour installer et utiliser les outils de contrôle aérien de la French vACC (Linux- MacOS) en se passant de la virtualisation “classique” (VirtualBox, Parallels etc…) avec l’utilisation de Wine.

Ces solutions ne sont certainement pas les seules et sont vouées à améliorations. Chacun est encouragé à partager son retour d'expérience via le Discord de French vACC.

Ce document décrit l’installation de :

- <a href="https://github.com/pierr3/VectorAudio" target="_blank">Vector Audio pour la communication vocale</a>
- <a href="https://www.euroscope.hu/wp" target="_blank">Euroscope et le pack CoFrance à travers Wine</a>
- <a href="https://vatis.app/docs/" target="_blank">vATIS</a>


Il est fortement recommandé de lire la documentation des différents logiciels, principalement de Wine si vous découvrez ce logiciel. La documentation se trouve <a href="https://gitlab.winehq.org/wine/wine/-/wikis/fr/home" target="_blank">ici</a>. 

>**_Prérequis avant d’aller plus loin_**: savoir installer des programmes en fonction du système et/ou de la distribution utilisée. {.is-warning}


Voici une solution alternative sous Linux permettant une  <a href="https://lutris.net/" target="_blank">winecfg spécifique par application</a>. 

Et enfin quelques références documentaires utiles:
- <a href="https://forums.vatsim.net/topic/31019-euroscope-on-linux-howto/" target="_blank">Forum Euroscope</a>
- https://github.com/jonaseberle/euroscope-afv-wine

>La marche à suivre sur les pages suivantes a été testée sous ArchLinux et Ubuntu 22.04 LTS


# Etape 1 : Installer Wine

Commençons par installer **Wine**, **Wine-mono** et **Winetricks**.

En fonction de votre système d’exploitation :

- si vous êtes sur Linux, se référer à <a href="https://wiki.winehq.org/FAQ#Installing_Wine" target="_blank">ce lien</a>
- si vous êtes sur Ubuntu, se référer à <a href="https://doc.ubuntu-fr.org/wine" target="_blank">ce lien</a> 
- si vous êtes sous Arch linux, se référer à <a href="https://wiki.archlinux.org/title/Wine_(Fran%C3%A7ais)" target="_blank">ce lien</a>
- si vous êtes sur MacOS, se référer à <a href="https://wiki.winehq.org/MacOS" target="_blank">ce lien</a> 


Ensuite, pour installer Winetricks, consultez <a href="https://wiki.winehq.org/Winetricks" target="_blank">le lien suivant</a> 

Nota: Il est possible que vous ayez besoin d’activer la prise en charge 32-bit sur votre système.
Vérifier la documentation spécifique à votre distribution pour le faire.

Enfin, depuis l’interface Winetricks ou par la commande: winetricks `-q [nom du module]`, il ne vous reste plus qu’à installer les extensions suivantes :

- dotnet40
- dotnet45
- dotnet46
- dotnet461
- dotnet462
- dotnet472
- dotnet48
- dotnet60
- iertutil
- msls31
- msxml6
- urlmon
- vcrun2010
- vcrun2017
- wininet




Une fois ceci fait, passons à l’étape 2 pour installer le client audio qui nous permettra d’entendre les pilotes et de pouvoir communiquer avec eux.

# Etape 2 : Installer Vector Audio

TrackAudio est un client audio alternatif et multi-plateformes pour Vatsim. L'installation ce fait via <a href="https://github.com/pierr3/TrackAudio" target="_blank"> le lien suivant</a>. 


![trackaudioa_appercu.png](/doc-atc/trackaudioa_appercu.png)

# Etape 3 : Installer vAtis

**vAtis**:
vATIS est maintenant multiplateforme: <a href="https://vatis.app/" target="_blank"> le fichier d'installation se trouve ici</a>.

Ajouter les <a href="https://github.com/vaccfr/vatis-profiles" target="_blank"> profils</a>.

French vACC a rédigé une fiche sur le fonctionnement de vATIS. Cette fiche est disponible [ici](/fr/atc/documentation/vatis).


# Etape 4 : Installer Euroscope + CoFrance

Suivre le tutoriel d’installation standard disponible <a href="https://www.youtube.com/watch?v=VLQ42PTqrFU" target="_blank"> ici (vidéo) </a>. 

_Note_ : la structure de l'installation est en cours de changement. 

Euroscope s’installera dans votre environnement Wine.

La partie installation des polices diffère.
Il suffit de copier les fichiers .ttf c:\windows\fonts de votre environnement wine

>TIP: Pour les utilisateurs de grands écrans, il est possible via winecfg de modifier la taille de police.
Cela peut être utile pour Euroscope mais attention à remettre le paramètre au minimum pour lancer vATIS.






