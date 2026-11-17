---
title: "Batocera USB Not Booting: Diagnose a PC That Skips the Drive"
description: "Fix batocera usb not booting when your PC skips the USB or returns to the existing OS. Step-by-step checks for boot order, USB mode, and secure boot."
seo_title: "Batocera USB Not Booting: Diagnose a PC That Skips the Drive"
seo_description: "Fix batocera usb not booting when your PC skips the USB or returns to the existing OS. Step-by-step checks for boot order, USB mode, and secure boot."
keywords:
  - "batocera usb not booting"
date: 2026-11-17T07:59:17+08:00
publishDate: 2026-11-17T07:59:17+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You're at the Batocera PC with a controller, but when you power on, the PC skips the USB and loads its existing OS—so you're stuck before a controlled diagnosis. Let's walk through this together.

## Check the boot menu and USB entry

Restart and tap the boot-menu key (often F12, F11, or Esc) as soon as the logo appears. Look for your USB drive by name. If it's missing, power off, reseat the drive in a rear USB 2.0 port, and try again. If it appears but selecting it returns to the existing OS, the firmware isn't accepting the drive's bootloader—note that and move on.

## Verify USB mode and secure boot

Enter BIOS/UEFI setup and check two settings. First, set USB boot to enabled or legacy-compatible if available. Second, disable Secure Boot; Batocera's bootloader may be blocked otherwise. Save and exit. If the drive still doesn't appear, the issue is likely the USB itself, not the PC.

## Test the USB on another machine

Plug the USB into a different PC and open its boot menu. If that machine also skips it, reflash the USB with a fresh Batocera image using a known-good writer. If it boots there, your original PC's firmware is the blocker—recheck boot order and CSM settings.

## Verification test

With the USB in a rear port and Secure Boot off, power on and open the boot menu. Select the USB entry. Success means you see the Batocera splash and controller input at the menu. If you return to the existing OS, stop and recheck the bootloader step before repeating.

## Rollback and recovery

If changes to BIOS leave the PC unbootable, re-enter setup and restore default settings, then re-enable Secure Boot if your main OS requires it. Keep your original OS drive untouched so you can always boot back. For a guided diagnosis of **batocera usb not booting**,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
