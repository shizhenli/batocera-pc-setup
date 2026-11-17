---
title: "Batocera Controller Not Detected: USB Boot Input Diagnosis"
description: "Fix Batocera controller not detected when booting from USB: check ports, cables, input mode, and verify with a controlled test."
seo_title: "Batocera Controller Not Detected: USB Boot Input Diagnosis"
seo_description: "Fix Batocera controller not detected when booting from USB: check ports, cables, input mode, and verify with a controlled test."
keywords:
  - "batocera controller not detected"
date: 2026-11-17T08:59:16+08:00
publishDate: 2026-11-17T08:59:16+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller sends no input, leaving you stuck before any diagnosis. This guide isolates that specific failure.

## Check Physical Connection and Mode

Start with the cable and port. Unplug the controller and try a different USB port, preferably a rear port directly on the motherboard. Avoid hubs and front-panel extensions during diagnosis. If the controller has a mode switch, set it to the mode Batocera expects: XInput for Xbox-style pads, DirectInput for older gamepads. Confirm the cable is data-capable, not charge-only. Result interpretation: if the controller's LED stays off or the PC never lists it, the problem is physical or mode-related, not Batocera.

## Confirm the PC Sees the Controller

At the Batocera menu, press a key on a keyboard to open the main menu, then go to Controller Settings and open the input configuration screen. Watch for any detected device name. If nothing appears, switch to a terminal or another OS on the same PC and check whether the controller enumerates. If it does not appear there either, replace the cable or controller before touching Batocera settings. If it appears but Batocera ignores it, continue below.

## Reset and Reconfigure Input

In Controller Settings, remove any stale mapping for that device, then run the input configuration again and press buttons when prompted. Save the profile. If the menu still ignores input, reboot once and retest. This clears a half-written mapping that can block detection.

## Verification Test

After saving, return to the main menu and press the d-pad and a face button. The selection should move and activate. If it does, the fix is complete. If not, repeat the port and mode check once.

## Rollback Note

If changes make things worse, delete the controller profile you just created and reboot; Batocera will prompt for input again. For a persistent **batocera controller not detected** case,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
