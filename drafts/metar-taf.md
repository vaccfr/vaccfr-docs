---
title: METAR et TAF
description: Décrire les messages
published: true
date: 2026-08-09T15:10:49.247Z
tags: 
editor: markdown
dateCreated: 2026-02-27T22:02:12.327Z
---

# Décryptage du METAR et du TAF

**On appelle METAR**, le Message d'observation d'aérodrome (Meteorological Aerodrome Report). Il se compose de paramètres estimés (visibilité, nébulosité) et de paramètres mesurés (Pression atmosphérique, vent). Il est rédigé systématiquement toutes les heures ou demi-heures.

**On appelle TAF**, le Message de prévision d'aérodrome (Terminal Aerodrome Forecast). Il est rédigé systématiquement toutes les 3 heures. Il décrit le temps prévu sur l'aérodrome pour une durée de 9 heures (TAF court) ou 18 heures (TAF long). Sa structure est la même que celle du METAR.

## Codage des messages météorologiques

### Les particularités

Certains groupes ne sont présents que dans des conditions particulières, ou sont propres à l'un des deux messages :

- **CAVOK** (Ceiling And Visibility OK) : remplace les groupes visibilité, portée visuelle de piste, temps présent et nébulosité lorsque simultanément : visibilité ≥ 10 km, aucun nuage en dessous de 5 000 ft (ou en dessous de l'altitude minimale de secteur si supérieure) et absence de Cb/TCu, absence de phénomène météorologique significatif.
- **RMK** : groupe de remarques, propre à certains pays (notamment l'usage nord-américain), placé en fin de message.
- **NSC** (No Significant Cloud) et **NSW** (No Significant Weather) : utilisés en TAF pour indiquer l'absence de nébulosité ou de phénomène significatif prévu.
- **NIL** : message non disponible (absence d'observation ou de prévision).
- **AMD** (Amended) : TAF amendé, publié en dehors du cycle normal pour corriger une prévision devenue caduque.
- **COR** (Corrected) : message corrigé après une erreur de codage.
- **AUTO** : indique que le message provient d'une observation entièrement automatique, sans intervention humaine.

---

## Structure générale du message

Un METAR/TAF s'articule toujours dans le même ordre :

1. Type de message (METAR / METAR AUTO / SPECI / TAF)
2. Indicatif OACI de l'aérodrome (4 lettres, ex : LFPG)
3. Date et heure de l'observation (ou d'émission pour le TAF) au format **jjhhmmZ**
4. Vent
5. Visibilité horizontale
6. Portée Visuelle de Piste (RVR) si applicable
7. Temps présent (phénomènes significatifs)
8. Nébulosité (ou CAVOK)
9. Température et point de rosée (absent en TAF)
10. Calage altimétrique (QNH)
11. Évolution prévue (tendance en METAR, groupes de changement en TAF)

---

## Détail des groupes

### 1. Type de message

| Code | Signification |
|---|---|
| METAR | Observation régulière, horaire ou semi-horaire |
| METAR AUTO | Observation automatique sans contrôle humain |
| SPECI | Observation spéciale, émise hors cycle suite à un changement significatif |
| TAF | Prévision d'aérodrome |

### 2. Date et heure

Format **jjhhmmZ** : jour du mois (2 chiffres), heure et minutes en UTC (temps universel, indiqué par le Z, dit "Zulu").

Exemple : `091530Z` = le 9 du mois, à 15h30 UTC.

### 3. Le vent

Format **dddffGfmaxKT** (ou MPS/KMH selon les pays) :

- **ddd** : direction du vent en degrés vrais (arrondie à la dizaine), par rapport au nord géographique
- **ff** : force du vent moyennée sur 10 minutes
- **G fmax** : rafales (Gust), si l'écart entre vent moyen et vent instantané dépasse 10 kt
- **KT** : unité (nœuds, standard OACI ; MPS = mètres/seconde, KMH = km/h selon les pays)
- **VRB** : vent variable en direction (utilisé quand la direction n'est pas stable, en général pour des vents faibles < 3 kt)
- Un groupe complémentaire **dddVddd** peut indiquer l'amplitude de variation de la direction quand elle dépasse 60° pour des vents > 3 kt

Exemple : `27015G25KT` = vent du 270° (Ouest), 15 kt, rafales à 25 kt.

### 4. La visibilité

Exprimée en mètres (jusqu'à 5000 m par pas de 50 m, puis par pas de 100 m jusqu'à 9999 m qui signifie "10 km ou plus") ou en milles terrestres (SM) selon les pays (usage nord-américain).

- **9999** : visibilité ≥ 10 km
- Une visibilité directionnelle minimale peut être ajoutée si elle diffère significativement de la visibilité dominante.

### 5. La Portée Visuelle de Piste (RVR)

Format **Rpp/vvvvFT** ou **Rpp/vvvv** :

- **pp** : numéro de piste concernée
- **vvvv** : portée visuelle en mètres
- Un indicateur de tendance peut être ajouté : **U** (Upward, en hausse), **D** (Downward, en baisse), **N** (No change, stable)

La RVR n'est reportée que lorsque la visibilité ou la RVR elle-même est inférieure à 1500 m.

### 6. Le temps présent (phénomènes significatifs)

Codé par la combinaison d'un descripteur d'intensité/proximité, d'un descripteur du phénomène, et du phénomène lui-même.

![metar_array.png](/metar_array.png)

Exemple : `+TSRA` = orage fort avec pluie ; `-SHSN` = faibles averses de neige ; `VCFG` = brouillard au voisinage.

### 7. La nébulosité

Format **NNNhhh(CB/TCU)**, répété pour chaque couche significative (jusqu'à 4 en général) :

**Quantité (NNN), en octas :**

| Code | Octas | Signification |
|---|---|---|
| SKC / CLR | 0 | Ciel clair |
| FEW | 1-2 | Quelques nuages |
| SCT | 3-4 | Épars (Scattered) |
| BKN | 5-7 | Fragmenté (Broken) |
| OVC | 8 | Couvert (Overcast) |

- **hhh** : altitude de la base en centaines de pieds (ex : 020 = 2000 ft)
- **CB** : Cumulonimbus, **TCU** : Towering Cumulus (indiqués si présents, en raison de leur intérêt pour la sécurité des vols)
- **VV** suivi d'un code à 3 chiffres : visibilité verticale, utilisée quand le ciel est obscurci (ciel invisible, ex. brouillard épais)

### 8. Température et point de rosée

Format **TT/TdTd**, en degrés Celsius entiers, séparés par une barre oblique. Un **M** précède les valeurs négatives (Minus).

Exemple : `18/12` = température 18°C, point de rosée 12°C. `M02/M05` = -2°C / -5°C.

### 9. Le calage altimétrique (QNH)

Format **Qpppp** (hectopascals, standard OACI) ou **Ainnn** (pouces de mercure, usage nord-américain).

Exemple : `Q1013` = QNH 1013 hPa. `A2992` = QNH 29.92 inHg.

### 10. Groupe de tendance (METAR) et groupes d'évolution (TAF)

**En METAR**, une tendance à court terme (2h) peut être ajoutée en fin de message :

| Code | Signification |
|---|---|
| NOSIG | Pas de changement significatif attendu |
| BECMG | Évolution progressive attendue (Becoming) |
| TEMPO | Fluctuations temporaires attendues |

**En TAF**, les évolutions prévues sont codées ainsi :

| Code | Signification |
|---|---|
| BECMG hhhh/hhhh | Changement progressif et durable entre les deux heures indiquées |
| TEMPO hhhh/hhhh | Fluctuations temporaires (< 1h à la fois, < 50% de la période) durant l'intervalle |
| FM hhhhmm | Changement rapide et net à partir de l'heure indiquée (From) ; réinitialise le message qui suit |
| PROB30 / PROB40 | Probabilité (30% ou 40%) d'occurrence d'une évolution, souvent associée à TEMPO |

Exemple : `TEMPO 1214/1218 4000 TSRA BKN008CB` = entre 12h et 18h le jour 14, possibilité temporaire de visibilité réduite à 4000 m, orage avec pluie, et une couche fragmentée de Cumulonimbus à 800 ft.

---

## Exemples décodés

### Exemple METAR

```
METAR LFPG 091530Z 27015G25KT 240V300 9999 FEW030 SCT100 18/12 Q1013 NOSIG=
```

- **LFPG** : Paris Charles de Gaulle
- **091530Z** : observation du 9 à 15h30 UTC
- **27015G25KT** : vent du 270°, 15 kt, rafales à 25 kt
- **240V300** : direction variable entre 240° et 300°
- **9999** : visibilité ≥ 10 km
- **FEW030** : quelques nuages à 3000 ft
- **SCT100** : nuages épars à 10 000 ft
- **18/12** : température 18°C, point de rosée 12°C
- **Q1013** : QNH 1013 hPa
- **NOSIG** : pas d'évolution significative attendue

### Exemple TAF

```
TAF LFPG 091100Z 0912/1018 26012KT 9999 SCT025
  BECMG 0915/0917 22008KT
  TEMPO 1000/1006 4000 BR BKN006
  PROB30 TEMPO 1006/1010 1000 FG VV002=
```

- Émis le 9 à 11h00 UTC, valable du 9 à 12h UTC au 10 à 18h UTC
- Vent initial du 260°, 12 kt, visibilité ≥ 10 km, nuages épars à 2500 ft
- Évolution progressive entre 15h et 17h le jour 9 vers un vent du 220°, 8 kt
- Fluctuations temporaires entre 00h et 06h le jour 10 : visibilité 4000 m, brume, plafond fragmenté à 600 ft
- 30% de probabilité, entre 06h et 10h le jour 10, de brouillard dense (visibilité 1000 m) avec ciel obscurci et visibilité verticale à 200 ft

---

## Points clés à retenir

- Le METAR **observe**, le TAF **prévoit** : leur structure de codage est identique, seules les significations des groupes de fin diffèrent (tendance vs. évolution).
- L'heure est **toujours exprimée en UTC** (Zulu), jamais en heure locale.
- **CAVOK** simplifie le message quand les conditions sont bonnes sur tous les critères simultanément.
- Les groupes **BECMG**, **TEMPO**, **FM** et **PROB** structurent l'évolution temporelle du TAF et sont essentiels pour l'analyse du risque météorologique en préparation de vol.
- La présence de **CB** ou **TCU** dans la nébulosité doit toujours attirer l'attention, en raison des risques associés (turbulence, cisaillement, grêle, givrage).