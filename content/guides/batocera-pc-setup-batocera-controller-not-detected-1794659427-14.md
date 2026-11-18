---
title: "Batocera Controller Not Detected: Diagnose No Input at the Menu"
description: "Fix Batocera controller not detected when booting from USB. Step-by-step checks for cable, port, and controller mode, plus a verification test and recovery note."
seo_title: "Batocera Controller Not Detected: Fix No Input at the Menu"
seo_description: "Fix Batocera controller not detected when booting from USB. Step-by-step checks for cable, port, and controller mode, plus a verification test and recovery note."
keywords:
  - "batocera controller not detected"
date: 2026-11-18T08:59:17+08:00
publishDate: 2026-11-18T08:59:17+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from USB, the menu appears, but your controller does nothing. This is the controller is not detected step, and we will diagnose it calmly before changing settings.

## Check the Physical Connection First

Unplug the controller and inspect the cable or dongle for damage. Plug it directly into a rear USB port on the PC, not a hub or front-panel extension. Result to interpret: if the controller's LED lights up or the dongle is recognized by the PC, power is reaching it. If nothing lights, try a different cable or port before continuing.

## Confirm the Controller Mode

Many controllers default to a mode Batocera may not read at boot. For PlayStation pads, hold the PS button until the light bar settles. For Switch Pro-style pads, ensure they are in wired mode, not pairing mode. Result to interpret: a solid or steady LED usually means the controller is active; a rapid blink often means it is still searching for a host.

## Test Input at the Menu

Press a direction on the D-pad or left stick and watch the menu highlight. Then press the confirm button. Result to interpret: if the highlight moves, input is reaching Batocera and the issue is mapping, not detection. If nothing moves, the controller is still not detected.

## Verification Test

Reboot the PC with the controller already connected. At the menu, move the stick once and wait two seconds. If the highlight responds, detection is restored. If not, repeat the rear-port check with a different controller to isolate the device.

## Rollback and Recovery

If you changed any controller configuration, revert it before rebooting again. Keep the USB drive unchanged so you can return to the previous state. For guided diagnosis,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).

A **batocera controller not detected** fault is usually a port, cable, or mode issue, so verify those before editing configuration.
