---
title: "Batocera Multiple Controllers: No Input at the Menu When Booting from USB"
description: "Batocera boots from USB but no controller input reaches the menu. Follow these step-by-step checks to diagnose multiple controllers and restore input."
seo_title: "Batocera Multiple Controllers Not Working at Menu: USB Boot Input Fix"
seo_description: "Batocera boots from USB but no controller input reaches the menu. Follow these step-by-step checks to diagnose multiple controllers and restore input."
keywords:
  - "batocera multiple controllers"
date: 2026-11-25T07:59:18+08:00
publishDate: 2026-11-25T07:59:18+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick with a controller connected, but the menu appears and none of your controllers respond.

## Check physical connections and controller mode

Start by confirming each controller is detected by the PC itself. Reconnect one controller directly to a rear USB port, avoiding hubs. If it has a mode switch, set it to the correct mode (for example, XInput on Xbox-style pads). Then reboot and watch the boot messages: if the controller LED never lights, the issue is power or cable, not Batocera. If it lights but the menu still ignores input, move to the next check.

## Test one controller before adding others

Disconnect every controller except one. Boot to the menu and press a button. If that single controller works, the problem is with how **batocera multiple controllers** are being enumerated at startup. Reconnect the second controller only after the first is recognized, then reboot and test both. If neither works alone, the input layer is not loading; check that you are using a supported Batocera image and that the USB boot completed without errors.

## Verification test

With one controller connected, open the controller configuration screen from the main menu. Press buttons and confirm each one registers. Then add the second controller and repeat. If both register individually but not together, note the order in which they were connected; that order often determines which device Batocera assigns to player one.

## Rollback and recovery

If a recent change caused this, revert it: remove any custom controller configuration you added and reboot with only the original controller. Keep a backup of your userdata so you can restore it if input stops working after an update.

If these checks do not restore input,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your controller models and connection order.
