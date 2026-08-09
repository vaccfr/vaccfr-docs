---
title: Before any connection
description: Before any connection
published: true
date: 2026-05-30T20:32:18.384Z
tags: 
editor: markdown
dateCreated: 2026-05-26T19:35:06.060Z
---

# Before connecting
## What is expected of me as a pilot?

Before considering any flight on the VATSIM network, you must be able to:

- **handle your aircraft properly** (heading, altitude, speed — indicated airspeed or Mach number)

- know how to fly an **ILS**, **RNP** (or even VOR) or **visual approach**

- know how to **set your radio panel to tune a frequency**

Those are the really basics.

VATSIM [Learning Center](https://my.vatsim.net/learn) is a good first place to build your theoretical foundations.

<br>

Don't forget those **10 golden rules**:

| Number | Golden Rule  |
|:-------------------------------:|:---:|
| 1 | Aviate, Navigate, Communicate |
| 2 | Ask a question if unsure ! |
| 3 | Maintain a positive and supportive attitude |
| 4 | Remain vigilant of other nearby traffic |
| 5 | Use good radio etiquette |
| 6 | Be familiar with how to fly your aircraft and intervene when necessary |
| 7 | Think ahead of the aircraft. What is next? |
| 8 | Follow instructions and clearances from ATC |
| 9 | Review procedures and use applicable charts while flying |
| 10 | Have fun! |

## How to learn phraseology?

Phraseology can seem intimidating at first. Before flying on the network, take the time to familiarize yourself with a phraseology manual so you know what to say in common situations: clearance request, taxi, takeoff, approach, landing, and so on. **You are expected to know the basics of radio communication and phraseology**.

See the SIA phraseology manual: https://www.sia.aviation-civile.gouv.fr/reglementation

We also strongly recommend this very comprehensive video by [AviationPro](https://www.youtube.com/@AviationPro) :

[![Full Phraseology Guide for a VATSIM IFR Flight from A to B! [VATSIM Tutorials 2017 - #8]](http://img.youtube.com/vi/ecHWjt7cnJM/0.jpg)](http://www.youtube.com/watch?v=ecHWjt7cnJM "Full Phraseology Guide for a VATSIM IFR Flight from A to B")

Feel free to browse their Youtube channel, as it contains a great deal of content.

## Do I need to know how to follow a SID and a STAR?

Yes, it is essential: both for you as a pilot and to make the controller’s job easier. It will allow you to **depart from and arrive at your airport in the most efficient way possible**. We therefore recommend that you understand and know how to follow standard departure procedures (SID) and standard arrival procedures (STAR), as well as the initial altitude or flight level assigned to you.

## "Transponder mode C", what is this?

Setting your transponder to Mode C will **allow all the necessary information to appear on the controller’s radar**: altitude, speed, and your aircraft callsign. Indeed, if your transponder is in standby mode (or OFF, if you prefer), this information will not appear on the radar, making it very difficult for the controller to issue instructions to you.

With the exception of a few airports, whose exceptions do not make the rule, you may assume that your transponder should be set to:

- Standby (OFF) when on ground
- Charlie (ON) when on a runway or airborne

## In which language is air traffic control provided?

Whether by text or by voice:

- in France, you may be controlled in French or English.
- abroad, you will be controlled in English

> Pay in mind, French is a comfort for native people. Not an obligation. English is still the default language on the network, no matter what.
{.is-info}


# I would like to fly on VATSIM
## How to setup my VATSIM pilot client?

Your client (e.g: xPilot, vPilot, Swift) shoud be properly setup, specifically on below points:

- your **mic configuration** (emitting / receiving / general volumes / PTT (push to talk key))

- your **VATSIM identity** (VATSIM CID + password + your identity*)

<br>

About your identity, as per A4b Code of Conduct article, you must choose **one of these 5 options, exclusively** :

- **Option 1:** Full first and last name as provided when you registered (e.g. Joseph Smith)
- **Option 2:** A shortened first name followed by a last name (e.g. Joe Smith)
- **Option 3:** First name only (e.g. Joseph)
- **Option 4:** A shortened first name only (e.g. Joe)
- **Option 5:** Your VATSIM CID only

## What callsign can I choose?

Choose a plausible callsign (take inspiration from real flights or a flight tracker; e.g. for IFR flights: AFRxxx or AFRxxxx, and for VFR flights: Fxxxx).

## Where can I park when connecting to the network?

Whether ATC is online or not, **never spawn on a runway, whether it is active or inactive**. _Spawn at a gate or a parking stand_ instead.

## Is filling a flightplan mandatory?

On VATSIM, filling a flithplan if you are flying **IFR** is **mandatory**.

For a **VFR** flight, filing a flight plan remains **optional, but it is still greatly appreciated** by VATSIM controllers because it helps them anticipate your intentions and place your route within the airspace under their responsibility based on the expected traffic situation.

## Is flight level I will use for cruise solely based on my preference?

No. For IFR flights, choose a cruising level that complies with the __French airspace semi-circular rule__ and the associated parity rules.

## Can I specifically inform that I am a beginner?

In the remarks section of your flight plan, you may include useful information for the controller (beginner / first flight / please speak English slowly / AIRAC cycle / simulator, etc.).

# During my flight
## What should I do if an ATC asks me to contact them?

**Always respond to a controller’s “Contact me”**, either by voice or by text (even if you think they are mistaken).

## How can I avoid interrupting an ongoing transmission on frequency?

When tuning to a new frequency, **wait a few seconds before transmitting** so as not to interrupt an ongoing exchange between the controller and another pilot.

## What is the purpose of UNICOM (advisory) ?

Use of the UNICOM frequency (122.800) is reserved for aeronautical information exchanges so that you can report your intentions and be aware of those of others (takeoff, landing, runway in use, etc.).

You should not use UNICOM to chat about unrelated matters, whether by voice or text. If needed, send a private message to the other person using the following command:

>.msg [station] [your message] {.is-info}

Then press "Enter" to send the message.

**Example:**

> .msg AFR48C Hello ! Confirm you will plan runway 22 for departure?

## Do all VATSIM controllers have the same level of responsibility?

Controllers are grouped by rating, depending on the scope of their responsibility:

- S1 (Delivery, Ground), 
- S2 (Tower), 
- S3 (Approach), 
- C1 (Center).

> **Moving from one rating to another** is made possible by **passing a practical examination on the network** (CPT: Controller Practical Test). To train with greater autonomy, the student controller, just like in PPL (Private Pilot Licence) training, goes through a **solo release phase** during which they may control their training platform independently for a defined period of time.
{.is-info}


## What is “topdown" principle?

Each controller on VATSIM normally provides a **top-down service**: _a higher position covers the duties of lower positions when those lower positions are not open_.

> **Example:** if an approach controller is online, they also provide tower and ground services.

In exceptional circumstances, a controller may reduce the scope of their service or no longer provide certain lower-level services, especially depending on traffic load.

> **Example:** a center controller may decide not to handle traffic patterns at an aerodrome that still falls within their area of responsibility.

## Are there any tools to view aircraft in flight on VATSIM?

You can always check the network status, see which controllers are online, confirm your own presence on the network, and verify that your flight plan has been filed correctly using tools such as VATSPY, SIMAWARE, VATSCOPE, or others.

We recommend using VATSIM Radar, which is actively maintained and supported by VATSIM : https://vatsim-radar.com/

## I’m about to contact a controller: what should I do if I’m unsure?

- If you are unsure, **do not hesitate to contact the relevant controller to ask whether you are within their area of responsibility or whether they are able to provide any service**.

- **Make sure not to block the frequency with your push-to-talk (PTT) stuck transmitting** (this can notably happen when you switch screens or “tab out” of your application).

# In case of disconnection

- In the event of a _connection loss_ (without a simulator crash), you may reasonably reconnect within the next 2 minutes, generally without issue.

- In the event of a simulator crash, if you have an autosave, you may of course reconnect, but common sense requires that you first check carefully whether there is too much nearby traffic. 

Indeed, restarting a simulator and reloading a saved situation often takes 2–3 minutes, and at best you will reappear at the point where you crashed. Traffic following you will most likely already have reached your position, and reconnecting may therefore create a conflict and disrupt the sequence previously established by the controller.

# Other pro-tips

## Is Paris Charles de Gaulle an ideal airport for my first VATSIM flight?

If you are a beginner, **start by flying from smaller or less busy airports**.

Do not depart from London Gatwick if you are not familiar with the specifics of English procedures and phraseology, if you are flying in text and English is not your language, or if you do not know how to program and fly holding patterns. he same applies to LFPG (and Paris TMA in general due to its complexity)

## Am I allowed to connect at a parking stand just to listen to the frequency?

You may connect at a parking stand and remain stationary simply to listen to the frequency, so you can become familiar with the communications and what is expected from you.

## Can the ATC help me configure my FMC ?

During an active control session, the controller may be able to give you some guidance, but assume **they will not necessarily have the time to give you their full attention** to help with connection client settings, finding an appropriate flight plan, FMC setup, and similar matters.

## I can see LFPG_APP is online: what does it control?

On VATSIM, Paris Charles de Gaulle Approach (LFPG_APP) also provides approach service for Le Bourget (LFPB), Orly (LFPO), and sometimes even Beauvais (LFOB).

> **Example:** If you are departing from LFPO and LFPG_APP is online, you are expected to request your clearance from LFPG_APP.

## Can I fly traffic patterns at Orly or Paris Charles de Gaulle?

> No VFR allowed at Paris Charles de Gaulle (LFPG) and Orly (LFPO).
{.is-danger}

If you want to fly VFR in the Paris area, use satellite airfields such as Lognes (LFPL) or Paris-Saclay-Versailles (LFPN) instead. 

Make sure you are familiar with the airspace. Paris area is not easy for VFR flights.

## I need to step away from my PC for a few minutes. What should I do?

If you need to leave the cockpit for a few minutes while in flight, **ask the controller first**. 

That way, their call will not go unanswered while you are away on a toilet break ;)

## I’m experiencing low FPS in my simulator. What should I do?

**Set up your simulator so that, at all times, you remain above the low-FPS warning threshold, which is around 20 FPS** (especially when approaching major airports, where scenery and traffic density are higher).

When your FPS drops and your simulator starts lagging, your aircraft will also appear to move more slowly on the controller’s radar screen. This makes it more difficult to fit you properly into an arrival or departure sequence.

Otherwise, you will be disconnected automatically. You may reconnect, but keep in mind that this will erase part of the information the controller had previously assigned to your label.

