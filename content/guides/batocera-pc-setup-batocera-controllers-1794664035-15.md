---
title: "Batocera Controllers Not Working? Diagnose USB Detection Before the Menu"
description: "Fix Batocera controllers not detected at the menu. Step-by-step USB diagnosis, verification test, and recovery for PC booting from USB."
seo_title: "Batocera Controllers Not Detected: USB Diagnosis Before Menu"
seo_description: "Fix Batocera controllers not detected at the menu. Step-by-step USB diagnosis, verification test, and recovery for PC booting from USB."
keywords:
  - "batocera controllers"
date: 2026-11-21T14:27:46+08:00
publishDate: 2026-11-21T14:27:46+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from USB, but your controller gives no input at the menu. This article walks through a controlled diagnosis to confirm whether the controller is not detected.

## Check physical and USB connection

First, unplug the controller and try a different USB port, preferably a rear port directly on the motherboard. Avoid hubs. Reboot and watch the boot messages: if the controller is detected, you should see a USB device line appear. If nothing appears, the controller is not being enumerated at the hardware level.

## Check Batocera input configuration

At the menu, press F4 to open the terminal. Run `lsusb` and look for your controller's vendor and product ID. If it is missing, the system does not see it. If it appears, run `cat /proc/bus/input/devices` and check for a matching event device. No event device means the kernel driver did not bind, so **Batocera controllers** cannot receive input.

## Verification test

Connect a known-working USB keyboard. If the keyboard works but the controller does not, the issue is controller-specific. If neither works, the USB subsystem or port is the problem. This isolates the failure before changing settings.

## Rollback and recovery

If you changed controller mappings or emulator settings, restore the previous configuration from the backup or reset the input configuration to defaults. Reboot and retest with the same port and cable to confirm the change did not persist.

If the controller still does not appear in `lsusb`, try another cable or controller to rule out hardware. For further diagnosis,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
