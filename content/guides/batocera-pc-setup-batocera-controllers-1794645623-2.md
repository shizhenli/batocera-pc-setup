---
title: "Batocera Controllers Not Detected: Fix No Input at the Menu"
description: "Troubleshoot Batocera when your controller isn't detected at the menu. Step-by-step checks for USB, Bluetooth, and controller configuration."
seo_title: "Batocera Controllers Not Detected: Fix No Input at the Menu"
seo_description: "Troubleshoot Batocera when your controller isn't detected at the menu. Step-by-step checks for USB, Bluetooth, and controller configuration."
keywords:
  - "batocera controllers"
date: 2026-11-14T19:16:21+08:00
publishDate: 2026-11-14T19:16:21+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from USB, the menu appears, but your controller does nothing—no cursor movement, no button response.

## Check the physical connection first

If you're using a USB controller, unplug it and try a different port—preferably a rear port directly on the motherboard, not a hub. Watch the controller's LED: if it doesn't light up, the problem is power or the cable, not Batocera. If it lights but still doesn't respond, move to the next check.

For Bluetooth controllers, ensure pairing mode is active (usually holding the pairing button until the LED flashes rapidly). Batocera won't detect a controller that isn't in pairing mode.

## Verify Batocera sees the device

From the main menu, go to Controller Settings and look at the detected devices list. If your controller appears but buttons don't register, the mapping is wrong—re-run the configuration and press each button firmly when prompted. If nothing appears, the input layer isn't receiving the device at all.

## Test with a known-good input

Plug in a USB keyboard and navigate the menu. If the keyboard works but the controller doesn't, Batocera's input system is fine and the issue is isolated to the controller or its connection. If neither works, the problem is deeper—likely the USB subsystem or a corrupted boot image.

## Rollback and recovery

If you recently changed controller settings, boot with a fresh Batocera USB or reset the controller configuration from the menu. This restores default input handling without wiping your games.

For persistent **batocera controllers** detection failures, confirm your controller model is supported and try a different USB cable. If the issue remains after these checks,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your controller model and connection type.
