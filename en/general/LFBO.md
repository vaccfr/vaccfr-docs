---
title: LFBO - Toulouse Blagnac
description: 
published: true
date: 2026-03-18T21:55:38.499Z
tags: 
editor: markdown
dateCreated: 2026-02-27T21:02:36.394Z
---

# General overview
## General information
Toulouse-Blagnac is one of the most important airports in terms of traffic. It is the sixth largest international airport in France and a key hub in Europe. It is located in the north-west of Toulouse, serving the Occitanie region. The airport is also home to Airbus Industries, making it a major center for the aerospace industry.
## Charts
The use of charts is strongly recommended for any pilot flying to or from TLS. Multiple updated versions of these charts are available from the following sources :
- <a href="https://www.sia.aviation-civile.gouv.fr/" target="_blank"> SIA (French eAIP)</a>
- <a href="https://chartfox.org/LFBO" target="_blank">ChartFox (French eAIP)</a>
- Navigraph / Jeppesen / NavDataPro / etc... (paywares)
## Sceneries
There are many sceneries adapted for different simulators for TLS; some of them are free and others are not. To help you find the correct one for your need, we provided you a list of available and/or recommended sceneries.

|Simulator|Editor|Link|Additional Information|
|:-:|:-:|:-:|:-:|
|P3D|Flightbeam|<a href="https://secure.simmarket.com/flightbeam-studios-lfbo-toulouse-blagnac-airport-p3d4-5.phtml" target="_blank">SimMarket</a>|Payware, resource consuming|
|X-Plane 11/12|Totish|<a href="https://x-plane.to/file/1582/toulouse-blagnac-airport-lfbo" target="_blank">X-Plane.to</a>|Freeware|
|MSFS 2020/2024|Flightbeam|<a href="https://shop.flightbeam.net/products/flightbeam-lfbo-msfs" target="_blank">Flightbeam Shop</a>|Payware, <a href="https://flightsim.to/addon/61596/lfbo-gsx-profile-flightbeam" target="_blank">GSX Profile</a>|

## ATS positions and frequencies
> Be aware that some changes (callsign, frequency or areas of responsibility) may occur
{.is-info}

|Position|Split (if applicable)|Frequency|Callsign|
|:-:|:-:|:-:|:-:|
|LFBO_DEL| |121.705|Blagnac Prévol<br>*Blagnac Delivery*|
|LFBO_GND| |121.900|Blagnac Sol<br>*Blagnac Ground*|
|LFBO_TWR| |118.100|Blagnac Tour<br>*Blagnac Tower*|
|LFBO_APP| |129.305|Toulouse Approache<br>*Toulouse Approach*|
| |LFBO_W_APP|121.105|Toulouse Approache<br>*Toulouse Approach*|
| |LFBO_E_APP|125.180|Toulouse Approache<br>*Toulouse Approach*|


|Position|Split (if applicable)|Frequency|Callsign|
|:-:|:-:|:-:|:-:|
|LFBB_CTR| |125.105|Bordeaux Contrôle<br>*Bordeaux Control*|
| |LFBB_UN_CTR|118.430|Bordeaux Contrôle<br>*Bordeaux Control*|
| |LFBB_US_CTR|136.040|Bordeaux Contrôle<br>*Bordeaux Control*|

## Clearance request, pushback and taxi
### General overview
Toulouse Blagnac airport has 2 terminals, 1 general aviation apron, 2 remote stands aprons, a freight apron and 2 Airbus Industries apron : 
- Blagnac 1 - business aviation (A,B,C), Blagnac 2 (E, U, V)
- Apron G (General aviation)
- Apron D, F
- Apron St MARTIN LAGARDERE, ST MARTIN (ZIEGLER (delivery center), BELUGA, VENDÉE(delivery center), MORVAN, QUERCY, LANDES, PYRENEES)

![adc-bo.png](/doc-atc/adc-bo.png)

### Clearance request
Delivery is responsible for issuing IFR clearances. During times of high traffic load, the use of **CDM** (Collaborative Decision Making) to optimize the sequence will be **announced via the ATIS**. 
When CDM is in operation, pilots are requested to send a **TOBT** (Target Off-Block Time = time at which they will be ready for pushback) at : <a href="https://cdm.vatsim.fr" target="_blank">https://cdm.vatsim.fr</a>.
This will ensure better departure sequence planning.  In order to participate in major events like Cross The Land, pilots have to **book a slot**, in this case a CTOT (CTOT = Calculated Take Off Time).

