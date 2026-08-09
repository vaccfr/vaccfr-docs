---
title: Installation des outils pour contrôler
description: 
published: true
date: 2026-07-11T13:05:50.791Z
tags: 
editor: markdown
dateCreated: 2026-04-26T21:21:51.800Z
---

# Installation des outils pour contrôler

Bienvenue sur cette page ! Ici, nous vous expliquons tout ce dont vous avez besoin pour contrôler en France sur VATSIM. Nous vous guidons pas à pas pour installer tous les logiciels nécessaires.

# Euroscope

Euroscope est le logiciel qui simule le radar du contrôleur. Ce sera donc notre outil de contrôle indispensable.![lfbb_img1.png](/lfbb_img1.png =50%x){.align-center}

## Prérequis

- **Système d'exploitation** : Windows XP; Me; Vista; 7; 10; 11 (recommandé) - 32 bit, 64-bit (recommandé)
- Dernière version des frameworks [Microsoft .NET](https://dotnet.microsoft.com/fr-fr/download)

Les autres dépendances nécessaires sont précisées sur le site de l'éditeur d'Euroscope et proposées lors de l'installation du logiciel.

## Installation d'Euroscope

> La version utilisée par French vACC est la 3.2.9. Il ne s'agit pas de la dernière version du logiciel.
{.is-warning}


- Rendez-vous sur [ce lien](https://euroscope.hu/install/EuroScopeSetup.3.2.9.msi) et **téléchargez l'installateur** (version 3.2.9)
- Lancez l'installation en suivant les étapes. Assurez-vous que le **répertoire d'installation** est `C:\Program Files (x86)\Euroscope`

![euroscope_install.png](/euroscope_install.png =50%x){.align-center}

# Télécharger le pack contrôleur

Maintenant que vous disposez d'Euroscope, il vaut faut télécharger le pack contrôleur, c'est à dire le package de données vous permettant d'avoir la visualisation radar appropriée pour contrôler.

## 🌍 Liens des packs par FIR

- LFFM – Pack de base CoFrance : https://files.aero-nav.com/LFFM
- LFBB – Bordeaux : https://files.aero-nav.com/LFBB
- LFEE – Reims : https://files.aero-nav.com/LFEE
- LFFF – Paris : https://files.aero-nav.com/LFFF
- LFMM – Marseille : https://files.aero-nav.com/LFMM
- LFRR – Brest : https://files.aero-nav.com/LFRR

> Les packs sont compartimentés par FIR afin d'en limiter le poids pour Euroscope au chargement des fichiers.
{.is-info}

> La FIR LFFM (anciennement LFXX) est utilisée comme pack de base global pour toutes les FIR (settings et plugins) et n'est déosrmais utilisée que pour les opérations militaires.
{.is-warning}

## 📥 Quels fichiers télécharger ?

### Première installation

Vous devez télécharger le `Pack de base CoFrance` ainsi que l'ensemble des `Install-Packages` de chacune des FIRs pré-citées.

### Vous avez déja installé un pack auparavant

Vous devez télécharger l'archive `Update-Package` pour la FIR correspondante.

> Le téléchargement via `Update-Package` n'est pas à utiliser pour une première installation.
{.is-warning}

## 📥 Installation des packs

Il existe 2 méthodes de téléchargement, à vosu de choisir celle qui répond le mieux à vos besoins.

### Méthode automatique (recommandée)

Dès lors que vous aurez téléchargé le pack de base et les Install-Packages de l'ensemble des FIRs. Rendez-vous sur le Github maintenu par la vACC pour y télécharger :
- [L'installeur de pack (installer)](https://github.com/vaccfr/Sector-Files/releases)
- [Le configurateur de profil (ProfileConfigurator)](https://github.com/vaccfr/Sector-Files/releases)

Une fois ces éléments téléchargés, vous avez tout ce qu'il faut pour débuter l'installation.

#### Étape 1 : Pack Installer

Ouvrez **Installer.exe** et suivez les instructions affichées à l'écran.

1) Sélectionnez le dossier dans lequel vous souhaitez installer les packs
2) Cliquez sur **Install/Update Packages** puis sélectionnez tous les packs

> S'il s'agit de votre **première installation**, vous devriez avoir un total de **6 packs sélectionnés**.
{.is-info}

Une fois les packs sélectionnés, cliquez sur **Install Controller Pack**. L'installation devrait alors s'effectuer sans encombre. L'installer indiquera un message dans ce sens.

![controller_pack_installer.png](/controller_pack_installer.png){.align-center}

#### Étape 2 : Profile Configurator

Ouvrez **ProfileConfigurator.exe**. Une fois l'application ouverte, renseignez :
- votre nom
- votre CID
- votre mot de passe
- votre grade contrôleur
- l'activation ou non du *Discord Rich Presence*

![profile_configurator.png](/profile_configurator.png){.align-center}

> _Aucune des infos saisies n'est stockée ailleurs que sur votre ordinateur_. L'application se charger simplement de modifier les fichiers **.prf** avec les infos saisies. Votre CID est aussi modifié automatiquement dans les liens de feedback.
{.is-info}

### Méthode manuelle

Une fois le `Pack de base` et les `packs de FIRs individuels` téléchargés, créez un dossier principal pour vos fichiers secteurs français. Nommez le "France" par exemple. Placez alors tous les packs téléchargez à l'intérieur

> S'il s'agit de votre **première installation**, vous devriez avoir un total de **6 packs sélectionnés**.
{.is-info}

Effectuez les modifications suivantes :
1) Renommez le dossier **LFFM** du CoFrance Base Pack en **LFXX**
2) A l'intérieur du dossier **LFXX**, créez un dossier nommé **Sector**
3) Déplacez tous les fichiers **.sct** et **.ese** spécifiques aux FIRs dans **LFXX/Sector**
4) Renommez tous les fichiers **.sct et .ese** uniquement avec leur code FIR afin de faciliter les futures mises à jour (ex : *LFFF.sct / LFFF.ese, LFEE.sct / LFEE.ese, LFMM.sct / LFMM.ese, etc*)
5) Déplacez tous les fichiers **.prf** dans leurs dossiers FIRs respectifs (ex : CCA Aquitaine.prf doit être placé dnas le dossier **LFBB**)

Votre structure finale devra donc contenir un dossier principal (ex : France) avec à l'intérieur :
- le pack de base renommé **LFXX**
- Tous les dossiers FIRs individuels (**LFBB**, **LFEE**, **LFFF**, etc)

Cette organisation est nécessaire afin que chacun des packs puisse **référencer le répertoire LFXX (pack de base)**

> Veillez à respecter scrupuleusement cette procédure au risque d'avoir des erreurs à l'ouverture de vos fichiers .prf.
{.is-warning}

![root_sector_files.png](/root_sector_files.png){.align-center}
<center><b>Exemple du dossier racine des packs une fois installés</b></center>

![fir_folder_example.png](/fir_folder_example.png){.align-center}
<center><b>Exemple d'un dossier FIR (pack individuel)</b></center>


## Réglages importants avant lancement

Avant de lancer un pack, il est **essentiel** d'effectuer les réglages suivants dans Euroscope. Ceci vous permettra de changer facilement entre les différents profils.

