---
title: CDM - Collaborative Decision Making
description: CDM
published: true
date: 2026-03-18T21:53:38.949Z
tags: 
editor: markdown
dateCreated: 2026-02-27T22:03:43.100Z
---

# Introduction

CDM or Collaborative Decision Making is a European project whose objective is to fluidify departures. It allows an airport to maintain a fluid traffic flow in nominal situations but also in cases of very high demand.

CDM is based on information sharing by all actors involved. It calculates a departure sequence from the stand allowing an orderly flow while optimizing runway capacities.

The benefits of CDM are both economical and environmental because it reduces taxi time by limiting holding point waiting times.

## Clearance Request
As usual, delivery is responsible for issuing IFR clearances. The use of CDM (Collaborative Decision Making) to optimize the sequence will be announced via the ATIS.

When CDM is in operation, pilots are requested to send a TOBT (Target Off-Block Time = time at which they will be ready for pushback) at : <a href="https://cdm.vatsim.fr" target="_blank">https://cdm.vatsim.fr</a>

This ensures an optimum departure sequence planning.

<u>Notes :</u> 
- You should send a TOBT even when it is the same as your flight plan EOBT. 
- You can update your TOBT if you require more time to prepare or are ready to go earlier.

All pilots are expected to make contact with Delivery as soon as practicable to get their IFR clearance.
- If you sent a TOBT, Delivery will confirm your  **TSAT** (= Target Start-up Approval Time)
- In case you haven’t sent a TOBT yet, ATC will ask you at what time you expect to be ready for push (meaning your TOBT), once you give it to them they will confirm it in the CDM and give you a TSAT.

Example :

- ATC :  “AFR123, cleared to Dubai, LANVI5B departure, runway 26R, initial flight level 100, squawk 5624”
- Pilot : “cleared to Dubai, LANVI5B departure, runway 26R initial flight level 100, squawk 5624, AFR123”
- ATC : “correct, TSAT 1020z, report ready”

“TSAT 1020Z” means that you as a pilot can expect start-up/push back approval at the mentioned time.

We recommend taht you request your clearance via datalink in order to get a PDC message directly in your aircraft. This avoids frequency congestion and will include your TSAT and CTOT if applicable.

## Pushback and Engine Start-Up
To ensure a smooth experience, all pilots have an **engine start-up/pushback window** defined as TSAT-5 minutes to TSAT+5 minutes that they must comply with in order to be on time in the departure sequence.

All pilots are expected to be ready for pushback and have informed the Delivery controller **at least 5 minutes prior to their TOBT**.
If you fail to do so by TSAT+5 minutes, you will have to send a new TOBT in order to be resequenced.

The delivery controller will transfer you to GND as soon as your TSAT becomes valid if you reported ready for push beforehand.

On **first contact** with the ground controller, state your stand number, you will then receive a Start-Up or Pushback clearance that you have to **comply with within 2 minutes**.
Failure to do so may invalidate your pushback window and you may lose your departure sequence slot.

## Summary : Actions to do when you connect

|Steps|When|What to do|
|:-:|:-:|:-:|
|1|at connexion|Enter the time you will be ready for pushback (TOBT) here : <a href="https://cdm.vatsim.fr" tagret="_blank">cdm.vatsim.fr</a>|
|2|as soon as possible|**Ask for your IFR clearance**<br>=> you will be given your assigned pushback time (TSAT)|
|3|at TSAT - 10 minutes|**Call Delivery and inform that you are ready for pushback**<br>=> you will be transferred to Ground|
|4|at TSAT - 5 minutes|make sure to be fully ready for pushback and **the last thing you have to do is release your parking brake**|
