---
title: "Batocera Controllers: Diagnose No Input at the Menu Before Replacing Hardware"
description: "Batocera boots but your controller does nothing at the menu? Follow this controlled diagnosis to confirm whether the controller is not detected and restore input."
seo_title: "Batocera Controllers Not Detected: Fix No Input at the Menu"
seo_description: "Batocera boots but your controller does nothing at the menu? Follow this controlled diagnosis to confirm whether the controller is not detected and restore input."
keywords:
  - "batocera controllers"
date: 2026-11-24T11:59:15+08:00
publishDate: 2026-11-24T11:59:15+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

## Check the controller is seen before Batocera loads

You boot Batocera from USB, the menu appears, but no button press moves the selection. Start by confirming the controller is alive outside Batocera. Unplug it, then plug it back in while the PC is off, and boot into your PC's BIOS or boot menu. If arrow keys or the D-pad move there, the controller and cable are fine and the problem is inside Batocera. If nothing responds in BIOS either, test another cable or port first; that is a hardware or connection fault, not a Batocera fault.

## Confirm what Batocera detects

With Batocera running, connect a keyboard and press F4 to open the terminal. Type `lsusb` and press Enter. Look for a line naming your controller or its USB receiver. If the line appears, the system sees the device but input mapping is failing. If no line appears, the controller is not detected at the USB level, so try a different port, ideally a rear USB 2.0 port, and run `lsusb` again. A controller that appears only on one port points to a port or hub issue.

## Verification test

Reboot with the controller connected and watch the first menu. Press a face button and a direction. If the selection moves, input is restored. If it still does not, open the controller configuration screen from the main menu and check whether any device is listed. An empty list confirms detection is failing before mapping; a listed but unresponsive device means remap it.

## Rollback and recovery

If you changed controller settings, restore the previous configuration from the backup you made, or reset the controller configuration to defaults. Keep the keyboard connected until input works, so you can always recover the menu.

If these checks still leave **batocera controllers** undetected,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your `lsusb` output and port details.
