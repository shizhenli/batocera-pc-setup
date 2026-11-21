---
title: "Batocera Controller Not Detected: USB Boot Input Fix"
description: "Controller not detected after booting Batocera from USB? Follow these focused checks to restore input at the menu and verify the fix."
seo_title: "Batocera Controller Not Detected: Fix No Input When Booting from USB"
seo_description: "Controller not detected after booting Batocera from USB? Follow these focused checks to restore input at the menu and verify the fix."
keywords:
  - "batocera controller not detected"
date: 2026-11-21T14:21:31+08:00
publishDate: 2026-11-21T14:21:31+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller does nothing—no cursor movement, no button presses.

## Confirm the controller is seen by the PC

Start by checking whether the controller is recognized at the hardware level. With Batocera running, connect the controller directly to a rear USB port (avoid hubs and front-panel ports). Then open a terminal from the main menu (if you can navigate with a keyboard) and run:

`lsusb`

Look for your controller's vendor name or a generic gamepad entry. If it appears, the PC sees it and the issue is Batocera's input configuration. If it does not appear, try a different cable or port—some cables are charge-only. A controller that never shows in `lsusb` is a hardware or cable problem, not a software one.

## Check the input configuration

If `lsusb` lists the controller, Batocera may have bound it incorrectly. Reboot and hold the button to enter the boot menu, then choose the option to reset the controller configuration (often labeled as resetting EmulationStation input). Alternatively, from a terminal run:

`batocera-config controllers`

and re-run the detection wizard. When prompted, press buttons firmly and wait for each confirmation. If the wizard skips a button, the mapping is incomplete and the menu will ignore that input.

## Verification test

After reconfiguring, return to the main menu and press the d-pad and a face button. The selection should move and open a menu. If it does, the fix is confirmed. If not, repeat the `lsusb` check to rule out a loose connection.

## Rollback note

If reconfiguration makes things worse, restore the previous controller profile from the backup Batocera creates automatically, or reboot without saving changes. For persistent **batocera controller not detected** issues,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your `lsusb` output and controller model.
