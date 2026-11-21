---
title: "Batocera Multiple Controllers: Fix One Unresponsive Controller Before the Menu"
description: "One controller works but another doesn't in Batocera? Diagnose port order, USB mode, and udev rules to restore input before the menu."
seo_title: "Batocera Multiple Controllers: Fix One Unresponsive Controller"
seo_description: "One controller works but another doesn't in Batocera? Diagnose port order, USB mode, and udev rules to restore input before the menu."
keywords:
  - "batocera multiple controllers"
date: 2026-11-21T14:24:39+08:00
publishDate: 2026-11-21T14:24:39+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from USB with two controllers, but only one responds at the menu—or none do—and you need to isolate the faulty controller without reinstalling.

## Check physical connection and port order

Unplug all controllers, then connect only the unresponsive one to a rear USB port. Reboot. If it now works, the front port or hub is the culprit; if it still fails, move to the next check. Note whether the controller's LED stays off (no power) or blinks (power but no data).

## Test each controller alone

Boot with just the suspect controller. If it works alone but not with others, the issue is port power or controller order. If it fails alone, the controller or cable is faulty—try a different cable or controller.

## Verify USB mode and udev detection

Some controllers default to a mode that Batocera doesn't read. Check the controller manual for a mode switch (XInput vs DirectInput) and set it to XInput. Then, from a working keyboard, open a terminal and run `lsusb`; if the controller appears, the kernel sees it but Batocera's input layer may not. Run `evtest` and select the controller event; if no events appear when pressing buttons, the device is not reporting input.

## Verification test

Reboot with both controllers connected to rear ports. At the menu, press a button on each. Both should navigate. If only one works, swap the working controller to the other port to confirm the port is not dead.

## Rollback and recovery

If you changed controller order or udev rules, restore the previous configuration by renaming your backup file back. If Batocera still fails to detect any controller, boot without controllers, then reconnect one at a time to rebuild the input map. For persistent **batocera multiple controllers** detection issues,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your `lsusb` and `evtest` output.