> Pro-tip : Créez d'abord un raccourci vers le bureau de l'éxécutable Euroscope. Ceci vous permettra de gagner beaucoup de temps Le .exe du logiciel est normalement installé à cet endroit : `C:\Users\nom_utilisateur\AppData\Roaming\EuroScope\`
{.is-info}

![auto_load_last_profile.png](/auto_load_last_profile.png){.align-right}

1) Lancez Euroscope
2) Cliquez sur **Other Set** dans la barre verte, en haut du logiciel
3) Décochez **Auto load last profile on startup**
4) Redémarrez Euroscope

Au redémarrage, Euroscope vous demanderea de charger un fichier .prf (profil). Ces profils vous permettront de basculer entre les différentes FIRs (par exemple : *CoFrance LFBB.prf, CoFrance LFEE.prf, etc*)

> **Une explication détaillée des profils est présentée plus bas dans cette page**.
{.is-info}

## Lancement d'Euroscope avec son pack FIR

Ouvrez Euroscope. Lorsque le logiciel vous le demande, accédez au dossier dans lequel vous avez installé votre pack contrôleur.

Sélectionnez ensuite le fichier .prf (profil) correspondant afin de charger la FIR.

> Le fichier .prf vous permet de lancer Euroscope avec les bons réglages pour la FIR choisie.
{.is-info}

![open_prf.png](/open_prf.png){.align-center}

> Pas de panique, au premier lancement, vous pourriez recevoir une erreur vous indiquant un problème avec le fichier .toml. 
{.is-info}

## Structure des packs FIR

Dans cette section, vous trouverez la structure des packs FIR ainsi que des explications détaillées pour comprendre à quoi correspondent les différents fichiers et dossiers.

### Explication des profils (.prf)

Par défaut, chaque pack FIR contient un fichier “CoFrance {CODE FIR}.prf”. Ce profil charge automatiquement tous les éléments essentiels, notamment :
- Un fichier **.asr** pour l’UIR ou la FIR
- Un fichier **.asr** pour l’APP (approche)
- Les fichiers AVISO .asr individuels

Vous avez alors une configuration de base prête à l'emploi.

### Profils spécifiques (CCA)

Ces profils sont spécifiques à un Centre de Contrôle d’Approche (CCA).

> Exemple : EGA Paris.prf, CCA Nice.prf

Ces profils chargent uniquement les fichiers .asr liés à ce CCA, ainsi que les cartes CoFrance v2 correspondantes.

Par défaut, les profils configurent automatiquement les raccourcis *ASRFastKeys (F1+1 à F1+9)* ainsi que les raccourcis *RecentFiles 1 à 9* avec les vues suivantes :
```diagram
PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHN0eWxlPSJiYWNrZ3JvdW5kOiB0cmFuc3BhcmVudDsgYmFja2dyb3VuZC1jb2xvcjogdHJhbnNwYXJlbnQ7IGNvbG9yLXNjaGVtZTogbGlnaHQgZGFyazsiIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2ZXJzaW9uPSIxLjEiIHdpZHRoPSI0NTFweCIgaGVpZ2h0PSIxNjFweCIgdmlld0JveD0iMCAwIDQ1MSAxNjEiIGNvbnRlbnQ9IiZsdDtteGZpbGUgaG9zdD0mcXVvdDtlbWJlZC5kaWFncmFtcy5uZXQmcXVvdDsmZ3Q7Jmx0O2RpYWdyYW0gaWQ9JnF1b3Q7Z2dDcDV6WkVXU2t0aEktZXZrVzMmcXVvdDsgbmFtZT0mcXVvdDtQYWdlLTEmcXVvdDsmZ3Q7N1ZsdGI1c3dFUDQxU051SFRid24rWml3cHF1MGFWSXlkWjhkY01DYXNabHhtbVMvZm1jd0FRTHAycFZNcllRVUNkL0RjVGIzUEw2TGpPRUU2ZUZXb0N6NXlpTk1EZHVNRG9ienliQnR5N1ZjdUNqa1dDS1RxVk1Dc1NDUmRxcUJOZm1OTldocWRFY2luTGNjSmVkVWtxd05ocHd4SE1vV2hvVGcrN2JibHRQMnJCbUtjUWRZaDRoMjBSOGtra21KVHUxSmpYL0dKRTZxbVMxL1Z0NUpVZVdzM3lSUFVNVDNEY2k1TVp4QWNDN0xVWG9JTUZYSnEvSlNQcmU4Y1BlME1JR1pmTW9EZHZjQkhTT1h4K3AxWVpHWkdrcTBVZEFpbDBoSXpZb0pOcVJaSXNLd0FOc3FiRXBSbHBQQ3UvUklDSTIrb0NQZnlTcE9aUzIyOExRT1p2bGdsOU0vSUxyVDAyc0FDNGtQalNYcUY3ckZQTVZTSE1FbGFlYmMxeG5lMXdTNW5zWjBHRmVieDBwZDJrWmFIdkVwZEoxQkdPZ2s5aWZVNlNiVWZqeWhLOFgvSXVHQy9GWjVwRHBsNTBuTzl5U2xpSUd3VUhRR0xYaXhrY3FuQlArSkEwNjVJb093QkF1aWtpeDVwajBvM2tvOTNIQXBlYW9Ob1hObjloSVlDWjU5UnlMR2xjdVdVRnBOd3poVHNzZzRZYkpJbmJlQUh5UXpNRDk2aGdkdkhJQnQxVGI4bEx1UUFXZXdZdENPQ290Ukx2YzR2NTRtM0VjazhSTE8zUzduemtYT3dVc1NSRmRRbHhDTGkvMlV5SlRxcmJOUGlNVHJESVhLZFEvVnM5eGVxb3FobW8xTExITkl5SllXOVNRaFVZVFpHVkdHN2N6OXFibVlQbHNSQmJkWTNEemdrbUxyYVNUNXRHS3psUXovMTQ1WE56N2tSWWc1T0ZodWRpamlRT0V1RnF4QUVXL2UyWjZuTkdTYnpjSDd3clVLQmFOWVg0czVONzBUZHYxWEtBejVUb1JFelVyUkE0RXFwa01BN1p2enNJQ1ZiMVBCdzhqUW1sbVhaYWlqMVlwNWZqaEVnVHlHSkpTS0hZdnlqcmhQSzMyUzNyMVI3NC9xdmFPYS83a0JscHlGa25CMlViRjk0aDVHeGJZM2EvWFhnVlY5Q244ZFZVKzZxaDQ3OXh2bzNNZTJ5MHNhK2JRcmdjbXJMR3lhdDlmY3d6dDFDV2dHaWxSeHM4WnUyaERkYkJUZDFVUjN2MVA4Q2hRaCtGZG5Cc0g4eXNwNzJ4M1E2amsrR0Z2ZzIybUIwd0Zhb05WM0luVDVTR2lzUi8vYUJPMnhDVFpsMTNOdU5zcHUyRFo0djF5TlRmQ3ZTdXc3elJ1YjRGQk5jUENlWjlrRE5MMitFNjFLQjJQMUdiRHBPV1BUYThyT0gyVjNQZG5ONysvVzM4QUJWcURxVTE2Y3FqSXBqTUF4Rmk1VmwvbE1vVmpOTTEvZXJjZStXSXNWelBvcmRPbGVmOHQzYnY0QSZsdDsvZGlhZ3JhbSZndDsmbHQ7L214ZmlsZSZndDsiPjxkZWZzLz48Zz48ZyBkYXRhLWNlbGwtaWQ9IjAiPjxnIGRhdGEtY2VsbC1pZD0iMSI+PGcgZGF0YS1jZWxsLWlkPSIyIj48ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjUsMC41KSI+PHJlY3QgeD0iMCIgeT0iMCIgd2lkdGg9IjQ1MCIgaGVpZ2h0PSIxNjAiIGZpbGw9IiNmZmZmZmYiIHN0cm9rZT0ibm9uZSIgcG9pbnRlci1ldmVudHM9Im5vbmUiIHN0eWxlPSJmaWxsOiBsaWdodC1kYXJrKCNmZmZmZmYsIHZhcigtLWdlLWRhcmstY29sb3IsICMxMjEyMTIpKTsiLz48cGF0aCBkPSJNIDAgMCBMIDQ1MCAwIEwgNDUwIDE2MCBMIDAgMTYwIEwgMCAwIiBmaWxsPSJub25lIiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS1saW5lY2FwPSJzcXVhcmUiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9Im5vbmUiIHN0eWxlPSJzdHJva2U6IGxpZ2h0LWRhcmsocmdiKDAsIDAsIDApLCByZ2IoMjU1LCAyNTUsIDI1NSkpOyIvPjxwYXRoIGQ9Ik0gMCA0MCBMIDE5MSA0MCBMIDQ1MCA0MCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMDAwMDAwIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJub25lIiBzdHlsZT0ic3Ryb2tlOiBsaWdodC1kYXJrKHJnYigwLCAwLCAwKSwgcmdiKDI1NSwgMjU1LCAyNTUpKTsiLz48cGF0aCBkPSJNIDAgODAgTCAxOTEgODAgTCA0NTAgODAiIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiBwb2ludGVyLWV2ZW50cz0ibm9uZSIgc3R5bGU9InN0cm9rZTogbGlnaHQtZGFyayhyZ2IoMCwgMCwgMCksIHJnYigyNTUsIDI1NSwgMjU1KSk7Ii8+PHBhdGggZD0iTSAwIDEyMCBMIDE5MSAxMjAgTCA0NTAgMTIwIiBmaWxsPSJub25lIiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9Im5vbmUiIHN0eWxlPSJzdHJva2U6IGxpZ2h0LWRhcmsocmdiKDAsIDAsIDApLCByZ2IoMjU1LCAyNTUsIDI1NSkpOyIvPjxwYXRoIGQ9Ik0gMTkxIDAgTCAxOTEgNDAgTCAxOTEgODAgTCAxOTEgMTIwIEwgMTkxIDE2MCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMDAwMDAwIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJub25lIiBzdHlsZT0ic3Ryb2tlOiBsaWdodC1kYXJrKHJnYigwLCAwLCAwKSwgcmdiKDI1NSwgMjU1LCAyNTUpKTsiLz48L2c+PGcgZGF0YS1jZWxsLWlkPSIzIj48ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjUsMC41KSIvPjxnIGRhdGEtY2VsbC1pZD0iNCI+PGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC41LDAuNSkiPjxyZWN0IHg9IjAiIHk9IjAiIHdpZHRoPSIxOTEiIGhlaWdodD0iNDAiIGZpbGw9IiNhNjgwYjgiIHN0cm9rZT0ibm9uZSIgcG9pbnRlci1ldmVudHM9ImFsbCIgc3R5bGU9ImZpbGw6IGxpZ2h0LWRhcmsocmdiKDE2NiwgMTI4LCAxODQpLCByZ2IoMTM5LCAxMDYsIDE1NCkpOyIvPjxwYXRoIGQ9Ik0gMCAwIE0gMTkxIDAgTSAxOTEgNDAgTSAwIDQwIiBmaWxsPSJub25lIiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS1saW5lY2FwPSJzcXVhcmUiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9ImFsbCIgc3R5bGU9InN0cm9rZTogbGlnaHQtZGFyayhyZ2IoMCwgMCwgMCksIHJnYigyNTUsIDI1NSwgMjU1KSk7Ii8+PC9nPjxnPjxnPjxzd2l0Y2g+PGZvcmVpZ25PYmplY3Qgc3R5bGU9Im92ZXJmbG93OiB2aXNpYmxlOyB0ZXh0LWFsaWduOiBsZWZ0OyIgcG9pbnRlci1ldmVudHM9Im5vbmUiIHdpZHRoPSIxMDAlIiBoZWlnaHQ9IjEwMCUiIHJlcXVpcmVkRmVhdHVyZXM9Imh0dHA6Ly93d3cudzMub3JnL1RSL1NWRzExL2ZlYXR1cmUjRXh0ZW5zaWJpbGl0eSI+PGRpdiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94aHRtbCIgc3R5bGU9ImRpc3BsYXk6IGZsZXg7IGFsaWduLWl0ZW1zOiB1bnNhZmUgY2VudGVyOyBqdXN0aWZ5LWNvbnRlbnQ6IHVuc2FmZSBjZW50ZXI7IHdpZHRoOiAxODlweDsgaGVpZ2h0OiAxcHg7IHBhZGRpbmctdG9wOiAyMHB4OyBtYXJnaW4tbGVmdDogMXB4OyI+PGRpdiBzdHlsZT0iYm94LXNpemluZzogYm9yZGVyLWJveDsgZm9udC1zaXplOiAwOyB0ZXh0LWFsaWduOiBjZW50ZXI7IG1heC1oZWlnaHQ6IDM2cHg7IG92ZXJmbG93OiBoaWRkZW47IGNvbG9yOiAjMDAwMDAwOyAiPjxkaXYgc3R5bGU9ImRpc3BsYXk6IGlubGluZS1ibG9jazsgZm9udC1zaXplOiAxNnB4OyBmb250LWZhbWlseTogSGVsdmV0aWNhOyBjb2xvcjogbGlnaHQtZGFyaygjMDAwMDAwLCAjZmZmZmZmKTsgbGluZS1oZWlnaHQ6IDEuMjsgcG9pbnRlci1ldmVudHM6IGFsbDsgd2hpdGUtc3BhY2U6IG5vcm1hbDsgd29yZC13cmFwOiBub3JtYWw7ICI+PGZvbnQgc3R5bGU9ImZvbnQtc2l6ZTogMTRweDsgY29sb3I6IGxpZ2h0LWRhcmsocmdiKDI1NSwgMjU1LCAyNTUpLCByZ2IoMTgsIDE4LCAxOCkpOyI+PGIgc3R5bGU9IiI+UmFjY291cmNpIGNsYXZpZXI8L2I+PC9mb250PjwvZGl2PjwvZGl2PjwvZGl2PjwvZm9yZWlnbk9iamVjdD48dGV4dCB4PSI5NiIgeT0iMjUiIGZpbGw9ImxpZ2h0LWRhcmsoIzAwMDAwMCwgI2ZmZmZmZikiIGZvbnQtZmFtaWx5PSJIZWx2ZXRpY2EiIGZvbnQtc2l6ZT0iMTZweCIgdGV4dC1hbmNob3I9Im1pZGRsZSI+UmFjY291cmNpIGNsYXZpZXI8L3RleHQ+PC9zd2l0Y2g+PC9nPjwvZz48L2c+PGcgZGF0YS1jZWxsLWlkPSI1Ij48ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjUsMC41KSI+PHJlY3QgeD0iMTkxIiB5PSIwIiB3aWR0aD0iMjU5IiBoZWlnaHQ9IjQwIiBmaWxsPSIjYTY4MGI4IiBzdHJva2U9Im5vbmUiIHBvaW50ZXItZXZlbnRzPSJhbGwiIHN0eWxlPSJmaWxsOiBsaWdodC1kYXJrKHJnYigxNjYsIDEyOCwgMTg0KSwgcmdiKDEzOSwgMTA2LCAxNTQpKTsiLz48cGF0aCBkPSJNIDE5MSAwIE0gNDUwIDAgTSA0NTAgNDAgTSAxOTEgNDAiIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLWxpbmVjYXA9InNxdWFyZSIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiBwb2ludGVyLWV2ZW50cz0iYWxsIiBzdHlsZT0ic3Ryb2tlOiBsaWdodC1kYXJrKHJnYigwLCAwLCAwKSwgcmdiKDI1NSwgMjU1LCAyNTUpKTsiLz48L2c+PGc+PGc+PHN3aXRjaD48Zm9yZWlnbk9iamVjdCBzdHlsZT0ib3ZlcmZsb3c6IHZpc2libGU7IHRleHQtYWxpZ246IGxlZnQ7IiBwb2ludGVyLWV2ZW50cz0ibm9uZSIgd2lkdGg9IjEwMCUiIGhlaWdodD0iMTAwJSIgcmVxdWlyZWRGZWF0dXJlcz0iaHR0cDovL3d3dy53My5vcmcvVFIvU1ZHMTEvZmVhdHVyZSNFeHRlbnNpYmlsaXR5Ij48ZGl2IHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hodG1sIiBzdHlsZT0iZGlzcGxheTogZmxleDsgYWxpZ24taXRlbXM6IHVuc2FmZSBjZW50ZXI7IGp1c3RpZnktY29udGVudDogdW5zYWZlIGNlbnRlcjsgd2lkdGg6IDI1N3B4OyBoZWlnaHQ6IDFweDsgcGFkZGluZy10b3A6IDIwcHg7IG1hcmdpbi1sZWZ0OiAxOTJweDsiPjxkaXYgc3R5bGU9ImJveC1zaXppbmc6IGJvcmRlci1ib3g7IGZvbnQtc2l6ZTogMDsgdGV4dC1hbGlnbjogY2VudGVyOyBtYXgtaGVpZ2h0OiAzNnB4OyBvdmVyZmxvdzogaGlkZGVuOyBjb2xvcjogIzAwMDAwMDsgIj48ZGl2IHN0eWxlPSJkaXNwbGF5OiBpbmxpbmUtYmxvY2s7IGZvbnQtc2l6ZTogMTZweDsgZm9udC1mYW1pbHk6IEhlbHZldGljYTsgY29sb3I6IGxpZ2h0LWRhcmsoIzAwMDAwMCwgI2ZmZmZmZik7IGxpbmUtaGVpZ2h0OiAxLjI7IHBvaW50ZXItZXZlbnRzOiBhbGw7IHdoaXRlLXNwYWNlOiBub3JtYWw7IHdvcmQtd3JhcDogbm9ybWFsOyAiPjxiPjxmb250IHN0eWxlPSJmb250LXNpemU6IDE0cHg7IGNvbG9yOiBsaWdodC1kYXJrKHJnYigyNTUsIDI1NSwgMjU1KSwgcmdiKDE4LCAxOCwgMTgpKTsiPkZvbmN0aW9uPC9mb250PjwvYj48L2Rpdj48L2Rpdj48L2Rpdj48L2ZvcmVpZ25PYmplY3Q+PHRleHQgeD0iMzIxIiB5PSIyNSIgZmlsbD0ibGlnaHQtZGFyaygjMDAwMDAwLCAjZmZmZmZmKSIgZm9udC1mYW1pbHk9IkhlbHZldGljYSIgZm9udC1zaXplPSIxNnB4IiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj5Gb25jdGlvbjwvdGV4dD48L3N3aXRjaD48L2c+PC9nPjwvZz48L2c+PGcgZGF0YS1jZWxsLWlkPSI3Ij48ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjUsMC41KSIvPjxnIGRhdGEtY2VsbC1pZD0iOCI+PGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC41LDAuNSkiPjxyZWN0IHg9IjAiIHk9IjQwIiB3aWR0aD0iMTkxIiBoZWlnaHQ9IjQwIiBmaWxsPSJub25lIiBzdHJva2U9Im5vbmUiIHBvaW50ZXItZXZlbnRzPSJhbGwiLz48cGF0aCBkPSJNIDAgNDAgTSAxOTEgNDAgTSAxOTEgODAgTSAwIDgwIiBmaWxsPSJub25lIiBzdHJva2U9IiMwMDAwMDAiIHN0cm9rZS1saW5lY2FwPSJzcXVhcmUiIHN0cm9rZS1taXRlcmxpbWl0PSIxMCIgcG9pbnRlci1ldmVudHM9ImFsbCIgc3R5bGU9InN0cm9rZTogbGlnaHQtZGFyayhyZ2IoMCwgMCwgMCksIHJnYigyNTUsIDI1NSwgMjU1KSk7Ii8+PC9nPjxnPjxnPjxzd2l0Y2g+PGZvcmVpZ25PYmplY3Qgc3R5bGU9Im92ZXJmbG93OiB2aXNpYmxlOyB0ZXh0LWFsaWduOiBsZWZ0OyIgcG9pbnRlci1ldmVudHM9Im5vbmUiIHdpZHRoPSIxMDAlIiBoZWlnaHQ9IjEwMCUiIHJlcXVpcmVkRmVhdHVyZXM9Imh0dHA6Ly93d3cudzMub3JnL1RSL1NWRzExL2ZlYXR1cmUjRXh0ZW5zaWJpbGl0eSI+PGRpdiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94aHRtbCIgc3R5bGU9ImRpc3BsYXk6IGZsZXg7IGFsaWduLWl0ZW1zOiB1bnNhZmUgY2VudGVyOyBqdXN0aWZ5LWNvbnRlbnQ6IHVuc2FmZSBjZW50ZXI7IHdpZHRoOiAxODlweDsgaGVpZ2h0OiAxcHg7IHBhZGRpbmctdG9wOiA2MHB4OyBtYXJnaW4tbGVmdDogMXB4OyI+PGRpdiBzdHlsZT0iYm94LXNpemluZzogYm9yZGVyLWJveDsgZm9udC1zaXplOiAwOyB0ZXh0LWFsaWduOiBjZW50ZXI7IG1heC1oZWlnaHQ6IDM2cHg7IG92ZXJmbG93OiBoaWRkZW47IGNvbG9yOiAjMDAwMDAwOyAiPjxkaXYgc3R5bGU9ImRpc3BsYXk6IGlubGluZS1ibG9jazsgZm9udC1zaXplOiAxNnB4OyBmb250LWZhbWlseTogSGVsdmV0aWNhOyBjb2xvcjogbGlnaHQtZGFyaygjMDAwMDAwLCAjZmZmZmZmKTsgbGluZS1oZWlnaHQ6IDEuMjsgcG9pbnRlci1ldmVudHM6IGFsbDsgd2hpdGUtc3BhY2U6IG5vcm1hbDsgd29yZC13cmFwOiBub3JtYWw7ICI+PGZvbnQgc3R5bGU9ImZvbnQtc2l6ZTogMTRweDsiPkYxICsgMTwvZm9udD48L2Rpdj48L2Rpdj48L2Rpdj48L2ZvcmVpZ25PYmplY3Q+PHRleHQgeD0iOTYiIHk9IjY1IiBmaWxsPSJsaWdodC1kYXJrKCMwMDAwMDAsICNmZmZmZmYpIiBmb250LWZhbWlseT0iSGVsdmV0aWNhIiBmb250LXNpemU9IjE2cHgiIHRleHQtYW5jaG9yPSJtaWRkbGUiPkYxICsgMTwvdGV4dD48L3N3aXRjaD48L2c+PC9nPjwvZz48ZyBkYXRhLWNlbGwtaWQ9IjkiPjxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuNSwwLjUpIj48cmVjdCB4PSIxOTEiIHk9IjQwIiB3aWR0aD0iMjU5IiBoZWlnaHQ9IjQwIiBmaWxsPSJub25lIiBzdHJva2U9Im5vbmUiIHBvaW50ZXItZXZlbnRzPSJhbGwiLz48cGF0aCBkPSJNIDE5MSA0MCBNIDQ1MCA0MCBNIDQ1MCA4MCBNIDE5MSA4MCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMDAwMDAwIiBzdHJva2UtbGluZWNhcD0ic3F1YXJlIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJhbGwiIHN0eWxlPSJzdHJva2U6IGxpZ2h0LWRhcmsocmdiKDAsIDAsIDApLCByZ2IoMjU1LCAyNTUsIDI1NSkpOyIvPjwvZz48Zz48Zz48c3dpdGNoPjxmb3JlaWduT2JqZWN0IHN0eWxlPSJvdmVyZmxvdzogdmlzaWJsZTsgdGV4dC1hbGlnbjogbGVmdDsiIHBvaW50ZXItZXZlbnRzPSJub25lIiB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiByZXF1aXJlZEZlYXR1cmVzPSJodHRwOi8vd3d3LnczLm9yZy9UUi9TVkcxMS9mZWF0dXJlI0V4dGVuc2liaWxpdHkiPjxkaXYgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGh0bWwiIHN0eWxlPSJkaXNwbGF5OiBmbGV4OyBhbGlnbi1pdGVtczogdW5zYWZlIGNlbnRlcjsganVzdGlmeS1jb250ZW50OiB1bnNhZmUgY2VudGVyOyB3aWR0aDogMjU3cHg7IGhlaWdodDogMXB4OyBwYWRkaW5nLXRvcDogNjBweDsgbWFyZ2luLWxlZnQ6IDE5MnB4OyI+PGRpdiBzdHlsZT0iYm94LXNpemluZzogYm9yZGVyLWJveDsgZm9udC1zaXplOiAwOyB0ZXh0LWFsaWduOiBjZW50ZXI7IG1heC1oZWlnaHQ6IDM2cHg7IG92ZXJmbG93OiBoaWRkZW47IGNvbG9yOiAjMDAwMDAwOyAiPjxkaXYgc3R5bGU9ImRpc3BsYXk6IGlubGluZS1ibG9jazsgZm9udC1zaXplOiAxNnB4OyBmb250LWZhbWlseTogSGVsdmV0aWNhOyBjb2xvcjogbGlnaHQtZGFyaygjMDAwMDAwLCAjZmZmZmZmKTsgbGluZS1oZWlnaHQ6IDEuMjsgcG9pbnRlci1ldmVudHM6IGFsbDsgd2hpdGUtc3BhY2U6IG5vcm1hbDsgd29yZC13cmFwOiBub3JtYWw7ICI+PGZvbnQgc3R5bGU9ImZvbnQtc2l6ZTogMTRweDsiPlZ1ZSByYWRhciBDQ0E8L2ZvbnQ+PC9kaXY+PC9kaXY+PC9kaXY+PC9mb3JlaWduT2JqZWN0Pjx0ZXh0IHg9IjMyMSIgeT0iNjUiIGZpbGw9ImxpZ2h0LWRhcmsoIzAwMDAwMCwgI2ZmZmZmZikiIGZvbnQtZmFtaWx5PSJIZWx2ZXRpY2EiIGZvbnQtc2l6ZT0iMTZweCIgdGV4dC1hbmNob3I9Im1pZGRsZSI+VnVlIHJhZGFyIENDQTwvdGV4dD48L3N3aXRjaD48L2c+PC9nPjwvZz48L2c+PGcgZGF0YS1jZWxsLWlkPSIxMSI+PGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC41LDAuNSkiLz48ZyBkYXRhLWNlbGwtaWQ9IjEyIj48ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjUsMC41KSI+PHJlY3QgeD0iMCIgeT0iODAiIHdpZHRoPSIxOTEiIGhlaWdodD0iNDAiIGZpbGw9Im5vbmUiIHN0cm9rZT0ibm9uZSIgcG9pbnRlci1ldmVudHM9ImFsbCIvPjxwYXRoIGQ9Ik0gMCA4MCBNIDE5MSA4MCBNIDE5MSAxMjAgTSAwIDEyMCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMDAwMDAwIiBzdHJva2UtbGluZWNhcD0ic3F1YXJlIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJhbGwiIHN0eWxlPSJzdHJva2U6IGxpZ2h0LWRhcmsocmdiKDAsIDAsIDApLCByZ2IoMjU1LCAyNTUsIDI1NSkpOyIvPjwvZz48Zz48Zz48c3dpdGNoPjxmb3JlaWduT2JqZWN0IHN0eWxlPSJvdmVyZmxvdzogdmlzaWJsZTsgdGV4dC1hbGlnbjogbGVmdDsiIHBvaW50ZXItZXZlbnRzPSJub25lIiB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiByZXF1aXJlZEZlYXR1cmVzPSJodHRwOi8vd3d3LnczLm9yZy9UUi9TVkcxMS9mZWF0dXJlI0V4dGVuc2liaWxpdHkiPjxkaXYgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGh0bWwiIHN0eWxlPSJkaXNwbGF5OiBmbGV4OyBhbGlnbi1pdGVtczogdW5zYWZlIGNlbnRlcjsganVzdGlmeS1jb250ZW50OiB1bnNhZmUgY2VudGVyOyB3aWR0aDogMTg5cHg7IGhlaWdodDogMXB4OyBwYWRkaW5nLXRvcDogMTAwcHg7IG1hcmdpbi1sZWZ0OiAxcHg7Ij48ZGl2IHN0eWxlPSJib3gtc2l6aW5nOiBib3JkZXItYm94OyBmb250LXNpemU6IDA7IHRleHQtYWxpZ246IGNlbnRlcjsgbWF4LWhlaWdodDogMzZweDsgb3ZlcmZsb3c6IGhpZGRlbjsgY29sb3I6ICMwMDAwMDA7ICI+PGRpdiBzdHlsZT0iZGlzcGxheTogaW5saW5lLWJsb2NrOyBmb250LXNpemU6IDE2cHg7IGZvbnQtZmFtaWx5OiBIZWx2ZXRpY2E7IGNvbG9yOiBsaWdodC1kYXJrKCMwMDAwMDAsICNmZmZmZmYpOyBsaW5lLWhlaWdodDogMS4yOyBwb2ludGVyLWV2ZW50czogYWxsOyB3aGl0ZS1zcGFjZTogbm9ybWFsOyB3b3JkLXdyYXA6IG5vcm1hbDsgIj48Zm9udCBzdHlsZT0iZm9udC1zaXplOiAxNHB4OyI+RjEgKyAyPC9mb250PjwvZGl2PjwvZGl2PjwvZGl2PjwvZm9yZWlnbk9iamVjdD48dGV4dCB4PSI5NiIgeT0iMTA1IiBmaWxsPSJsaWdodC1kYXJrKCMwMDAwMDAsICNmZmZmZmYpIiBmb250LWZhbWlseT0iSGVsdmV0aWNhIiBmb250LXNpemU9IjE2cHgiIHRleHQtYW5jaG9yPSJtaWRkbGUiPkYxICsgMjwvdGV4dD48L3N3aXRjaD48L2c+PC9nPjwvZz48ZyBkYXRhLWNlbGwtaWQ9IjEzIj48ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjUsMC41KSI+PHJlY3QgeD0iMTkxIiB5PSI4MCIgd2lkdGg9IjI1OSIgaGVpZ2h0PSI0MCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJub25lIiBwb2ludGVyLWV2ZW50cz0iYWxsIi8+PHBhdGggZD0iTSAxOTEgODAgTSA0NTAgODAgTSA0NTAgMTIwIE0gMTkxIDEyMCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMDAwMDAwIiBzdHJva2UtbGluZWNhcD0ic3F1YXJlIiBzdHJva2UtbWl0ZXJsaW1pdD0iMTAiIHBvaW50ZXItZXZlbnRzPSJhbGwiIHN0eWxlPSJzdHJva2U6IGxpZ2h0LWRhcmsocmdiKDAsIDAsIDApLCByZ2IoMjU1LCAyNTUsIDI1NSkpOyIvPjwvZz48Zz48Zz48c3dpdGNoPjxmb3JlaWduT2JqZWN0IHN0eWxlPSJvdmVyZmxvdzogdmlzaWJsZTsgdGV4dC1hbGlnbjogbGVmdDsiIHBvaW50ZXItZXZlbnRzPSJub25lIiB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiByZXF1aXJlZEZlYXR1cmVzPSJodHRwOi8vd3d3LnczLm9yZy9UUi9TVkcxMS9mZWF0dXJlI0V4dGVuc2liaWxpdHkiPjxkaXYgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGh0bWwiIHN0eWxlPSJkaXNwbGF5OiBmbGV4OyBhbGlnbi1pdGVtczogdW5zYWZlIGNlbnRlcjsganVzdGlmeS1jb250ZW50OiB1bnNhZmUgY2VudGVyOyB3aWR0aDogMjU3cHg7IGhlaWdodDogMXB4OyBwYWRkaW5nLXRvcDogMTAwcHg7IG1hcmdpbi1sZWZ0OiAxOTJweDsiPjxkaXYgc3R5bGU9ImJveC1zaXppbmc6IGJvcmRlci1ib3g7IGZvbnQtc2l6ZTogMDsgdGV4dC1hbGlnbjogY2VudGVyOyBtYXgtaGVpZ2h0OiAzNnB4OyBvdmVyZmxvdzogaGlkZGVuOyBjb2xvcjogIzAwMDAwMDsgIj48ZGl2IHN0eWxlPSJkaXNwbGF5OiBpbmxpbmUtYmxvY2s7IGZvbnQtc2l6ZTogMTZweDsgZm9udC1mYW1pbHk6IEhlbHZldGljYTsgY29sb3I6IGxpZ2h0LWRhcmsoIzAwMDAwMCwgI2ZmZmZmZik7IGxpbmUtaGVpZ2h0OiAxLjI7IHBvaW50ZXItZXZlbnRzOiBhbGw7IHdoaXRlLXNwYWNlOiBub3JtYWw7IHdvcmQtd3JhcDogbm9ybWFsOyAiPjxmb250IHN0eWxlPSJmb250LXNpemU6IDE0cHg7Ij5WdWUgVkZSIENDQTwvZm9udD48L2Rpdj48L2Rpdj48L2Rpdj48L2ZvcmVpZ25PYmplY3Q+PHRleHQgeD0iMzIxIiB5PSIxMDUiIGZpbGw9ImxpZ2h0LWRhcmsoIzAwMDAwMCwgI2ZmZmZmZikiIGZvbnQtZmFtaWx5PSJIZWx2ZXRpY2EiIGZvbnQtc2l6ZT0iMTZweCIgdGV4dC1hbmNob3I9Im1pZGRsZSI+VnVlIFZGUiBDQ0E8L3RleHQ+PC9zd2l0Y2g+PC9nPjwvZz48L2c+PC9nPjxnIGRhdGEtY2VsbC1pZD0iMjQiPjxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuNSwwLjUpIi8+PGcgZGF0YS1jZWxsLWlkPSIyNSI+PGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC41LDAuNSkiPjxyZWN0IHg9IjAiIHk9IjEyMCIgd2lkdGg9IjE5MSIgaGVpZ2h0PSI0MCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJub25lIiBwb2ludGVyLWV2ZW50cz0iYWxsIi8+PHBhdGggZD0iTSAwIDEyMCBNIDE5MSAxMjAgTSAxOTEgMTYwIE0gMCAxNjAiIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLWxpbmVjYXA9InNxdWFyZSIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiBwb2ludGVyLWV2ZW50cz0iYWxsIiBzdHlsZT0ic3Ryb2tlOiBsaWdodC1kYXJrKHJnYigwLCAwLCAwKSwgcmdiKDI1NSwgMjU1LCAyNTUpKTsiLz48L2c+PGc+PGc+PHN3aXRjaD48Zm9yZWlnbk9iamVjdCBzdHlsZT0ib3ZlcmZsb3c6IHZpc2libGU7IHRleHQtYWxpZ246IGxlZnQ7IiBwb2ludGVyLWV2ZW50cz0ibm9uZSIgd2lkdGg9IjEwMCUiIGhlaWdodD0iMTAwJSIgcmVxdWlyZWRGZWF0dXJlcz0iaHR0cDovL3d3dy53My5vcmcvVFIvU1ZHMTEvZmVhdHVyZSNFeHRlbnNpYmlsaXR5Ij48ZGl2IHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hodG1sIiBzdHlsZT0iZGlzcGxheTogZmxleDsgYWxpZ24taXRlbXM6IHVuc2FmZSBjZW50ZXI7IGp1c3RpZnktY29udGVudDogdW5zYWZlIGNlbnRlcjsgd2lkdGg6IDE4OXB4OyBoZWlnaHQ6IDFweDsgcGFkZGluZy10b3A6IDE0MHB4OyBtYXJnaW4tbGVmdDogMXB4OyI+PGRpdiBzdHlsZT0iYm94LXNpemluZzogYm9yZGVyLWJveDsgZm9udC1zaXplOiAwOyB0ZXh0LWFsaWduOiBjZW50ZXI7IG1heC1oZWlnaHQ6IDM2cHg7IG92ZXJmbG93OiBoaWRkZW47IGNvbG9yOiAjMDAwMDAwOyAiPjxkaXYgc3R5bGU9ImRpc3BsYXk6IGlubGluZS1ibG9jazsgZm9udC1zaXplOiAxNnB4OyBmb250LWZhbWlseTogSGVsdmV0aWNhOyBjb2xvcjogbGlnaHQtZGFyaygjMDAwMDAwLCAjZmZmZmZmKTsgbGluZS1oZWlnaHQ6IDEuMjsgcG9pbnRlci1ldmVudHM6IGFsbDsgd2hpdGUtc3BhY2U6IG5vcm1hbDsgd29yZC13cmFwOiBub3JtYWw7ICI+PGZvbnQgc3R5bGU9ImZvbnQtc2l6ZTogMTRweDsiPkYxICsgMzwvZm9udD48L2Rpdj48L2Rpdj48L2Rpdj48L2ZvcmVpZ25PYmplY3Q+PHRleHQgeD0iOTYiIHk9IjE0NSIgZmlsbD0ibGlnaHQtZGFyaygjMDAwMDAwLCAjZmZmZmZmKSIgZm9udC1mYW1pbHk9IkhlbHZldGljYSIgZm9udC1zaXplPSIxNnB4IiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj5GMSArIDM8L3RleHQ+PC9zd2l0Y2g+PC9nPjwvZz48L2c+PGcgZGF0YS1jZWxsLWlkPSIyNiI+PGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC41LDAuNSkiPjxyZWN0IHg9IjE5MSIgeT0iMTIwIiB3aWR0aD0iMjU5IiBoZWlnaHQ9IjQwIiBmaWxsPSJub25lIiBzdHJva2U9Im5vbmUiIHBvaW50ZXItZXZlbnRzPSJhbGwiLz48cGF0aCBkPSJNIDE5MSAxMjAgTSA0NTAgMTIwIE0gNDUwIDE2MCBNIDE5MSAxNjAiIGZpbGw9Im5vbmUiIHN0cm9rZT0iIzAwMDAwMCIgc3Ryb2tlLWxpbmVjYXA9InNxdWFyZSIgc3Ryb2tlLW1pdGVybGltaXQ9IjEwIiBwb2ludGVyLWV2ZW50cz0iYWxsIiBzdHlsZT0ic3Ryb2tlOiBsaWdodC1kYXJrKHJnYigwLCAwLCAwKSwgcmdiKDI1NSwgMjU1LCAyNTUpKTsiLz48L2c+PGc+PGc+PHN3aXRjaD48Zm9yZWlnbk9iamVjdCBzdHlsZT0ib3ZlcmZsb3c6IHZpc2libGU7IHRleHQtYWxpZ246IGxlZnQ7IiBwb2ludGVyLWV2ZW50cz0ibm9uZSIgd2lkdGg9IjEwMCUiIGhlaWdodD0iMTAwJSIgcmVxdWlyZWRGZWF0dXJlcz0iaHR0cDovL3d3dy53My5vcmcvVFIvU1ZHMTEvZmVhdHVyZSNFeHRlbnNpYmlsaXR5Ij48ZGl2IHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hodG1sIiBzdHlsZT0iZGlzcGxheTogZmxleDsgYWxpZ24taXRlbXM6IHVuc2FmZSBjZW50ZXI7IGp1c3RpZnktY29udGVudDogdW5zYWZlIGNlbnRlcjsgd2lkdGg6IDI1N3B4OyBoZWlnaHQ6IDFweDsgcGFkZGluZy10b3A6IDE0MHB4OyBtYXJnaW4tbGVmdDogMTkycHg7Ij48ZGl2IHN0eWxlPSJib3gtc2l6aW5nOiBib3JkZXItYm94OyBmb250LXNpemU6IDA7IHRleHQtYWxpZ246IGNlbnRlcjsgbWF4LWhlaWdodDogMzZweDsgb3ZlcmZsb3c6IGhpZGRlbjsgY29sb3I6ICMwMDAwMDA7ICI+PGRpdiBzdHlsZT0iZGlzcGxheTogaW5saW5lLWJsb2NrOyBmb250LXNpemU6IDE2cHg7IGZvbnQtZmFtaWx5OiBIZWx2ZXRpY2E7IGNvbG9yOiBsaWdodC1kYXJrKCMwMDAwMDAsICNmZmZmZmYpOyBsaW5lLWhlaWdodDogMS4yOyBwb2ludGVyLWV2ZW50czogYWxsOyB3aGl0ZS1zcGFjZTogbm9ybWFsOyB3b3JkLXdyYXA6IG5vcm1hbDsgIj48Zm9udCBzdHlsZT0iZm9udC1zaXplOiAxNHB4OyI+QVZJU08gdGVycmFpbnMgY29udHLDtGzDqXMgZXQgQUZJUzwvZm9udD48L2Rpdj48L2Rpdj48L2Rpdj48L2ZvcmVpZ25PYmplY3Q+PHRleHQgeD0iMzIxIiB5PSIxNDUiIGZpbGw9ImxpZ2h0LWRhcmsoIzAwMDAwMCwgI2ZmZmZmZikiIGZvbnQtZmFtaWx5PSJIZWx2ZXRpY2EiIGZvbnQtc2l6ZT0iMTZweCIgdGV4dC1hbmNob3I9Im1pZGRsZSI+QVZJU08gdGVycmFpbnMgY29udHLDtGzDqXMgZXQgQUZJUzwvdGV4dD48L3N3aXRjaD48L2c+PC9nPjwvZz48L2c+PC9nPjwvZz48L2c+PC9nPjxzd2l0Y2g+PGcgcmVxdWlyZWRGZWF0dXJlcz0iaHR0cDovL3d3dy53My5vcmcvVFIvU1ZHMTEvZmVhdHVyZSNFeHRlbnNpYmlsaXR5Ii8+PGEgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMCwtNSkiIHhsaW5rOmhyZWY9Imh0dHBzOi8vd3d3LmRyYXdpby5jb20vZG9jL2ZhcS9zdmctZXhwb3J0LXRleHQtcHJvYmxlbXMiIHRhcmdldD0iX2JsYW5rIj48dGV4dCB0ZXh0LWFuY2hvcj0ibWlkZGxlIiBmb250LXNpemU9IjEwcHgiIHg9IjUwJSIgeT0iMTAwJSI+VGV4dCBpcyBub3QgU1ZHIC0gY2Fubm90IGRpc3BsYXk8L3RleHQ+PC9hPjwvc3dpdGNoPjwvc3ZnPg==
```

Ces profils sont spécialement conçus pour travailler sur une zone plus spécifique, avec un accès rapide aux vues radar et sol les plus utilisées.

### FIR / ASR

Regardons le contenu du dossier ASR.

### Dossier *Avisos*

Ce dossier contient les vues sol pour chaque aéroport contrôlé (tour) ou disposant d’un service AFIS.

> Les aérodromes non contrôlés ne sont pas inclus.
{.is-warning}


> L’affichage par défaut n’est pas toujours extensif, vérifiez l’affichage voulu dans *Other Sets > Display Settings*
{.is-warning}

### Dossier CCA ( *Centre de Contrôle d'Approche*)

Vous trouverez également un dossier dédié à certains CCA, contenant les vues radar spécifiques à cette zone.


### Dossier *Vues radar générales*

Ce dossier contient :
- une vue radar **UIR/FIR générale**
- une vue dite "**APP Legacy**" pour les zones qui ne disposent pas encore de vues spécifiques

### Dossier *Plugins*

Comme son nom l'indique, vous y trouverez tous les plugins utilisés dans le pack.

> Chaque plugin possède son propre dossier
{.is-warning}

Donc, chaque dossier de plugin contient uniquement ses propres fichiers de configuration.

### Dossier *Settings*
#### Fichier *General.txt*

Ce fichier contient les réglages généraux d'Euroscope

#### Fichier *List.txt*

Contient toutes les listes (start-up, départs, sector inbound, etc.)

> CoFrance dispose maintenant de ses propres listes *Sector Inbound* et *Sector Exit*. Elles sont donc par défaut désactivées.
{.is-warning}

#### Fichier *LoginProfiles.txt*

 Contient toutes les positions spécifiques au pack FIR que vous êtes en train d'installer.
 
#### Fichier *Plugins.txt*

Contient les réglages du plugin Timer d’Euroscope et du code Hoppie (vSMR CPDLC), ainsi que ceux des autres plugins installés.

#### Fichier *Screen.txt*

Pour définir la position des différentes listes à l’écran.

#### Fichier *Symbology.txt*

Contient les réglages de symbologie (couleurs, affichage, etc.)

#### Fichier *Tags.txt*

Contient les réglages des tags.

> CoFrance sait maintenant gérer les étiquettes nativement. Un fichier de tag vide est inclus.
{.is-info}

#### Fichier *VCCS.txt*

Contient les paramètres du système VCCS

#### Fichier *VoiceChannels.txt*

Contient toutes les fréquences spécifiques à la FIR auquel est rattaché le fichier.


## Mise à jour du cycle AIRAC
### Cycle AIRAC
Tous les 28 jours, les données aéronautiques sont mises à jour selon ce que l'on appelle des cycles AIRAC (Aeronautical Information Regulation And Control).

Dès qu'une mise à jour est disponible, le Département Nav de French vACC notifie les membres sur le serveur Discord dans le canal `#atc-updates`.

