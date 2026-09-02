---
creation-date: 2026-09-02
copyright-years: 2026
copyright-authors: David SPORN
SPDX-License-Identifier: AGPL-3.0-or-later
---

# Extension boards : pinout design

An extension board will be connected to the main board using a set of connectors that follows some general and common rules

**Legend**

```
x -> signal pin
. -> GROUND pin
012... : column position designators (0, 1, 2, ...)
```

## Key features

* 2 rows of 100mils pitched connectors (pin headers).
* 1 ground connectors for 5 signals connectors in a 2x3 group. In effect, any signal pin is next to at least one ground pin ('next' meaning either horizontally, vertically or diagonally).
* grounds signals are on the same row to allow the extension card to use right-angled connectors along one edge of the pcb, and the inner row (on the pcb) host all the ground pins.

## Base pattern : 5 signal pins

Every pattern is based on this one :

```
xxx
x.x
012
```

E.g. a 15 signal connectors will give the following 2*9 pins arrangement :

```
xxxxxxxxx
x.xx.xx.x
012345678
```

## Base pattern : 16 signal pins

A nice, symmetric arrangement, is made with 2*10 pins :

```
xxxxxxxxxx
.xx.xx.xx.
0123456789
```

For any need involving a set of signal pins that has a size being an integer multiple of 16, this pattern will be used by tiling it onto the connector.

E.g. for 32 signal pins, a 2*20 connector will be arranged like this : 

```
xxxxxxxxxxxxxxxxxxxx
.xx.xx.xx..xx.xx.xx.
0123456789abcdefghij
```

### Application

Example to see the gist of it. In a nutshell, 
* Isolate the DATA and ADDRESS bus
* Depending of the width of the required width for the ADDRESS bus and the number of control lines, the ADDRESS bus and control lines MAY share the same connector.

**E.g. : 32bits data bus**

There will be 3 connectors : 
* a 32 signals connector for the DATA bus
* a 32 signals connector for the ADDRESS bus
* a 16/32 signals connector for the control lines

**E.g. : 16bits data bus**

There will be 2 to 3 connectors : 
* a 16 signals connector for the DATA bus
* a 16/32 signals connector for the ADDRESS bus, and optionnally for the control lines
* an optionnal 16 signals connector for the control lines
