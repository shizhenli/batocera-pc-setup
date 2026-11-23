---
title: "Batocera Controllers Not Detected: A Step-by-Step Diagnosis Before the Menu"
description: "Batocera boots from USB but your controller doesn't respond? Follow these checks to diagnose why batocera controllers aren't detected and restore input."
seo_title: "Batocera Controllers Not Detected: Fix No Input at the Menu"
seo_description: "Batocera boots from USB but your controller doesn't respond? Follow these checks to diagnose why batocera controllers aren't detected and restore input."
keywords:
  - "batocera controllers"
date: 2026-11-23T10:59:19+08:00
publishDate: 2026-11-23T10:59:19+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller presses do nothing—so you're stuck before you can even run a proper diagnosis.

## Confirm the controller is seen by the PC
Start by ruling out the physical connection. Unplug and replug the controller into a different USB port, preferably one directly on the motherboard rather than a hub. If it's wireless, check the receiver is seated and the battery is charged. Watch for an LED on the controller: if it never lights, the PC isn't powering or enumerating it, which points to cable, port, or battery rather than Batocera.

## Check Batocera's input layer
Boot to the menu and, if you have a keyboard, press F1 to open the file manager or use SSH. Look for controller detection in the system logs—if the device appears there but the menu ignores it, the issue is mapping, not hardware. If nothing appears, the kernel isn't seeing the device at all. This distinction tells you whether to fix the controller connection or the input configuration.

## Verification test
With the controller connected, reboot and watch the boot process. If Batocera shows a controller configuration prompt, press a button when asked. A successful detection means the menu should respond immediately. If the prompt never appears and no input registers, the controller is still not detected—proceed to recovery.

## Rollback and recovery
If you recently changed controller settings, restore the previous configuration by renaming the controller profile in the userdata system config folder, or boot with a keyboard and reset input mappings. Keep a keyboard attached as a fallback so you can always reach the menu.

When these steps don't resolve why **batocera controllers** stay silent,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your log details for a targeted review.
