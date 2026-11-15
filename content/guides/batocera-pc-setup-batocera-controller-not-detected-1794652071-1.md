---
title: "Batocera Controller Not Detected: Diagnose Input Before the Menu"
description: "Step-by-step diagnosis for when Batocera boots from USB but your controller is not detected at the menu. Check ports, cables, and controller mode, then verify input."
seo_title: "Batocera Controller Not Detected: Fix No Input at the Menu"
seo_description: "Step-by-step diagnosis for when Batocera boots from USB but your controller is not detected at the menu. Check ports, cables, and controller mode, then verify input."
keywords:
  - "batocera controller not detected"
date: 2026-11-15T18:34:54+08:00
publishDate: 2026-11-15T18:34:54+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller does nothing. This guide isolates the cause of a **batocera controller not detected** failure so you can restore input without reinstalling.

## Check the physical connection first

Unplug the controller and plug it into a different USB port, preferably one directly on the motherboard rather than a hub or front-panel extension. Watch the controller's LED. If it never lights, the issue is power or cable, not Batocera. Try a different cable if the controller uses USB-C or micro-USB. For wireless dongles, move the receiver to a front port to reduce interference.

## Confirm the controller mode

Many controllers default to a mode Batocera does not read at boot. Put yours into its standard gamepad mode: on PlayStation pads, hold the PS button until the light bar settles; on Switch Pro pads, press the pairing button once. If the controller has a mode switch, set it to PC or XInput. Then reboot Batocera and watch for a brief input prompt during startup.

## Verify input at the menu

After the reboot, press a directional button and the confirm button. If the menu highlight moves, input is restored. If nothing moves, open the main menu with a keyboard and check that the controller appears under controller settings. A missing entry means the system is not seeing the device at all.

## Rollback and recovery

If you changed controller settings before this happened, revert them to defaults from the same menu. If the controller worked previously, remove any recently added USB devices and retest. Should the device remain invisible,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your controller model and connection type.

Once the menu responds, complete the controller mapping and save it so the fix persists across reboots.
