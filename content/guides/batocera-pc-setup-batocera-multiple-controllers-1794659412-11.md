---
title: "Batocera Multiple Controllers Not Detected: Isolate the Input Fault"
description: "Fix Batocera when multiple controllers are not detected at the menu. Step-by-step checks to isolate the input fault before the menu appears."
seo_title: "Batocera Multiple Controllers Not Detected: Isolate the Input Fault"
seo_description: "Fix Batocera when multiple controllers are not detected at the menu. Step-by-step checks to isolate the input fault before the menu appears."
keywords:
  - "batocera multiple controllers"
date: 2026-11-17T10:59:19+08:00
publishDate: 2026-11-17T10:59:19+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from USB with a controller connected, but the menu appears and no button press registers.

## Check physical connection and mode
Unplug and reseat the controller, then try a different USB port directly on the PC, not a hub. Confirm the controller is in the correct mode: many gamepads have a switch for XInput, DirectInput, or PS mode. Set it to XInput for Batocera. If a light on the controller stays off, the port or cable is the fault. If it lights but still no input, move to the next check.

## Test one controller, then add the second
Connect only one controller. Boot Batocera and press a button at the menu. If that works, shut down, add the second controller, and boot again. If the first still works but the second does not, the issue is the second device or its mode switch. If neither works alone, the problem is the PC port or Batocera input configuration, not the **batocera multiple controllers** setup itself.

## Verify with a known-good device
Use a wired keyboard to reach the menu. If the keyboard works, Batocera is running and the fault is controller-specific. If the keyboard also fails, the USB port or boot media is the problem. This separates input faults from boot faults.

## Rollback and recovery
If you changed controller settings in Batocera, rename the controller configuration file in the userdata system config folder and reboot. Batocera will recreate defaults. Keep a backup of the original file so you can restore it if needed.

If these checks do not isolate the fault,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your controller model and port details.
