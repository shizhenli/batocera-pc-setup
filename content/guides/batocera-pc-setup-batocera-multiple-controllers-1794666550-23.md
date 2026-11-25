---
title: "Batocera Multiple Controllers Not Detected: A Step-by-Step Input Diagnosis"
description: "Batocera boots from USB but no controller input reaches the menu? Follow this controlled diagnosis to isolate multiple controller detection issues and restore input."
seo_title: "Batocera Multiple Controllers Not Detected: Fix No Input at Menu"
seo_description: "Batocera boots from USB but no controller input reaches the menu? Follow this controlled diagnosis to isolate multiple controller detection issues and restore input."
keywords:
  - "batocera multiple controllers"
date: 2026-11-25T11:59:19+08:00
publishDate: 2026-11-25T11:59:19+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from USB with a controller connected, but the menu appears and no button press registers, leaving you stuck at the controller not detected step.

## Confirm the controller is seen by the PC

Start with the physical layer. Unplug and replug the controller into a different USB port, preferably a rear port directly on the motherboard. Watch for a brief LED flash or vibration. If nothing happens, try a different cable or controller. No light and no vibration usually means the controller is not receiving power, so the issue is hardware or the port, not Batocera.

## Check Batocera's input detection

At the menu, press F4 to open a terminal. Type `lsusb` and press Enter. Look for your controller's name or a generic gamepad entry. If it appears, Batocera sees the device but input mapping may be failing. If it does not appear, the controller is not enumerated at the USB level.

Next, type `cat /proc/bus/input/devices` and press Enter. Scan for an entry matching your controller. A missing entry confirms the kernel is not creating an input device. This is common when using a USB hub or a controller in a non-standard mode.

## Test with a single controller

Disconnect all other controllers and input devices. Reboot and test one controller alone. If it works, the problem is with **batocera multiple controllers** competing for detection during boot. Reconnect them one at a time, rebooting between each, to find the device that blocks the others.

## Verification test

After any change, return to the menu and press a button. If the menu responds, input is restored. If not, repeat the `lsusb` check to confirm whether the device is still missing.

## Rollback and recovery

If a configuration change breaks input entirely, remove the USB drive, mount it on another computer, and delete the `batocera.conf` file from the `boot` partition to reset controller settings. If you need guided help,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
