---
title: Approach Position
description: SOP - LFMN
published: true
date: 2026-07-15T17:09:37.160Z
tags: 
editor: markdown
dateCreated: 2026-07-15T16:39:53.538Z
---

![doc_banner_sops.png](/banners/doc_banner_sops.png)
# Approach Position
## Sectors
![lfmn-ats.png](/doc-atc/lfmn-ats.png)

## Sector splits

When traffic load requires it, the Nice TMA can be split into 4 sectors.

### Nice Approach (LFMN_APP)
This is the main sector (bandbox). The position covers the entire Nice TMA as well as its FIS sector (SIV).

#### With the ITM present (LFMN_F_APP)
Nice Approach (LFMN_APP) handles traffic arriving from the West *(NISAR, XIRBI, PERUS, ABDIL, TUPOX, ABLAK and BIRGO)* up to the IAF **MUS**.

> In this case, Nice Approach is responsible for the holding pattern at **MUS** if open.
{.is-info}


Transfers to the ITM are made on heading before or after MUS, in coordination with the controller present.

> When the holding pattern is open, the preferred strategy is to descend the traffic to FL80 and transfer it to the ITM, who will then take it out of the hold.
{.is-info}


#### Without the ITM (LFMN_F_APP)
Nice Approach (LFMN_APP) is in charge of traffic up to the IF.

#### Without the East Approach (LFMN_E_APP)
Nice Approach is then responsible for Eastern arrivals, as described in the section dedicated to LFMN_E_APP.

### Nice Departure (LFMN_DEP)
This is the sector in charge of all departures from the airport.

Opening conditions:
- Nice Approach (LFMN_APP) is connected.
- Nice Tower (LFMN_TWR) is connected.

#### Without Mandelieu Tower (LFMD_TWR)
Nice Departure provides top-down service for LFMD.

#### Special points to note
> Be alert to **BASIP departures climbing when BORDI or VEVAR arrivals** are present. Their paths cross with 1,000ft of vertical separation at MIKRU.
{.is-warning}


STAR constraints help reduce the risk of conflict described above by having departures climb to FL100 and arrivals descend to FL110.

#### Nice Approach, East sector (LFMN_E_APP)
This is the sector in charge of arrivals from the East (VEVAR, BORDI, OZMIC, KERIT, SODRI and LONSU) up to the IAF NERAS.

> In this case, Nice Approach (LFMN_E_APP) is responsible for the holding pattern at **NERAS** if open.
{.is-info}


Opening conditions:

1. Nice Approach (LFMN_APP) is connected.

#### Special points to note
> Be alert to **descent clearances for traffic arriving via VEVAR and BORDI**, which cross the flight path of BASIP departures.
{.is-warning}


The conflict risk illustrated above can be reduced by clearing arrivals to FL110 (in accordance with their MVA) to ensure 1,000ft of vertical separation at MIKRU.

Transfers to LFMN_APP or LFMN_F_APP are made on heading before or after NERAS, in coordination with the controller present.

> When the holding pattern is open, the preferred strategy is to descend the traffic to the last assigned level and transfer it to the ITM, who will then take it out of the hold.
{.is-info}


#### Special points to note Nice Arrival, ITM (LFMN_F_APP)
This is the final approach sector, in charge of sequencing traffic to the IF for the approach in use.

Opening conditions:
- Nice Approach (LFMN_APP) is connected.
- Nice Tower (LFMN_TWR) is connected.

#### Special points to note
The sector manages traffic **between MUS and NERAS**, as well as taking traffic out of the holding patterns when they are open.

#### Nice Information, flight information sector (LFMN_I_APP)

This sector covers only the Nice FIS area (SIV) for flight information service outside the TMA.

## Minimum vectoring altitudes
The altitudes below must be strictly observed when traffic is under radar vectoring or proceeding direct to a point.

![lfmn-amg.png](/doc-atc/lfmn-amg.png)

For initial approaches using CDO (Continuous Descent Operations), the descent clearance to the approach platform altitude should be issued once the traffic is within the corresponding MVA area. The traffic will be cleared for the approach at the same time.

## Departure tracks
Northbound departure tracks pass between the Eastern and Western arrivals. Southbound departures pass through the centre of the radar vectoring area.

Vertically, departures pass above traffic under radar vectoring. BASIP departures climb to FL100 and pass beneath VEVAR and BORDI arrivals. Arrivals must cross MIKRU at FL110 or above. Care should therefore be taken with departure climb clearances when North-East arrivals are present.

> For initial levels, refer to the Departures section of the briefing for the Clearance Delivery position.
{.is-info}

Transfers to Marseille Control are made at FL140 for all departures, except Northbound departures, which must climb to FL170; BASIP departures may climb to FL160 if there is no conflict (see COPX).

