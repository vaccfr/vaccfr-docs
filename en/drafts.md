---
title: Edition
description: Edition home page.
published: true
date: 2026-06-16T16:08:22.750Z
tags: 
editor: markdown
dateCreated: 2026-02-26T15:02:17.171Z
---

![doc_banner_editing_en.png](/banners/doc_banner_editing_en.png)
# Editing

Welcome to the editing section of the French vACC documentation platform. Thank you for contributing to the enrichment of our documentation base.

This page aims to provide a clear framework for creating, updating, and reviewing the documents published on the platform. It brings together:

- contribution principles
- a simple workflow
- specific SOP rules
- and some useful technical reminders

> The tracking of published documents and those currently being written is managed on Planka. If you do not have access to it, please contact the French vACC administration.
{.is-info}

# Before you begin

Before creating a new document or modifying an existing one, a few simple checks must be carried out.

## Check what already exists

Before writing anything, check whether:

- a similar document already exists on the platform
- an equivalent document is already being drafted
- the topic is already tracked on Planka
- the documentation need is clear and corresponds to an identified use case

The goal is to avoid duplicates, unnecessary overlap, and inconsistencies between documents.

## Check the tracking on Planka

Any document, major redesign, or substantial modification must be tracked on **Planka**.

![planka_doc_overview.png](/planka_doc_overview.png =x400)

If no tracking exists yet for the topic you are working on, create a card or contact the Doc Team focal point / administration to initiate it.

### Format de la carte sur Planka

The image below shows a card with the appropriate level of information:

![card_doc_example.png](/card_doc_example.png =x300)

1) Un titre reflétant clairement le nom du support / document
2) Une description avec le lien du document sur la plateforme

> As an editor, you have write permissions in `/drafts/`. Once the document is ready, it will be moved to the correct URL by the Doc Team focal point or the administration.
{.is-info}


To make it easier to identify who is working on which topic, add yourself to the card as a member by clicking the Member button.

The card can then receive several labels depending on its progress status:

![tags_planka_doc.png](/tags_planka_doc.png)

> The `Publié vatsim.fr` label is intended to be phased out. It refers to documents that are still present in the Documentation section of vatsim.fr but have not yet been migrated to this platform.
{.is-info}

# Contribution Workflow

## Step 1: Identify the need and its impacts

Before writing a document, ask yourself the following questions:

- who the document is intended for
- in what context it will be used
- what information it actually needs to convey
- which teams are affected by its content

A document is not meant to be as exhaustive as possible. Above all, it must be **useful to its reader and usable in its intended context**.

If the topic spans multiple areas, make sure the relevant teams are identified from the start.

In particular:

- if the document impacts ATC training, the Training Department must be consulted
- if the topic involves a training platform, a tool, a configuration, or a cross‑functional scope, the relevant teams must be involved before validation

## Step 2: Create or prepare the document

A page can be created when:

- the need is clear
- no duplicate exists
- the topic is properly tracked on Planka
- the relevant teams have been identified if necessary

If a document needs to be updated, request editing access from the administration or the Documentation focal point.

## Step 3: Write with a sufficient level of maturity

Before requesting a review, the document must reach a level of completeness that allows a real assessment of:

- the selected content
- the chosen level of detail
- the clarity of the structure
- the consistency with other materials
- and the long‑term maintainability of the document

A validation request cannot be based on a title, a simple outline, or an empty structure. There must be enough substance to move forward.


## Step 4: Request review / validation

When a document reaches a sufficient level of maturity, a review can be requested.

Depending on the topic, you should contact:
- the **Doc Team** for documentation review
- the **Training Department** if the document relates to training, a training platform, or a tool used in that context
- other relevant teams if the document impacts their scope

## Step 5: Publication

Document publication is reserved for the Doc Team focal point and the administration.

Publication can only occur after:
- review by **at least two people**
- obtaining the necessary validations depending on the topic
- a final consistency check

# Specific Framework for SOPs

SOPs follow a dedicated framework to ensure a coherent, readable, and maintainable documentation base.

## Common Reference

The vACC uses **LFMN** as the **reference model SOP**.

This SOP serves as a common baseline for the structure of future documents of the same type. The goal is not to freeze the content of all SOPs, but to avoid each contributor adopting a different structural logic.

## General Principle

An SOP is intended to describe the **local specificities** relevant to operations on **VATSIM**.

It is not intended to become:
- a general ATC course
- a full reminder of ATC principles already known
- a document covering everything remotely related to a position

## What an SOP *should* contain

An SOP should contain elements that:
- have a concrete impact on operating a position or an airfield on VATSIM
- are applicable within the network
- contribute to local operational consistency
- are not already sufficiently covered by generic documents or network rules

## What an SOP is *not meant* to contain

An SOP is not meant to include:
- generic reminders on how to control
- theoretical developments with no concrete operational impact
- elements valid only in real‑world operations but not applicable on VATSIM
- excessive levels of detail compared to expected network usage

## Expected Structure

The structure of future SOPs must match that of the reference model SOP.

Flexibility applies to the content, not to the architecture of the document.

## Expected Level of Detail

The appropriate level of detail in an SOP is the one that allows a controller to:
- understand the relevant local specificities
- apply only what can actually be applied on the network
- quickly find the relevant information without overwhelming the reader

The goal is not to produce the longest document possible, but the most **clear, applicable, and maintainable** one.

# Writing Guidelines

Ces consignes peuvent évoluer à tout moment.

- Document publication is reserved for the Doc Team focal point and the administration
- A document may only be published after review by at least two people, and approval from the Training Department if it concerns or involves a training platform or tool
- To avoid modifying a published document directly, editing access must be requested from the administration
- This does not apply to new documents or documents being migrated to the new platform
- Documents must be written using the Markdown editor to allow the use of all available integrations
- External links must be inserted using an HTML tag so they open in a new tab, for example: 
`<a href="your-link-here" target="_blank">Your text here</a>`
- Images must be uploaded to the doc-atc folder before being inserted into a document
- Before starting to write a document, check whether a similar resource already exists
- Documents must be written in English. They may be translated into French if the Doc Team’s workload allows it

# Useful tips

Feel free to request additions to further enrich this section.

- To underline text:  `<u>Text</u>`

- To change text alignment (center, left, right) : `<p align="center">Text</p>`

- To center an image (center, left, right) : `![image.png](/image.png =50%x){.align-center}`

The `=XX%` part sets the maximum width of the image as a percentage of the display width.

- To change text color: `<span style="color:red">Text</span>`

- To highlight text: `<mark>Text</mark>`

- Table example:
`|Header 1|Header 2|Header 3|`
`|:-:|:-:|:-:|`
`|1|2|3|`
`^^|4||`
|Header 1|Header 2|Header 3|
|:-:|:-:|:-:|
|1|2|3|
^^|4||

- To insert a line break within a paragraph or a table, use: `<br>`