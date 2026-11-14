---
title: "Batocera Controller Not Detected: Fix No Input at the Menu"
description: "Troubleshoot a controller that is not detected in Batocera when booting from USB. Check connections, ports, and EmulationStation input settings to restore menu control."
seo_title: "Batocera Controller Not Detected: Fix No Input at the Menu"
seo_description: "Troubleshoot a controller that is not detected in Batocera when booting from USB. Check connections, ports, and EmulationStation input settings to restore menu control."
keywords:
  - "batocera controller not detected"
date: 2026-11-14T19:16:21+08:00
publishDate: 2026-11-14T19:16:21+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from USB, the menu appears, but your controller does nothing—so you are stuck at the controller is not detected step with no way to navigate. Let's diagnose this in order.

## Check the physical connection and port

First, confirm the controller is fully plugged in. If it is USB, try a different port—preferably a rear port directly on the motherboard, not a front-panel hub. Unplug any USB hubs or extension cables. If it is wireless, replace the batteries or charge it, then re-pair the receiver. Result to interpret: if the controller's LED lights up or the receiver is recognized, the connection is likely fine and the issue is in software. If nothing lights up, treat it as a power or cable fault.

## Test with a known-good device

Connect a different controller or a USB keyboard. If the keyboard works in the menu, Batocera itself is running and the problem is specific to your controller. If nothing works, the USB port or boot media may be at fault—recheck the drive in another port.

## Verify in EmulationStation input settings

Press F4 or use a keyboard to open the main menu, then go to Controller & Bluetooth Settings and Input Configuration. Re-run the input mapping. If your controller appears in the list but buttons do not register, remap it. If it does not appear at all, the kernel did not load a driver for it.

## Verification test

After remapping or changing ports, return to the main menu and press a direction on the D-pad. The highlight should move. That confirms input is restored.

## Rollback and recovery

If a recent configuration change caused this, restore your previous batocera.conf from backup or reflash the USB with the same image. Keep a keyboard attached so you can always recover the menu. If the **batocera controller not detected** problem persists after these steps,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your controller model and Batocera version.
