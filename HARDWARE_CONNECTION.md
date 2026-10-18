# Hardware and connections

## Two separate cables

1. **USB KKL 409.1 interface:** the active USB-to-K-Line electronics. USB connects to the PC; its OBD-shaped male connector connects to the breakout cable. The field-validated interface uses FTDI. Confirm the actual chipset and Windows driver; appearance is not a compatibility test.
2. **OBD female-to-banana breakout cable:** passive wires ending in separate plugs. It lets you choose the vehicle's diagnostic line. It does not replace the KKL interface or convert communication protocols.

### What the two cables look like

**1. USB KKL interface — connects your computer to the diagnostic cable.**

![USB KKL 409.1 interface reference photo](images/kkl-interface-reference.jpg)

**2. OBD female-to-banana breakout cable — connects the KKL interface to individual vehicle sockets.**

![OBD female-to-banana breakout cable reference photo](images/banana-breakout-reference.jpg)

Connect them in this order: **PC USB → KKL interface → breakout cable → vehicle diagnostic sockets**. These original product photos were supplied by Pellaeon Chi as identification references; a matching blue case does not prove an FTDI chipset. Check the chipset, driver and each lead's function. The pictured CD/software is not required or included.

![Connection relationships](images/hardware-wiring.svg)

The illustration is original artwork. It shows logical connections, not socket-hole positions or a particular seller's product. The product reference photos above are separate from this wiring diagram; they do not establish electrical pin assignments.

## Documented W124 HFM setup only

| Function | KKL / OBD side | Vehicle X11/4 16-pole side |
| --- | --- | --- |
| Vehicle-side positive supply | Pin 16 | Socket 16 |
| Ground | Pin 4 or 5 | Socket 1 |
| K-Line | Pin 7 | Socket 8 |

This is the connection used in the project's validated W124 HFM setup. It is not an assurance that every Mercedes-Benz 16-pole socket has the same occupied contacts or supply behavior. It must not be applied to 8-pole or 38-pole connectors or other engine-management systems without their own documentation. The vehicle's old 16-pole X11/4 socket is not the modern 16-pin OBD-II connector on the KKL cable.

Red often indicates positive and black ground, but **check the wire's function, not just its color**. In a multi-lead cable, select the lead connected to **OBD pin 7** for K-Line; do not select an arbitrary yellow plug or the lead marked 8 merely because the vehicle socket is 8.

Read the numbers molded into the vehicle socket. Plug-face and wire-side drawings can be mirrored. With both cable ends disconnected and unpowered, use its wiring diagram or a continuity meter to identify the correct leads. Do not use continuity mode on an energized vehicle circuit. If the cable or vehicle pinout cannot be identified, stop before connecting power.

## Before the first session

- Install the interface maker's appropriate Windows driver and check the COM port in Device Manager. The bundled application does not include a driver or the seller's software CD.
- Confirm vehicle-specific supply and ignition requirements. Socket 16 was used successfully for the project's KKL supply, but behavior in every OFF/ACC/cranking state has not been established.
- Connect with ignition off, follow vehicle/interface instructions, and use a stable supply. Then use the ignition state requested by the operation.
- Keep the vehicle stationary, parking brake applied, transmission in P/N, and leads clear of pedals and hot/moving parts. Do not run simultaneous diagnostic tools on the same K-Line.
- Start with ECU identification and reading. Do not bypass an ECU restriction because a plug fits or a COM port appears.

Use QUICK_START.md for software operation and TEST_REPORTING.md before sharing logs.
