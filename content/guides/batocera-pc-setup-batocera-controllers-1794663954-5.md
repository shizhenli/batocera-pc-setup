---
title: "Batocera Controller Not Detected: A Step-by-Step Diagnosis"
description: "Batocera boots from USB but your controller doesn't respond at the menu? Follow this controlled diagnosis to confirm whether the controller is detected and restore input."
seo_title: "Batocera Controller Not Detected: Fix No Input at the Menu"
seo_description: "Batocera boots from USB but your controller doesn't respond at the menu? Follow this controlled diagnosis to confirm whether the controller is detected and restore input."
keywords:
  - "batocera controllers"
date: 2026-11-21T14:21:31+08:00
publishDate: 2026-11-21T14:21:31+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller sends no input and you are stuck before you can finish a controlled diagnosis.

## Confirm the controller is seen by the PC

Start with the physical layer. Unplug and reseat the controller, then try a different USB port, preferably a rear port directly on the motherboard rather than a hub. If it is wireless, replace the batteries or charge it and re-pair it. Watch the controller's LED: a steady light usually means it has power, while a blinking light often means it is still searching for a receiver. If the LED never lights, the problem is power or the cable, not Batocera.

## Check whether Batocera registers any input

At the menu, press a button on each connected controller one at a time. If nothing moves, open the main menu with a keyboard and go to Controller Settings, then Controllers. A listed device with a name means Batocera sees it; an empty list means the controller is not being enumerated at the USB or Bluetooth level. If a device is listed but buttons do nothing, the mapping is wrong rather than the detection.

## Verification test

After reseating or re-pairing, return to the menu and press a direction on the D-pad. If the highlight moves, input is restored. If the Controllers list stays empty, the issue is below Batocera and you should test the controller on another computer to rule out hardware.

## Rollback and recovery

If you changed mappings, reset the controller configuration to default before retesting. Keep a keyboard attached so you can always navigate the menu, and if a bad mapping locks you out, delete the controller configuration from the boot USB and reboot.

If these checks leave you at the same controller is not detected step,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your controller model and what the Controllers list shows. For more on **batocera controllers**, confirm detection before changing any mapping.
