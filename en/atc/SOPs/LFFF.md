---
title: SOP LFFF
description: 
published: true
date: 2026-04-04T14:54:30.545Z
tags: 
editor: markdown
dateCreated: 2026-03-21T12:41:06.673Z
---

# Introduction

This document provides useful information to various positions and describes how they are being operated on the VATSIM network. If you have any questions or doubts, please do not hesitate to reach out to the Training Department.

## Certification

Paris Control doesn’t have its own certification. However, it is **highly recommended** to first obtain the LFPG_APP endorsement. In absence of LFPG_APP, this endorsement becomes <ins>mandatory</ins> for controllers to open any position that provides topdown services at LFPG.

You must ensure that you have the necessary knowledge to operate this facility. This document is intended to provide additional guidance but should not replace the official AIP available on the [SIA](https://www.sia.aviation-civile.gouv.fr/plandesite) (eAIP FRANCE) website. Furthermore, it is assumed that readers are familiar with [MANEX LFPG Radar](/en/atc/SOPs/LFPG).

## Disclaimer

While our goal is to provide ATC service as close to reality as possible, some real-world practices are not suited to the VATSIM environment. Therefore, it is essential to consider:

- pilot skill level, ranging from beginners to highly experienced individuals.
- limitations specific to each simulator and aircraft, including flight models, noise abatement procedures, and other constraints.
- ATC tools constraints: while they are few, our radar systems remain less advanced than those used in real life

> **Caution!** This document is intended for training purposes on the VATSIM network, and is therefore strictly for simulation use only.
{.is-danger}

# General Information

<img src="/doc-atc/lfff/generic-flow.png" alt="DashBoard" style="float: right; max-width: 25%; margin-left: 3%"></img>

Paris ACC operates as an extended approach for CDG and Orly airports.
It also covers a small portion of higher airspace neighbouring Marseille ACC and Geneva ACC.

The facility is divided between the <font color='#6d9eeb'>**West area**</font> (RPAW) and the <font color='#93c47d'>**East area**</font> (RPAE).

Design of most sectors follows:
- Paris departures (<font color='#346cce'>in blue</font>)
- CDG arrivals (<font color='#990000'>in red</font>)
- Orly arrivals (<font color='#c79e20'>in yellow</font>)

Apart from Paris airports, LFFF is also responsible for some of the Lille, Brussels and London flights climb/descending through Paris airspace.

# ATS Positions

**Bandbox** positions such as PAR_CTR are only recommended during <ins>low to medium traffic conditions</ins>, if no other split is open. Approach top down also needs to be considered, when choosing a position.

## Topdown

|Sector|Provision of topdown|
|-|-|
|DODG|Paris TMA|
|TB|Lille TMA|
|--|Seine TMA|

# Sectorization

The sectorization of Paris has been adapted for the VATSIM network. The split between Paris Low and Paris High occurs at FL 265, with the exception of sectors such as LMH and UJ, which start at FL 195. Full sectorization details can be found [here](/en/atc/SOPs/LFFF/sectorisation).

Additionally, some primary sectors have been reorganised and renamed. Sectors DG and DO structured with a diagonal vertical split to accommodate the climb profiles of LFPG and LFPO, are resulting in a simplified DODG sector.

## Paris EGA

Paris EGA defines the airspace shared by LFPG, LFPO & LFPV APP. It includes Paris TMA 2, 3, 4, 5 and a portion of Paris TMA 7 & 9 (class A airspace) also shared with Paris ACC depending on the configuration and whether holding stacks are open.

# Operating Procedures

For transfer conditions with APP, a [dedicated LOA]() is currently being written.

## Arrivals to Paris TMA

Inbounds to the same destination shall be sequenced with a minimum radar separation of **8 NM in trails** to the Initial Approach Fix (IAF), with an assigned speed to ensure a constant or increasing separation. Any assigned speed other than the IAF speed must be reported to the receiving controller.

<img src="/doc-atc/lfff/apte-sequence-example.png" alt="DashBoard" style="max-width: 40%"></img>

> Given the limited space available for most arrival sectors, sequencing can be challenging. For this reason delay vectors **even up to 40° or more** can be given early enough to allow for proper sequencing, as speed control is generally not effective enough.
{.is-info}

> As a last resort if lateral separation could not be established, Paris may coordinate an additional transfer level that is **1000 ft above** the standard one. This can be especially useful when pilots cannot maintain specific speeds.
{.is-warning}


### Direct routing

Arrivals on downwind may be transferred to the IAF directly. Other arrivals shall be transferred on the point located on the boundary of Paris EGA, or any point before.

### Propeller aircraft

Due to technical limitations, XFLs shown in the tags are those for jet aircraft only. Propeller aircraft arriving on downwind, are transferred to a lower altitude. For further details, refer to the [dedicated LOA]() that is currently being written.

## Departures from Paris TMA

De Gaulle APP (LFPG) and Orly APP (LFPO) stream departures following the same SID with a minimum radar separation of **8 NM in trails**, and assign them speeds to ensure a constant or increasing separation. <ins>Coordination with adjacent ACCs</ins> is then crucial to remove the assigned IAS, notably if the routes diverge outside of Paris airspace, where a well-chosen DCT could allow these restrictions to be lifted.

## Paris TMA configuration

Paris configuration is **Linked** when LFPG and LFPO are facing the same direction otherwise the configuration is referred to as **Opposite**. Possible configurations:

|Config.|LFPG|LFPO|
|-|-|-|
|WL|<font color='#346cce'>WEST</font>|<font color='#346cce'>WEST</font>|
|IPGW|<font color='#346cce'>WEST</font>|<font color='#c79e20'>EAST</font>|
|EL|<font color='#c79e20'>EAST</font>|<font color='#c79e20'>EAST</font>|
|IPOW|<font color='#c79e20'>EAST</font>|<font color='#346cce'>WEST</font>|

Due to its close proximity Le Bourget (LFPB) is always facing the same direction as LFPG, on the other hand, Paris-Saclay-Versailles (LFPN) and Villacoublay (LFPV) are linked with LFPO.

### Opposite configurations

The following is a non-exhaustive list of changes that apply to Paris ACC when Opposite configurations are in use:

- **Config IPOW**:
	- LFPB arrivals on OKABO (downwind) are transferred to PO INI instead of PO DEP
  - LFPG LANVI / BUBLI / BAXIR departures are transferred in climb to FL 110 (J) and FL 90 (P) to climb below Orly departures
  - LFPO / PN / PV arrivals on VEBEK are transferred to PG DEP N
- **Config IPGW**:
	- LFPB arrivals on BANOX (downwind) are transferred to PO ITM instead of PO DEP

## Holding Procedures

### Arrivals

Holding stacks for arrivals into Paris TMA, are located on the IAFs. When these stacks are in use, De Gaulle APP and Orly APP are responsible for all levels within the stacks. Additional holding can be possible in Paris airspace using upstream holding stacks.

When arriving north, holding is only possible on **IAF MOPAR** (+BIBAX, LUKIP & ROU) and **IAF LORNI** (+XERAM & ENORI). Therefore northwest arrivals to IAF MOBRO must be <ins>rerouted on MOPAR</ins> for holding, and northeast arrivals to IAF VEBEK <ins>on LORNI</ins> which includes arrivals to LFPO.

### Enroute

|Waypoint|Inbound CRS|Turns|Flight Levels<br>(included)|Speed|
|-|-|-|-|-|
|**DJL**|360°|Right|FL 200 - 350^1^|Standard|
|**PIBAT**|149°|Right|All levels|Standard|
|**LUMAN**|037°|Right|FL 200 - 280|if FL<250,<br>max 240 kts|

^1^Higher levels up to FL 380 must be coordinated with LFEE ACC (Reims), as it interacts with IBODI-GOTED-TRO route above FL 355.