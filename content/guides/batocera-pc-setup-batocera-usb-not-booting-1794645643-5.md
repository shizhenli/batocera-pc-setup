---
title: "Batocera USB Not Booting: When the PC Skips the Drive and Returns to Windows"
description: "Troubleshoot a Batocera USB that does not boot because the PC skips it or returns to the existing OS. Check boot order, USB mode, and verify with a controlled test."
seo_title: "Batocera USB Not Booting: Fix PC Skipping USB and Returning to OS"
seo_description: "Troubleshoot a Batocera USB that does not boot because the PC skips it or returns to the existing OS. Check boot order, USB mode, and verify with a controlled test."
keywords:
  - "batocera usb not booting"
date: 2026-11-15T18:34:54+08:00
publishDate: 2026-11-15T18:34:54+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You plugged in your Batocera USB, restarted the PC with a controller connected, and instead of the Batocera menu the machine skipped the drive and loaded your existing OS.

## Confirm the PC Sees the USB at All

Enter your firmware boot menu (often F12, F11, or Esc during power-on). Look for the USB entry. If it is missing, power off, move the stick to a rear USB 2.0 port, and recheck. If it appears but does not launch, note the exact label. A label like "UEFI: SanDisk" means the firmware is reading the drive; no label means the drive is not being enumerated.

## Check Boot Order and Mode

In firmware settings, set USB first in the boot order and disable fast boot. Match the boot mode to how the image was written: UEFI images need UEFI enabled, legacy images need CSM or legacy support. A mismatch here is the most common cause of **batocera usb not booting** when the drive is otherwise detected.

## Verification Test

Save settings, shut down completely, then power on with the USB attached and the controller unplugged. If Batocera reaches its menu, reconnect the controller and confirm input. If the PC still returns to the existing OS, the firmware is not handing off to the drive.

## Rollback and Recovery

If changes make the PC unbootable, re-enter firmware and restore the previous boot order, then re-enable fast boot if it was on. Keep your existing OS drive untouched so you can always boot it. For guided diagnosis,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
