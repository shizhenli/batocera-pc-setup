---
title: "Batocera USB Not Booting: Diagnose the Skip Before You Rebuild"
description: "Fix Batocera USB not booting when the PC skips the drive or returns to the existing OS. Step-by-step checks for boot order, USB detection, and a verification test."
seo_title: "Batocera USB Not Booting: Diagnose the Skip Before You Rebuild"
seo_description: "Fix Batocera USB not booting when the PC skips the drive or returns to the existing OS. Step-by-step checks for boot order, USB detection, and a verification test."
keywords:
  - "batocera usb not booting"
date: 2026-11-16T07:59:15+08:00
publishDate: 2026-11-16T07:59:15+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You plug in your Batocera USB, restart the PC with a controller connected, and it either skips the drive or drops back to the existing OS. Here is how to diagnose that specific skip before you rebuild anything.

## Confirm the PC sees the USB at all

Enter your firmware setup (usually Del, F2, or F12 at power-on) and open the boot menu. If the USB is listed, note its exact label; if it is absent, the PC is not enumerating it. In that case, power off, move the stick to a rear USB 2.0 port, and recheck. A drive that appears only sometimes points to a flaky port or connector.

## Check boot order and mode

In the boot priority list, move the USB entry above the internal disk, save, and exit. Also check whether the firmware is in UEFI or Legacy/CSM mode. If the USB appears only under one mode, match the firmware to it. If the drive is listed but still skipped, disable Fast Boot and Secure Boot, then retry.

## Read the result correctly

If the PC now attempts the USB but returns to the OS, the firmware is not finding a bootloader on the stick. That is a different fault from a missing drive. If it still skips silently, return to the port and detection check.

## Verification test

With the USB first in boot order, save and restart. A successful result shows the Batocera boot menu or splash instead of the existing OS. If it returns to the OS again, the skip is confirmed at the firmware level.

## Rollback note

If changes make the PC unbootable, re-enter firmware setup and restore the previous boot order, then re-enable Secure Boot and Fast Boot. This returns you to a working OS while you address the **batocera usb not booting** fault. For a guided diagnosis,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
