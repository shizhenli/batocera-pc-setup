---
title: "Batocera Multiple Controllers: Fix No Input at the Menu"
description: "Batocera boots from USB but no controller input reaches the menu. Follow these checks to diagnose multiple controller detection and restore input."
seo_title: "Batocera Multiple Controllers Not Detected: Fix No Input"
seo_description: "Batocera boots from USB but no controller input reaches the menu. Follow these checks to diagnose multiple controller detection and restore input."
keywords:
  - "batocera multiple controllers"
date: 2026-11-18T10:59:17+08:00
publishDate: 2026-11-18T10:59:17+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick with a controller connected, but the menu appears and none of your controllers respond.

## Confirm the controller is seen by the PC

Start at the hardware level. Unplug and replug the controller, then watch the USB port light or listen for the system chime. If nothing changes, try a different port, preferably a rear USB 2.0 port on a desktop. A controller that never enumerates will not work in Batocera regardless of settings.

## Check Batocera's input layer

Boot to the menu and connect a keyboard. Press F4 to open the terminal. Run `lsusb` and look for your controller's vendor name. If it is missing, the issue is cabling, port, or controller mode. If it appears but still no input, run `cat /proc/bus/input/devices` and confirm an event handler is listed. No handler means the kernel driver did not bind. For **batocera multiple controllers**, repeat this check with each controller connected one at a time to isolate a single faulty device.

## Verify with a controlled test

Disconnect all but one controller. Reboot and test menu navigation. If that controller works, add the next one and reboot again. This tells you whether the failure is per-device or a conflict across several controllers. If only one device fails, replace its cable or try a different model.

## Rollback and recovery

If input worked before a recent change, restore your previous Batocera configuration backup or reflash the USB image. Keep a keyboard attached so you can always reach the terminal and recover.

If these steps do not restore input,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your `lsusb` output and controller models.