> For detailed tracks, refer to the SID_RWY22L-22R_RNAV and SID_RWY04L-04R_RNAV charts.
{.is-info}

## Arrival tracks

Arrivals are handed over by Marseille Control at FL140 via AMFOU, KESAK, BIRGO at FL180 via GAPDO, and FL170 via BORDI.

> For detailed tracks, refer to the STAR_EAST_RWY_ALL_RNAV and STAR_WEST_RWY_ALL_RNAV charts.
{.is-info}


You will also find on the Diagram section of this SOP a radar vectoring diagram for arriving aircraft.

## Holding patterns

![lfmn-holds.png](/doc-atc/lfmn-holds.png)

## Point merge

### Config 04
When vectoring traffic to the IAF (BISBO or LEMPU), it is advisable to use the point merge technique.

> The optimal setting is to use 7NM arcs for BISBO and LEMPU with speed vectors set to 2 minutes.
{.is-success}


### Config 22
When vectoring traffic to the IAF (NANAX), it is advisable to use the point merge technique.

> The optimal setting is to use 8NM arcs with speed vectors set to 2 minutes.
{.is-success}

This additional nautical mile allows for a slight increase in spacing between arriving traffic, as there is no rapid exit taxiway on QFU 223.

## Missed approach

On VATSIM, a large proportion of go-arounds will occur during VPTs rather than during instrument approaches.

> The missed approach procedure to be followed differs depending on whether traffic is flying an instrument approach or is established on a VPT.
{.is-warning}


It should therefore be remembered that:
- the ILS 04L/R missed approach procedures always end with radar vectoring,
- the RNP missed approach procedures theoretically end at NERAS (except RNP Z (AR) 22L/R), but in practice this will likely be radar vectoring,
- the VPT missed approach procedures are radar vectoring.

## Other airports in TMA
### LFMD - Cannes Mandelieu
#### Departures
At Cannes, only runway 17 is used for IFR departures.

Departures climb to 2,000ft towards DIMAD, then follow radar vectoring.
Runway 35 remains available for visual departures.

#### Arrivals
Cannes arrivals are similar to those at Nice, and the transfer from LFMM follows the same procedure. The tracks pass below Nice arrivals and are slightly offset to limit interference.

The STARs end at the approach IAF, so traffic must be cleared for the approach before NEKIP or INLOV, unless they are proceeding direct to another point.

#### Approaches
There are 2 preferential approaches at Cannes: the LOC A runway 17, followed by the VPT A 17, and the RNP Y runway 35.

For the runway 17 VPT, another aircraft may only be cleared for the VPT if it joins the downwind leg before the preceding traffic turns onto final. Ideally, sufficient spacing upstream of the LOC approach avoids these situations.

#### VFR
For the following points, it is advisable to refer to the VAC chart.

Note that the traffic pattern differs (altitude and track) depending on the aircraft type.
Several departure and arrival routes exist.

Helicopters preferably use runway 04/22 via HW and HE (MAX 600ft).

In addition, the Quai du Large heliport (LFTL) is located within the Cannes CTR, and is therefore covered by the Tower, or by LFMN_APP/LFMN_DEP in a top-down role.

### LFTZ - La Mole Saint-Tropez
IFR traffic at La Mole is very rare, but it does occur on the network.

#### Departures
At La Mole, only runway 06 is used for IFR departures. Departures climb to 4,000ft towards **STP then LERMA**, before receiving radar vectoring. Departure clearances may be issued, but traffic must report passing 3,500ft.

#### Arrival
Arrival tracks are the same as at LFMD, and are managed in a similar way.

#### Approach
There is only one instrument approach, the VOR A. Arriving traffic must be cleared to descend to 4,000ft, then cleared for the approach.

> When passing 3,500ft, said traffic leaves the class D airspace of the TMA and subsequently receives flight information service only.
{.is-warning}

#### VFR
Flight information service only; for any additional information, refer to the VAC chart.

### LFTH - Toulon-Hyères

Arrivals into LFTH coming from the North cross the Eastern sector of the TMA; they must be cleared to descend to FL70.

> As Nice Approach does not cover Toulon, no arrival or approach clearance should be issued.
{.is-warning}

## FIS

The Nice FIS area (SIV) covers the horizontal limits of the TMAs, from the surface up to the base of the TMA.

To add a layer of realism, you may assign the following transponder codes to helicopters operating within the Nice FIS area.

|Squawk code|5470|5471|5472|5473|5474|5475|5476|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|Destination|Various|LFTZ : La Mole & Presqu’île de St-Tropez|LFMD : AD Cannes Mandelieu|LFTL : HST Cannes Quai du Large|LFMN : AD Nice Côte d’Azur|LNCM : Monaco Heliport|Scenic Flights