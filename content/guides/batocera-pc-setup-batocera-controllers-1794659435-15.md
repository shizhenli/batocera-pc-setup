---
title: "Batocera Controllers Not Working on USB Boot: A Step-by-Step Diagnosis"
description: "Controller not detected after booting Batocera from USB? Follow these exact checks to diagnose and restore input at the menu."
seo_title: "Batocera Controllers Not Detected on USB Boot: Fix No Input"
seo_description: "Controller not detected after booting Batocera from USB? Follow these exact checks to diagnose and restore input at the menu."
keywords:
  - "batocera controllers"
date: 2026-11-18T09:59:16+08:00
publishDate: 2026-11-18T09:59:16+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller does nothing—no cursor movement, no button presses. This is a common detection issue, and we can work through it systematically.

## Check physical and connection basics
First, confirm the controller is fully plugged in or paired. For USB, try a different port—preferably one directly on the motherboard, not a hub. For Bluetooth, ensure it is in pairing mode. Then reboot Batocera. If the controller still does not respond, move to the next check.

## Verify Batocera sees any input device
At the main menu, press F4 to open a terminal. Type `lsusb` and press Enter. Look for your controller’s name or a generic gamepad entry. If it appears, the hardware is recognized; the issue is likely mapping or driver. If nothing appears, the controller is not being detected at the USB level—try another cable or controller to rule out hardware failure.

## Check controller configuration
Return to the menu (type `exit`). Navigate to Controller Settings using a keyboard. If your controller is listed but not responding, select it and choose “Configure.” Follow the on-screen button prompts. If it is not listed at all, the system has not detected it, which points back to the connection or a missing driver.

## Verification test
After any change, reboot and try moving the menu cursor with the controller. Success means the cursor moves and buttons register. If not, repeat the `lsusb` check to see if detection changed.

## Rollback and recovery
If a configuration change makes things worse, you can reset controller settings from the same menu or restore a previous backup of your Batocera configuration. Keep a keyboard handy for navigation.

If these steps do not restore input, the issue may be specific to your hardware or Batocera build. For a guided diagnosis of your **batocera controllers**,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