### Comment mettre à jour les packs?

#### Méthode 1 (automatique)

Pour mettre à jour vos packs contrôleur, téléchargez le pack **LFXX-CoFrance-Base-Update** ainsi que tous les **Update-Packages** des FIR concernées.

Lancez l'[Installer.exe](https://github.com/vaccfr/Sector-Files/releases) téléchargé plus tôt dans ce tutoriel.

> Assurez-vous de lancer l'installeur depuis l’emplacement où vos packs contrôleur sont déjà installés.
{.is-warning}

Une fois ouvert :
**1)** Cliquez sur **Install/Update Packages**
**2)** Sélectionnez tous les packages de mise à jour (6 au total si vous souhaitez tout mettre à jour)
**3)** Une fois tous les packages sélectionnés, cliquez sur **Update Controller Pack from GitHub + GNG**

![update_airac.png](/update_airac.png){.align-center}

L’installer mettra automatiquement à jour vos packs contrôleur. Aucune autre action n'est nécessaire !

#### Méthode 1 (manuelle)

À chaque cycle AIRAC, un Update-Package sera publié contenant uniquement les fichiers nécessaires pour maintenir votre installation à jour, notamment :
- Les fichiers .sct / .ese mis à jour contenant les dernières NavData et positions ATC des FIR françaises
 → Ces fichiers doivent être placés dans le dossier LFXX/Sector
