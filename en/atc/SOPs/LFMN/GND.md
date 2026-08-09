---
title: Ground Position
description: SOP - LFMN
published: true
date: 2026-07-15T16:05:20.446Z
tags: 
editor: markdown
dateCreated: 2026-07-15T15:47:07.007Z
---

![doc_banner_sops.png](/banners/doc_banner_sops.png)
# Ground Position
## Terminals

Nice Airport is made up of 2 terminals:

- **Terminal 1**: runs alongside taxiways S and T
- **Terminal 2**: runs alongside taxiways C and T

As well as 3 additional areas:

- **Kilo parking**: to the east of the airport, for general and business aviation
- The **cargo terminal**: to the north of Terminal 2

> The **helicopter FATOs and stands** are located to the south of the airport, **outside the Ground controller's area** of responsibility.
{.is-info}

![apron-lfmn.png](/doc-atc/apron-lfmn.png)

## Gate assignment

The RampAgent plugin included in the controller pack handles gate assignment for you.

## Pushback

> Some stands have published pushback directions. In the context of VATSIM, best practice is to **systematically issue the pushback direction** in order to avoid any surprises. **CoFrance helps you** by indicating the appropriate direction.
{.is-info}


Stands between T and U do not require pushback, although pilots on the network may still request it. The same applies to stands located between S, D and T, with the exception of stands 7 and 9 (North-facing), which must push back onto T, and stand 15 (South-facing), which must push back onto S.

The main published pushback directions are described below:

- C, pushback facing South (from stand 40B to stand 48)
- D, pushback facing South preferred. North-facing possible depending on the ground situation.
- S, stand 24 included up to 10B, pushback facing East to taxi via T or D.
- T from T1 or T2, pushback facing the holding points in use.
- Stand 40A and Cargo (28 and 26), pushback facing West to taxi onto C. It is possible to coordinate with the crew a North-facing pushback onto C to taxi right onto S.

For stands 62 to 50 on QFU 043, it is preferable to push back facing West to avoid congestion on C.
![taxi-lfmn.png](/doc-atc/taxi-lfmn.png)

## Taxi

> **On VATSIM**, it is recommended to use **T for departing traffic and U for arriving traffic**. This applies in both runway configurations.
{.is-info}

To streamline ground movements on arrival and avoid blocking the runway, an initial taxi route off the runway can be coordinated with the TWR controller.

Also, to give the TWR controller more flexibility, it is good practice to offer **Light traffic** a **departure from B3 intersection** (TORA 2157m) on 04R.

**There is no intermediate taxi point at Nice**. Clearances should therefore be issued using the following format:

> “Roulez et maintenez avant… / Taxi and hold short of…”

## Holding points
### QFU 043 in use

Runway 04L has 3 usable holding points: A1, B1 and C1.

B1 is the preferred holding point for VFR traffic departing from runway 04L.

A1 and C1 are the preferential holding points.

> Under high traffic load, just 2 aircraft holding at C1 are enough to block taxiways U, C and T, and therefore the whole airport.
{.is-warning}


> The simultaneous use of several holding points is not recommended, in order to limit the risk of conflicts after crossing the inner runway.
{.is-info}


When the number of simultaneous ground movements is low, C1 intersection nonetheless remains a good option for reducing taxi time. This holding point should be used if traffic wishes to depart from intersection B3 on runway 04R.

### QFU 223 in use

Crossing via G1 makes it possible to keep several aircraft on taxiway Y and stabilize the departure rate in high-load situations.

## Special case ILS 04L
![lfmn-hp-a1.png](/doc-atc/lfmn-hp-a1.png =25%x){.align-right}

If weather conditions require the use of the ILS procedure on runway 04L, **several precautions are necessary**:

- traffic must not be held at A1 if another aircraft is about to capture the glideslope
- crews are requested to vacate the runway via F1 or EG/G1

The first constraint is due to the proximity between holding point A1 and the glideslope antenna (risk of signal disturbance).

The second constraint is due to a risk of disturbing the LOC signal.