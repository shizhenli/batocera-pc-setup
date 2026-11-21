---
title: "Batocera Controllers: No Input at the Menu? Diagnose Before You Reboot"
description: "Batocera boots from USB but your controller doesn't respond at the menu. Follow these checks to diagnose and restore input before rebooting."
seo_title: "Batocera Controllers Not Working: Fix No Input at the Menu"
seo_description: "Batocera boots from USB but your controller doesn't respond at the menu. Follow these checks to diagnose and restore input before rebooting."
keywords:
  - "batocera controllers"
date: 2026-11-21T14:24:39+08:00
publishDate: 2026-11-21T14:24:39+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You booted Batocera from a USB stick, the menu appeared, but your controller sends no input at all.

## Check the physical connection and controller mode

Unplug and replug the controller directly into the PC, not through a hub. If it is wireless, connect it by USB cable first. Watch the controller's LED: a steady light usually means it has power, while a blinking or dark light suggests it is not pairing or charging. On PlayStation-style pads, confirm the mode switch is not set to a profile the PC ignores.

## Test whether the PC sees the device

At the Batocera menu, press a key on a wired keyboard. If the keyboard works but the controller does not, the issue is input detection, not the system itself. Reboot and enter your PC's BIOS/UEFI. If the controller also fails there, the problem is below Batocera: cable, port, or controller mode. If it works in BIOS but not in Batocera, continue below.

## Rule out the USB boot environment

Power off, remove the USB stick, and boot the PC normally. Plug the controller in and check whether Windows or Linux detects it in device settings. If it does not appear there either, replace the cable or try another controller to confirm the hardware. If it appears normally, the USB boot session may have initialized USB ports late; shut down fully, then boot again with the controller already connected.

## Verification test

With the controller connected before power-on, boot Batocera and press the D-pad at the menu. A moving highlight confirms input is restored. If nothing moves, the controller is still not detected and you should not keep rebooting blindly.

## Rollback note

If you changed controller settings or mappings before this happened, revert them to default and retest. Keep a keyboard attached so you can always navigate the menu while diagnosing **batocera controllers**.

Still stuck after these checks?

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your controller model and connection type.
