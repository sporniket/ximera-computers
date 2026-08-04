---
creation-date: 2026-08-04
copyright-years: 2026
copyright-authors: David SPORN
SPDX-License-Identifier: AGPL-3.0-or-later
---
# Objectives and Key Results

## General

### OKR-GEN-01

A Ximera project mixes modern programmable logic (CPLD, FPGA,...), modern controllers, and vintage controllers, to constitute a computer that reproduce the design of _"vintage"_ computers. _"Vintage"_ computers will mean computers sold approximatively between year 1970 and year 2000, using sub-gigahertz CPU of the time (like the MC68k family, the x86 family, previous families like the MC6809, and so on...).

The initial target computers are : 

* The family of computers known as _"Atari ST"_, comprised of the ST, STf, STe, Mega ST, Mega STe, TT030 and Falcon030. This will give the `XMR-ATR-xx` family :
  * **FIRST TARGET** `XMR-ATR-ST` for a 16/32 bits design (16-bits data bus)
  * `XMR-ATR-TT` for a 32/32 bits design (32-bits data bus)
* The family of computers known as "Thomson MO/TO", comprised of the MO5, MO5NR, MO5E, MO6, TO7, TO8, TO9, TO9+. This will give the `XMR-THMSN-xxx` family, with xxx being the particular computer being reproduced.

### OKR-GEN-02

A Ximera project has a modular design, meaning that it is comprised of : 
* A main board, holding the CPU, some PLDs and clocking system for orchestrating the computer. **The main board beyond experimental/proof of concepts, WILL use standard form factor, e.g. ATX**
* A set of extension boards tasked with some subsystems of the target computers. **Unless stated otherwise, extension boards will follow ISA/PCI cards format, but use custom connectors to the
  main board**; the connectors to the main board will be based on **regular 0.1 pitched headers** (rationale : it should be available for longer time than ISA/PCI connectors ; simpler PCB shape -rectangle-).
  _Some designs MAY use standard ISA/PCI extension cards, like designs to reproduce x86-based PCs._
  E.g. of extension boards : 
  * Video+RAM extension, to be able to plug a screen and have a display.
  * HID extension, to plug keyboards, mouses and game controllers.
  * ...

### OKR-GEN-03

A Ximera project WILL be able to run an official ROM of the original target computers, when any required subsystem is present or simulated enough to handle initialization procedures.

A Ximera project MAY be able to run original software, provided it does not require special behaviour from the original system. Typically, office/productivity software, without copy protection tricks, should be able to work.

## Designs inspired by the family of computers "Atari ST" -- XMR-ATR-ST

TODO
