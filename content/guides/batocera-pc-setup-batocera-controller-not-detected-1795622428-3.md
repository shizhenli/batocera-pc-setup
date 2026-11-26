---
title: "Batocera Controller Not Detected: USB Port and Input Diagnosis"
description: "Fix a controller that is not detected in Batocera when booting from USB. Step-by-step checks for USB ports, input devices, and recovery."
seo_title: "Batocera Controller Not Detected: USB Port and Input Diagnosis"
seo_description: "Fix a controller that is not detected in Batocera when booting from USB. Step-by-step checks for USB ports, input devices, and recovery."
keywords:
  - "batocera controller not detected"
date: 2026-11-26T09:13:20+08:00
publishDate: 2026-11-26T09:13:20+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller does nothing.

## Check the physical connection first
Unplug the controller and try a different USB port, preferably a rear port directly on the motherboard rather than a hub or front-panel extension. Reboot Batocera and watch the boot messages. If the controller's LED stays off, the problem is likely power or the cable. If it lights up but still no input, move to the next check.

## Confirm Batocera sees any input device
At the main menu, press F4 to open a terminal. Type `cat /proc/bus/input/devices` and press Enter. Look for an entry with your controller's name or a generic gamepad listing. If nothing appears, Batocera is not receiving a USB device at all. If an entry appears but the menu still ignores it, the controller is recognized but not mapped.

## Rule out a mapping or configuration issue
If the device shows in the list, exit the terminal and go to Controller Settings. Choose to configure a controller and follow the prompts. If Batocera skips the step or shows no device, the **batocera controller not detected** state is confirmed at the input layer. Reboot once more with only that controller connected to rule out conflicts.

## Verification test
After any change, return to the main menu and press a direction on the D-pad. The highlight should move. Then open a game and confirm the same input works there. If the menu responds but games do not, the issue is per-emulator mapping, not detection.

## Rollback and recovery
If a recent configuration change caused this, restore your previous batocera.conf or controller profile from backup. If you cannot reach the menu, boot with a keyboard, undo the last change, and reboot.

Still stuck after these checks?

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
