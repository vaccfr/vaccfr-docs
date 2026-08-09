---
title: Ground Position
description: SOP - LFRS
published: true
date: 2026-07-20T15:31:57.425Z
tags: 
editor: markdown
dateCreated: 2026-06-25T13:47:32.996Z
---

![doc_banner_sops.png](/banners/doc_banner_sops.png)
# Ground position
## Clearance delivery
There is no DEL position in LFRS: GND provide clearance delivery services.

SIDs designators in LFRS are:
- xN for runway 03 (facing North)
- xS for runway 21 (facing South)

ANG departures have an additional designator (respectively P or T for 03 and 21). These SIDs initially go West instead of East; they can be requested by LFRS_APP in order to avoid a conflict with traffic arriving from that direction.

All SIDs are RNAV SIDs and have a 5000ft initial climb. Omnidirectional departures are available (for NON-RNAV aircraft ONLY, see charts for description) and should also be cleared to 5000ft.

Trafic going to LFRZ should receive an ERBIN SID (which brings them to MT). Initial climb is usually set to 3000ft, in coordination with APP if present.

## Aprons
The main (commercial) apron consists of stands 1 to 20 and L2 to L5. Additionally:
- Aprons J and N are used by airclubs and only allow single engine light aircraft.
- Apron M to the south of the main movement area is a remote parking area used as an overflow (code C max).
- Stand K1 is located next to the entry to aprons J and N can fit aircraft up to code C.
- Stand I located between apron N and taxiway F, is an autonomous stand for code A (wingspan <= 15m) aircraft only.

### Gate assignment
The RampAgent will handle gate assignment for you while complying with all stand restrictions.

In case of malfunction or errors, here are the major points to keep in mind :
- The only "large" (code E) stands are 19A (max span 65m) and 5A (max span 61m); stands 18A/19/20 can accommodate certain code D aircraft (check SIA charts for details).
- L gates are usually used by low-cost carriers (max A320),
- Stands 11/18/18A/19/19A/20 welcome cargo aircraft.
- Helicopters are not allowed on aprons I/J/N.

## Ground movement
### Taxi
Taxiways D, E, RD, VN, VS and VM are limited to code C aircraft (*wingspan <= 36m*).

Code F aircraft can only use taxiway C to enter and vacate the runway, this means they require backtrack to line-up or vacate the runway.

### Pushbacks
Stands L2 to L5 and stand 1 push onto R, simultaneous pushbacks require 2 stands of spacing (1 + L3/L4/L5 or L2 + L5).

All applicable pushback restrictions are present in RampAgent.
In case of malfunction or errors, here are the main restrictions to keep in mind.
Code C aircraft (max span 36m):
- L gates and stand 1 push onto R,
- Stand 2 push facing W on RD or facing S on R,
- Stand 3 push facing W or E on RD,
- Stands 4/5/6/10 push on RD, VN, or facing N between RC and RD,
- Stands 7/8/9 must push long facing E on RD, or facing N between RC and RD,
- Stands 11/12/17/18/18A/19/20 push on RC, VS, or facing S between RC and RD,
- Stands 14/15/16 must push long facing E on RC, or facing S between RC and RD,
- M stands are autonomous.

Code D/E aircraft:
- Stand 5A (code E) can only push facing E on RD.
- Stand 18A/19/20 can either push face S between RC and RD, or facing N/S on taxiway R.
- Stand 19A push facing N or S on R.


### Holding points
Departures normally use the full runway length (holding point A or F).
In all cases priority shall be given to IFR traffic regardless of VFR wait times.

**Runway 03**:
- VFR traffic depart from B unless they request otherwise,
- IFR should depart from A. B is available on request for approach category B aircaft or below (eg. ATR, TBM, small business jets …)

**Runway 21**:
- F is standard unless E is requested and operationally feasable.

Arriving traffic on runway 03 should when able vacate via C, D or E to avoid the LOC critical area. The runway exit to be used shall be coordinated with the TWR controler (when present) to safeguard any conflicting movement.

When arriving on runway 21, traffic is expected to vacate via B.
