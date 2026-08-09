---
title: LFLL - Lyon Saint-Exupéry
description: SOP LFLL
published: true
date: 2026-07-11T11:59:18.662Z
tags: 
editor: markdown
dateCreated: 2026-02-27T11:51:10.535Z
---

# Introduction
This manual will enable you to familiarise yourself with the different positions at Lyon Saint-Exupéry: DEL, GND, TWR and APP. If in doubt, please contact the training team.

## Disclaimer
Although our aim is to provide control services as close to reality as possible, certain real-life practices are not adapted to the networked simulation environment, even on VATSIM. In this respect, it is important to be able to adapt to :

- the level of the pilots (which can vary from beginners to the most experienced)
- the specific limitations of each simulator/aircraft (flight model, low-noise procedures, etc)
- the limits of our tools: even if there are few of them, our radars are still less efficient than our real-life colleagues.

> Reminder: This document is for the use of VATSIM controllers and is therefore exclusively reserved for simulation.
{.is-warning}

You should ensure that you have the necessary knowledge to open this platform. This manual has been written to provide you with additional information but cannot replace the AIP available on the <a href="https://www.sia.aviation-civile.gouv.fr" target="_blank">SIA</a> website.

# General
The airport has 2 runways running North/South.
The airport has 3 terminals and 3 aprons:
- Terminal 1 is round to the south,
- Terminal 2 is wave-shaped and has a closed satellite section to the north,
- Terminal 3 offshore between the TL and TJ tracks,
- Cargo & general/business aviation:<br>Apron M (Cargo, oversize etc.) / N (Business) / G (CAG).

![lfll-adc01.png](/doc-atc/lfll-adc01.png)

# Use of CDM
The use of CDM (Collaborative Decision Making) is permitted at LFLL. Before opening a position at Lyon Saint-Exupéry, we strongly recommend reviewing the dedicated MANEX in the Documentation section of the French vACC website.

# Control positions
## Summary

|Indicatif|Découpe|Fréquence|Indicatif d'appel|
|:-:|:-:|:-:|:-:|
|LFLL_DEL| |121.655|Saint-Ex Prévol<br>*Saint-Ex Delivery*|
|LFLL_GND| |121.830|Saint-Ex Sol<br>*Saint-Ex Ground*|
|LFLL_TWR| |120.450|Saint-Ex Tour<br>*Saint-Ex Tower*|
|LFLL_DEP| |131.315|Lyon Départ<br>*Lyon Departure*|
|LFLL_APP| |120.230|Lyon Approche<br>*Lyon Approach*|
| |LFLL_E_APP|136.075|Lyon Approche<br>*Lyon Approach*|

## Delivery
### Departures

Departure procedures are allocated as follows:

|QFU|17|35|
|:-:|:-:|:-:|
|SID (RNAV)|#S|#N|
|Initial Climb|FL70 (except props)||

Omnidirectional departures are published and must be coordinated with the Approach controler.

### Particularities
ASLEG, GEMLA, LUKUM, MADOT, MTL, PIMAK and VEROT departures are reserved for props and prohibited in the 2200-0600LT* slot. These departures initially climb to 5000ft.

*This restriction cannot be imposed to VATSIM pilots and is therefore not mandatory.

### Strategy during VATSIM events
In order to limit the amount of traffic on the GND frequency (due to the impossibility of splitting this frequency), the best practice is to keep them on the DEL frequency until the traffic is ready to push back. This avoids saturating the ground position frequency.

## Ground
### Taxi
It is recommended giving priority to traffic leaving the apron by having it join taxiway T as directly as possible. It is better to maintain a single direction of traffic on T.

Please see below the parking stand allocation based on airline and/or aircraft type: 

|Parkings|A?C Type|Remark(s)|
|:-:|:-:|:-:|
|B, C et D|Heavys|Ending with B except B12|
|L and J|low-cost carriers|Transavia, EasyJet, etc|
|M, J11 to J19|Freight|ASL, DHL, etc|

Additional information: 
- E, G, N, M12, C19, A30 et A31 are remote stands.
- N1# stands are accessible via TN1, N2# and N3# via TN2, N4# via TN3.
- Cat F aircrafts (AN124, A380, B748, etc.) access the apron via TJ and TL only.
 