- Les fichiers FIR/ICAO et FIR/NavData mis à jour
- Les fichiers LFXX/Settings ou FIR/Settings mis à jour, tels que :
 → LoginProfiles.txt
 → VoiceChannels.txt

D’autres fichiers pourront occasionnellement être inclus si nécessaire, et cela sera toujours clairement précisé dans l’annonce AIRAC sur Discord.

📢 **Chaque annonce contiendra** :
- Un résumé des changements principaux
- Un changelog complet et détaillé pour les utilisateurs souhaitant consulter l’ensemble des modifications


# CoFrance

CoFrance est le plugin principal du pack qui simule un environnement contrôleur réaliste

Vous entendrez souvent parler de “pack CoFrance” car il s’agit d’un radar pré-configuré avec un ensemble de vues et de fichiers déjà en place pour vous faciliter l’installation. CoFrance a été développé par French vACC et dispose d’un ensemble de fonctionnalités permettant de simuler un environnement au plus proche du réel, avec ce que Euroscope permet de faire.

CoFrance est riche en fonctionnalités. Prenez le temps d'en lire le manuel et n'hésitez pas si vous avez des questions quant à son utilisation.

Vous trouverez le manuel de CoFrance [ici](https://github.com/vaccfr/CoFrance-v2/blob/main/CoFranceUserManual.pdf).

![user_manual_thumb.png](/user_manual_thumb.png){.align-center}

# Track Audio

Track Audio est le logiciel qui vous permettra d'entendre et de communiquer avec les pilotes.

> Euroscope ne disposant pas de client audio intégré, il est important que vous téléchargiez Track Audio.
{.is-info}


> Audio for VATSIM est voué à être mis à l'arrêt. Le logiciel à utiliser est Track Audio.
{.is-warning}


## Téléchargement et installation

- Rendez-vous sur sur [ce lien](https://github.com/pierr3/TrackAudio) et **téléchargez la dernière version du logiciel** dans l'onglet Releases.

![track_audio_github.png](/track_audio_github.png =20%x){.align-center}

- Suivez le processus d'installation et lancez Track Audio.

![track_audio_1.png](/track_audio_1.png =40%x){.align-center}

- Une fois TrackAudio lancé, vous devriez voir la fenêtre ci-dessus s'ouvrir. Cliquez sur le bouton `Settings`, la roue dentée située en haut du logiciel comme indiqué sur la capture précédente. Rentrez votre CID et votre mot de passe VATSIM :

![track_audio_1.png](/track_audio_2.png =20%x){.align-center}

- Sélectionnez vos paramètres de micro et casque. Un micro de qualité correcte est vivement recommandé :

![track_audio_1.png](/track_audio_3.png =20%x){.align-center}

- Activez ensuite les effets radio pour la VHF :

![track_audio_1.png](/track_audio_4.png =20%x){.align-center}

- Pour le type de rendu son, nous vous proposons le `Rockwell Collins` mais aurez peut être votre préférence ! Sélectionnez une touche à utiliser en tant que “**push-to-talk**”:

![track_audio_1.png](/track_audio_5.png =20%x){.align-center}

C’est ce bouton que vous utiliserez pour parler aux pilotes lors de vos sessions de contrôle, **veillez à ce qu’il ne soit pas utilisé par une autre application**.

Pour vous assurer d’être audible et que l’on vous entende avec un volume ni trop fort ni trop faible, vous pouvez lancer un test en cliquant sur `Start mic test`. Si tout va bien, la jauge devrait être dans le vert.

Vous pouvez appliquer les changements et cliquer sur OK.

# Conclusion

Félicitations, vous disposez désormais de tous les outils pour contrôler. Pour s'assurer que tout fonctionne, quoi de mieux que de réaliser quelques sessions d'observation ?

Rendez-vous sur [cette page](https://doc.vatsim.fr/fr/connect-as-obs) où nous vous expliquons comment faire et vous donnons également quelques informations supplémentaires sur CoFrance.

Bon apprentissage et bonnes sessions de contrôle !