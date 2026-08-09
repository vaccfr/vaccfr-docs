---
title: Outil vATIS
description: 
published: true
date: 2026-07-19T19:36:44.552Z
tags: 
editor: markdown
dateCreated: 2026-02-28T22:01:45.178Z
---

![banner_tools_fr.png](/banners/banner_tools_fr.png)
# Introduction
vATIS est un outil de gestion d’ATIS sur le réseau Vatsim. Il permet entre autres de créer des ATIS vocaux mais aussi de mettre en service plusieurs ATIS par session et par contrôleur. Dans cette fiche nous apprendrons à nous servir de cet outil dans le cadre du contrôle en France.
Vous trouverez ci joint la documentation fournie par les développeurs du logiciel : <a href="https://vatis.app/#/?id=what-is-vatis" target="_blank">Documentation vatis</a>


# Installation

La première étape est très simple, il s’agit de l’installation du programme. Pour cela, rendez-vous sur le lien github ci-dessous. <a href="https://github.com/vatis-project/vatis/releases" target="_blank">Téléchargement vATIS</a>


L'installation des fichiers de configuration classés par FIR sont obligatoires. 

<a href="https://github.com/vaccfr/vatis-profiles/releases/" target="_blank">Téléchargement des profils</a>


# Réglages

![param_vatis.png](/param_vatis.png)


1. Choisissez un serveur de réseau géographiquement le plus proche de votre emplacement.
2. Renseignez votre Nom, votre CID ainsi que votre mot de passe.
3. Puis sauvegardez les paramètres.


![param_vatis_2.png](/param_vatis_2.png)

# Configuration


Chaque fois que vous lancez vATIS, une boîte de dialogue s’affiche avec une liste de profils. La première fois que vous exécutez vATIS, la liste sera vide. Vous devez donc importer le fichier de configuration de la FIR qui vous intéresse. Dans le cadre de cette fiche nous prendrons comme exemple la FIR de Paris ( LFFF ).

Pour importer un profil VATIS, cliquez sur le bouton Importer . Une boîte de dialogue de navigateur de fichiers s'affiche, vous permettant de naviguer jusqu'à l'emplacement du fichier de profil. L'importation d'un profil importera les composites associés et leurs options et paramètres configurés.
Afin d’ouvrir un profil, double-cliquez sur le nom du profil dans la liste. La boîte de dialogue Profil disparaîtra afin de laisser place à la fenêtre principale de VATIS.


**Décryptons ensemble les différents éléments de cette fenêtre principale :**


![elements_vatis.png](/elements_vatis.png)


1. Ouvre la fenêtre Paramètres VATIS . Dans cette fenêtre, vous pouvez définir vos informations d'identification VATSIM, faire en sorte que la fenêtre vATIS reste visible et activer ou désactiver le son de notification ATIS.

2. Ouvre la fenêtre Configuration du profil . Dans cette fenêtre, vous pouvez créer, modifier ou supprimer des composites.

3. L'heure actuelle (UTC).

4. Masque la fenêtre principale du VATIS et ouvre la fenêtre "Mini Display".

5. Les composites associés au profil actuel. Si l'ATIS est connecté et transmet activement, la lettre ATIS s'affichera alors à côté de l'identifiant de la station en lettres de couleur cyan. La lettre ATIS clignotera en jaune s'il y a une nouvelle mise à jour. La lettre ATIS disparaîtra si l'ATIS n'est pas connecté au réseau.

6. La lettre ATIS actuelle. Cliquez avec le bouton gauche sur la lettre ATIS pour passer à la lettre suivante dans la séquence. Faites un clic droit pour revenir à la lettre précédente.

7. Le rapport METAR actuel.

8. Le réglage actuel du vent et de la pression du rapport METAR.

9. Un champ de texte libre utilisé pour définir les conditions actuelles de l'aéroport , telles que les pistes actives, les approches utilisées, etc. Si vous avez besoin de le modifier vous pouvez modifier le texte et l’enregistrer avec la petite disquette en bas à gauche. Un clique sur le texte ARPT COND permet d’activer des conditions que l’on aura préalablement définies.

