---
title: "Batocera Controllers: No Input at the Menu When Booting from USB"
description: "Controller not detected at the Batocera menu after USB boot? Follow these checks to verify input, rule out port and cable issues, and recover your setup."
seo_title: "Batocera Controllers Not Detected at Menu: USB Boot Fix"
seo_description: "Controller not detected at the Batocera menu after USB boot? Follow these checks to verify input, rule out port and cable issues, and recover your setup."
keywords:
  - "batocera controllers"
date: 2026-11-21T14:21:31+08:00
publishDate: 2026-11-21T14:21:31+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller sends no input, leaving you stuck before any diagnosis.

## Confirm the controller is seen at the hardware level

Unplug and replug the controller into a different USB port, preferably one directly on the PC rather than a hub. Watch the controller's LED: if it never lights or blinks, the PC is not enumerating it, so try another cable or a known-good controller. If it lights but Batocera ignores it, move to the next check.

## Check the input configuration

At the menu, press a button and watch for any cursor movement. No movement means Batocera has no mapping for that device. If you can reach a keyboard, use it to open the controller settings and confirm the device appears in the list. A device listed but unresponsive points to a mapping problem; a device absent from the list points to detection.

## Verification test

Reboot with only that controller connected and no hub. At the menu, press the d-pad in each direction and confirm the highlight moves once per press. If it does, input is restored. If not, the fault is detection, not mapping.

## Rollback and recovery

If a recent configuration change caused this, restore your previous Batocera configuration from backup or reflash the USB stick with a fresh image, then reconnect the controller before first boot. Keep a keyboard attached so you can always reach the settings menu.

For a guided diagnosis of your **batocera controllers**,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
