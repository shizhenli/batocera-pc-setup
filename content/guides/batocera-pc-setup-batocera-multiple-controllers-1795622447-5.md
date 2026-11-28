---
title: "Batocera Multiple Controllers: Fix No Input When Only One Pad Is Connected"
description: "Batocera boots from USB but your controller isn't detected at the menu. Follow these checks to restore input and verify the fix."
seo_title: "Batocera Multiple Controllers Not Working? Fix No Input at Menu"
seo_description: "Batocera boots from USB but your controller isn't detected at the menu. Follow these checks to restore input and verify the fix."
keywords:
  - "batocera multiple controllers"
date: 2026-11-28T21:37:48+08:00
publishDate: 2026-11-28T21:37:48+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from USB with a controller connected, but the menu appears and no button presses register. The controller is not detected, and you're stuck before any controlled diagnosis.

## Check the physical connection and power

Start with the cable or dongle. If wired, reseat the USB plug and try a rear port directly on the PC, not a hub. If wireless, confirm the receiver is in a USB 2.0 port and the controller is charged. Result to interpret: if the controller's LED stays off after pressing a button, it is not receiving power or pairing. If it lights but Batocera still ignores it, move to the next check.

## Confirm Batocera sees the device

Switch to a keyboard and press F4 to open the terminal. Run `lsusb` and look for your controller's vendor name. If it appears, the hardware is recognized and the issue is input mapping. If it does not appear, the controller is not reaching the system at all. For setups involving **batocera multiple controllers**, repeat this check with only one pad connected to isolate the faulty device.

## Test input directly

In the terminal, run `evtest` and select the controller's event number. Press buttons and watch for events. No events means the kernel sees the device but receives no input, so try a different cable or controller. Events appearing confirms the pad works and points to a configuration problem.

## Verify the fix

Return to the menu with F4 or restart. Press a button; if the menu responds, the controller is detected. If not, roll back by unplugging all controllers, rebooting, and connecting one pad only. If input still fails,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your `lsusb` and `evtest` output.
