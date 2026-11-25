---
title: "Batocera Controllers Not Detected: Isolate the Input Path Before the Menu"
description: "A focused troubleshooting walkthrough for when Batocera boots from USB but your controller is not detected and no input reaches the menu. Learn exact checks, result interpretation, and a verification test."
seo_title: "Batocera Controllers Not Detected: Fix No Input at the Menu"
seo_description: "A focused troubleshooting walkthrough for when Batocera boots from USB but your controller is not detected and no input reaches the menu. Learn exact checks, result interpretation, and a verification test."
keywords:
  - "batocera controllers"
date: 2026-11-25T10:59:15+08:00
publishDate: 2026-11-25T10:59:15+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller does nothing, and you are stuck at the controller is not detected step before any controlled diagnosis.

## Confirm the controller is seen by the PC

Start with the physical layer. Unplug and replug the controller into a different USB port, preferably a rear port directly on the motherboard. If it is wireless, connect it by cable first. Watch for a brief LED blink or a vibration when you plug it in. No light and no vibration at all means the controller is not receiving power or data, so try another cable before blaming Batocera.

## Check the input device list

From the Batocera main menu, open Controller Settings and then Pad to Keyboard. If the list is empty, the system is not enumerating the device. If a device appears but does not respond, the mapping is wrong rather than the connection. For **batocera controllers** that show up only intermittently, reseat the USB plug and avoid unpowered hubs.

## Run a verification test

Return to the main menu and press a direction on the d-pad or stick. The highlight should move one step per press. Then press the confirm button on a harmless entry. If the highlight moves, input is restored; if not, the controller is still not detected and you should stop changing settings and gather the exact device name shown in the list.

## Rollback and recovery

If you changed mappings while diagnosing, reset the controller configuration to default in Controller Settings, then reboot. This undoes a bad mapping without touching your ROMs or saves. Keep the USB stick unchanged so you can retry the same boot.

If the device never appears in the list after these checks,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with the controller model and connection type.
