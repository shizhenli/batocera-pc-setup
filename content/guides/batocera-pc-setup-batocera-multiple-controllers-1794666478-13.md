---
title: "Batocera Multiple Controllers: When No Input Reaches the Menu"
description: "Batocera boots from USB but no controller input reaches the menu. Follow these checks to diagnose multiple controller detection and restore input."
seo_title: "Batocera Multiple Controllers Not Working: Fix No Input at Menu"
seo_description: "Batocera boots from USB but no controller input reaches the menu. Follow these checks to diagnose multiple controller detection and restore input."
keywords:
  - "batocera multiple controllers"
date: 2026-11-24T10:59:18+08:00
publishDate: 2026-11-24T10:59:18+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but pressing buttons on any connected controller does nothing. Before assuming the controllers are broken, run a controlled check of what Batocera actually sees. This failure usually sits between the USB boot environment and controller enumeration, not in the emulator frontend itself.

## Check what the system reports

Disconnect all controllers, then reconnect one at a time. Watch the boot log or the controller configuration screen. If a single controller is detected but a second is not, the issue is port or hub related. If none are detected, move to the next check. Confirm the controller works on another device, and try a different USB port, preferably a rear port directly on the motherboard rather than a front-panel hub. A powered USB hub can also change how **batocera multiple controllers** are enumerated during boot.

## Interpret the result

If one controller appears only after a hot-plug, the boot-time scan missed it. If the configuration screen lists a device but input still fails, the mapping is wrong rather than detection. If no device ever appears, the USB boot environment may not be loading the input driver for that controller type.

## Verification test

Reboot with exactly one controller connected. Open the controller mapping screen and press a button. If the entry highlights, detection works. Then add a second controller and repeat. Record which step fails, because that tells you whether the problem is the controller, the port, or the boot image.

## Recovery note

If changes make things worse, remove any saved controller profile and reboot with a single wired controller. This returns you to a known state before retesting. For a guided diagnosis of your exact hardware,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