All pilots are expected to make contact with Delivery as soon as possible to get their IFR clearance along with their Start-Up Approval Time, also called **TSAT** (= Target Start-up Approval Time).

Example :
- ATC :  “AFR123, cleared to Doha, PILUL1W departure, runway 24, initial flight level 80, squawk 5624”
- Pilot : “cleared to Doha, PILUL1W departure, runway 24, initial flight level 80, squawk 5624, AFR123”
- ATC : “correct, TSAT 1020z, report ready”

“TSAT 1020Z” means that you as a pilot can expect start up/push back approval at the mentioned time.

We strongly recommend you to get your clearance via datalink in order to get a PDC message directly in your aircraft and avoid frequency congestion.

### Pushback and Engine Start-Up 
To ensure a smooth experience, all pilots have an **engine start-up/pushback window** defined as {TSAT-5, TSAT+5} that they have to comply with in order to be on time with their slots.

All pilots are expected to be ready for pushback and inform the DEL controller **at least 10 minutes prior to their TSAT**, failure to do so may lead to a slot loss and very long delays.

The controller will give you a pushback direction if needed and transfer you to GND at the appropriate time.

On **first contact** with the ground controller, make sure to state your stand number. At the appropriate time, the controller will issue a Start-Up or Pushback clearance that you have to **comply with within 2 minutes**. Failure to do so will cancel your pushback clearance and you may lose your slot.

### Summary : Actions to do when you connect

|Steps|When|What to do|
|:-:|:-:|:-:|
|1|at connexion|Enter the time you will be ready for pushback (TOBT) here : <a href="https://cdm.vatsim.fr" tagret="_blank">cdm.vatsim.fr</a>|
|2|as soon as possible|**Ask for your IFR clearance**<br>=> you will be given your assigned pushback time (TSAT)|
|3|at TSAT - 10 minutes|**Call Delivery and inform that you are ready for pushback**<br>=> you will be transferred to Ground|
|4|at TSAT - 5 minutes|make sure to be fully ready for pushback and **the last thing you have to do is release your parking brake**|

If the Pre-Departure Clearance (PDC) system is activated by the controller, we strongly recommend using it to minimize congestion on the *Delivery* frequency.
To access the PDC, you must have a Hoppie account.
We recommend following <a href="https://youtu.be/o65x1ShDRKo" target="_blank">this tutorial</a> to better understand how the system works.

### Taxi
All pilots (commercial side) should expect to taxi via **P** after pushing back from their stand. If you are parked at any of the terminals, you can expect to join **P** via the nearest intersection from your position **only if instructed**.

![apc-bo.png](/doc-atc/apc-bo.png)

All pilots (Airbus side) should expect to taxi via **W**.

<u>In case of  doubt or if you are lost, do not hesitate to ask for help from the controller. They will gladly help you navigate the airport</u>. This however should come as an assistance, and not replace the actual usage of charts.

There is only one ground frequency covering both regular traffic and Airbus aprons. It can get extremely busy in case of high traffic intensity. Please behave!

### Taxiways specificities
If you are flying with a <u>wide-body aircraft</u> (B77W, A340, B748, A35K, A3ST), please refer to the appropriate chart before requesting taxi.

As much as traffic allows, **ATC** will provide runway 14R/32L for departure to aircraft from the west Airbus Industries apron.

## Runway usage

TLS airport has 2 runways which are both used in normal operations. For noise abatement reasons, the runway closest to the civil terminal (14L/32R) is used for take-offs. The second (14R/32L) is used for landings.

If you are parked on the Airbus side, you can plan runway 14L/32L for takeoff.

![pistesbo.png](/doc-atc/pistesbo.png)

Runway 32 configuration is used most of the time due to the environment and proximity with Toulouse city.

Only if VMC conditions are met and gusting is less than 25 knots, runways are considered independent and therefore allow parallel and simultaneous take-offs and landings.

## Arrival procedures
Arrivals in TLS are decomposed in 3 different phases : Arrival (STAR), Initial Approach (Transition) and Radar vectors for ILS.

During a "standard" arrival, the en-route controller will clear you for an arrival procedure (STAR) to follow. After your descent, when approaching your IAF (end of STAR), the en-route controller will transfer you to the initial approach controller. The approach controller will clear you to follow an approach (a transition) and will give you your expected arrival runway, before transferring you to the final approach controller when you will be approaching the end of your transition.
This final approach controller is here to give you vectors to the ILS.