### Holding points
Take-offs from runway 35L are made from holding point A9 at the end of the runway or from A8 at the pilot's request or if this represents an operational advantage. In the event of a heavy load, it is preferable to use A9. On runway 17R, the default intersection is A3 unless requested by the pilot.

In LVP conditions, only the following CAT II/III holding points can be used:
- A9 and A8 for 35L alignment
- B9 for aligning in 35R
- B4 and B3 to cross the 35L after landing in 35R.


## Tower
### Preferred configuration
Runway 35 configuration is preferred due to instrumental procedures.

To ensure the airport's maximum capacity, the runways are operated as follows:
- runways 35R/17L preferred for landings.
- runways 35L/17R preferred for take-offs.

### Departure / arrival rates
The maximum capacity is 48 movements per hour, i.e. ~1m15s between each movement, including arrivals and departures. As the platform is A-CDM capable, the optimal rate of the CDM is 6 departures every 10 minutes.

### Runway management 
Runway use in Lyon is highly weather-dependent. With more details:

- In IMC : runways are considered <u>inter</u>dependent.
- In VMC : runways are considered independent except if: 
  - Go-around caused by too strong a crosswind (restart 10min after last occurrence)
  - Windshear reported (same as above)
  - RCC of any runway ≤ 4 (resume when RCC ≥ 5 on both runways)
  - VOR/DME or LOC arrival.

*VMC minimas : visibility ≥5000m & ceiling ≥1500ft.
**RCC : Runway Condition Code

### VFR
Traffic pattern is 1800ft East of the airport regardless of the runway configuration used. Beware of the proximity between runways and the downwind.
Departure and arrival routes are published, see the VAC map for full information.

### Overall management 
Lyon Saint-Exupéry has LVP procedures.
They must be in force at the latest when: RVR = 550m or ceiling = 200ft.

Only runways 35R and 35L have CAT II & III approaches and are approved for low-visibility take-offs with the following use restrictions : 
- vacating RWY 35L via A3 or A4,
- vacating RWY 35R via B3, B4 or V4; vacating via V5 prohibited.

## Approach
### Split	
Approach position can be split with an additional position (_E_APP) which opens up the eastern part of the TMA (opposite) and a departure (_DEP).

West approach (_APP) handles arrivals via TALAR & ARBON and interceptions on the ILS. The East approach (_E_APP) handles departures (if _DEP is not present) and arrivals via RIPTU and GOMET.

Transfer to the West approach (_APP) is made as soon as possible on a downwind or equivalent if possible, traffic must be descending towards 5000ft, limited to 220 kts and non-conflicting.

The following airports welcome IFR trafic and are under the responsibility of Lyon Approach: 

|ICAO|Name|Responsability||
|:-:|:-:|:-:|:-:|
|LFLY|Lyon Bron|Always||
|LFLS|Grenoble Isère|Always||
|LFLB|Chambéry|See below||
| | |LFLB_APP|Transfert before GOVNA|
| | |LFMM_CTR|On coordination|
| | |UNICOM|If trafic load doesn't permit topdown|

As far as VFR traffic management is concerned, a FIS covers the region from the surface up to flight level 115 (FIS 2 and 3). Part of the FIS is above neighbouring TMA/FIS. Some floors are different: FIS 1 has a floor at FL85 (on the Clermont side) and FISs 4 and 5 at FL95 (on the Chambéry side).

### STAR
STARs are given by the en-route controler as follows: S for QFU 17, N for QFU 35.
IAFs are common to both runway configurations.

|QFU|17|35|
|:-:|:-:|:-:|
|STAR / APP INI|S|N|
|IAF|TALAR, RIPTU, ARBON, GOMET||

### Reduced radar separation on final
The minimum radar separation of 3 NM may be reduced to 2.5 NM between two aircraft on final approach 17L or 35R when the preceding aircraft belongs to a wake turbulence category smaller than or equal to the category of the following aircraft. This reduction should not have to be systematic, but remains possible to avoid the need for a go-around.

### Go-around
Go-arounds must be executed as published or coordinated with the approach controller.

