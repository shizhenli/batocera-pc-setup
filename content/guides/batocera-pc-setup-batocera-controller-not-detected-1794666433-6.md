---
title: "Batocera Controller Not Detected: Check USB Port and Input Before the Menu"
description: "Fix a Batocera controller not detected at the menu when booting from USB. Check the port, cable, and input device, then verify with a quick test."
seo_title: "Batocera Controller Not Detected: Fix No Input at the Menu"
seo_description: "Fix a Batocera controller not detected at the menu when booting from USB. Check the port, cable, and input device, then verify with a quick test."
keywords:
  - "batocera controller not detected"
date: 2026-11-23T09:59:16+08:00
publishDate: 2026-11-23T09:59:16+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from USB and reach the menu, but your controller sends no input, leaving you stuck before any diagnosis.

## Start with the physical connection

Power off the PC, then move the controller to a rear USB port directly on the motherboard, not a front-panel hub or extension cable. Use a data-capable cable; some charge-only cables never carry input. Reboot and watch the boot messages. If the controller's light stays off and no input appears at the menu, the system is not seeing the device at all. If the light turns on but the menu still ignores it, the device is seen but not mapped.

## Confirm what Batocera sees

At the menu, press a key on a wired keyboard to open the main menu, then go to Controller Settings and open the input configuration screen. If the controller is listed there, remap it and save. If nothing is listed, the problem is below the menu layer, so return to the port and cable checks. This is the common shape of a **batocera controller not detected** fault: the device never reaches the input layer.

## Verification test

After remapping or changing the port, reboot once and press a direction on the controller at the menu. The highlight should move immediately. Then open a game and confirm the same input works there. If the menu responds but the game does not, the mapping saved but the emulator profile did not.

## Rollback and recovery

If a remap makes things worse, reopen Controller Settings and reset the input configuration to default, then reboot. Keep the original USB port noted so you can return to it. If the controller still never appears,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your controller model and port details.