10. Un champ de texte de forme libre utilisé pour définir les messages NOTAM , le cas échéant. De la même manière, un clique sur le texte “NOTAMS” permet d’active des NOTAM que l’on aura préalablement définis (par exemple: une fermeture de piste)

11. Enregistrez manuellement un ATIS à l'aide d'un microphone.

12. Une liste déroulante de tous les préréglages enregistrés pour le composite.

13. Ce bouton est utilisé pour connecter ou déconnecter l'ATIS du réseau.

# Atis vocal automatique

vATIS produit un texte à partir de l’ATIS texte envoyé sur le réseau VATSIM. Ce texte est ensuite envoyé à un synthétiseur vocal qui se charge de le transformer en voix. Il est ensuite à son tour envoyé sur le réseau VATSIM.

Il est important d’appliquer quelques règles afin que le texte soit correctement lu. Cela s’applique principalement aux champs décrivant les conditions de l'aéroport ainsi que les NOTAMs.

Toutes les pistes doivent être préfixées par RUNWAY, RUNWAYS, RY, RWY, RWYS, ou ^. Par exemple:
- Incorrecte: :”DEPARTURE 04R” sera a lu “DEPARTURE 04R”
- Correcte: “DEPARTURE RUNWAY 04R” sera lu “DEPARTURE 04 RIGHT”

Tous les départs et les transitions doivent être ajoutés dans le panel Contractions afin d’être lu correctement. Sans eux “7A” serait lu “SEVENA” au lieu de “SEVEN ALPHA”:


![vatis_alphzabet.png](/vatis_alphzabet.png)

Le panel Sandbox permet de valider que l’ATIS text et voix sont formatés et lus correctement. Cliquez sur le bouton “Fetch”, choisissez la version de l’ATIS et le preset, puis cliquez sur Refresh ATIS pour mettre à jour le texte. Cliquez sur “Play Voice ATIS” pour écouter l’ATIS voix:

![voix_vatis.png](/voix_vatis.png)

# Atis vocal enregistré


vATIS vous permet d'enregistrer manuellement un ATIS dans le cas où l'ATIS réel n'est pas numérisé et que vous souhaitez le simuler sur VATSIM. Pour enregistrer manuellement un ATIS, le Composite doit être configuré pour être enregistré vocalement. Voir la section Configuration pour plus de détails sur la façon de définir cette option.

1. Dans la configuration du profil, pensez à bien sélectionner Voice Recorded. Une fois la modification effectuée, n'oubliez pas d’enregistrer.

2. Connectez l'ATIS au réseau en cliquant sur le bouton CONNECT .

3. Cliquez sur le bouton Record Atis. Une fenêtre de dialogue apparaîtra. Sélectionnez votre périphérique d’entrée et votre périphérique de sortie (utilisé pour écouter l'enregistrement avant de le sauvegarder).

4. Cliquez sur le bouton Start recording l'enregistrement pour commencer l'enregistrement de votre ATIS. Une fois l'enregistrement terminé, cliquez sur le bouton Stop Recording.

5. Vous pouvez éventuellement écouter l'enregistrement en cliquant sur le bouton Listen.

6. Une fois que vous êtes satisfait, cliquez sur le bouton Save . L'ATIS commencera à émettre sur le réseau.

Lorsqu'une nouvelle mise à jour METAR est disponible, vous serez averti par l'icône du client clignotant dans la barre des tâches ainsi que la lettre ATIS clignotant en jaune. Suivez les étapes 2 à 5 pour enregistrer un nouvel ATIS.


![recording_voice_vatis.png](/recording_voice_vatis.png)

# Connexion

La connexion est très simple, il vous suffira de sélectionner la plateforme sur laquelle vous souhaitez mettre en place un ATIS et de sélectionner la configuration de votre plateforme.

Si l’on souhaite par exemple ouvrir un ATIS sur LFPG, il faut sélectionner la fenêtre adéquate puis la configuration  (est lié pour l’exemple). Il faut ensuite cliquer sur Connect pour connecter l’ATIS. Il est possible de réitérer cette action afin de connecter d’autres ATIS. 

>Si vous remarquez des erreurs ou des oublis dans les fichiers et profils que la French vACC fournit, n'hésitez surtout pas à nous en faire savoir en ouvrant une issue sur GitHub. {.is-warning}

