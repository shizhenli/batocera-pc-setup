---
title: "Batocera USB Not Booting: Diagnose Boot Order and USB Detection"
description: "Troubleshoot Batocera USB not booting when the PC skips the drive and returns to the existing OS. Check boot order, USB detection, and Secure Boot with clear steps."
seo_title: "Batocera USB Not Booting: Fix PC Skipping USB and Returning to OS"
seo_description: "Troubleshoot Batocera USB not booting when the PC skips the drive and returns to the existing OS. Check boot order, USB detection, and Secure Boot with clear steps."
keywords:
  - "batocera usb not booting"
date: 2026-11-22T09:59:19+08:00
publishDate: 2026-11-22T09:59:19+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

**batocera usb not booting**. You are at the batocera usb does not boot step, and your PC skips the USB or returns to the existing OS instead of launching Batocera.

## Check Boot Order and USB Detection

Restart and enter the boot menu (often F12, F11, or Esc during startup). Look for your USB drive by name or capacity. If it appears, select it and press Enter. If it does not appear, move to the next check.

Enter BIOS/UEFI setup and open the boot priority list. Ensure the USB is listed and set above the internal drive. Save and exit. If the USB is absent from the list, the firmware is not detecting it as bootable.

## Verify USB and Firmware Settings

Try a different USB port, preferably a rear USB 2.0 port. Re-seat the drive firmly. In BIOS, disable Secure Boot if present, and enable CSM/Legacy if your Batocera image was written for legacy boot. Confirm the USB was written correctly with a tool like BalenaEtcher or Rufus; a corrupt write will not boot.

## Verification Test

With the USB selected in the boot menu, you should see the Batocera splash and then the menu with controller input. If the PC still returns to the existing OS, note whether the USB appears in the boot menu at all. Appearing but failing to launch points to Secure Boot or a bad write; not appearing points to port, drive, or firmware detection.

## Rollback and Recovery

If changes prevent the PC from starting its existing OS, re-enter BIOS and restore the previous boot order or re-enable Secure Boot. Keep the original OS drive untouched and use the boot menu for one-time USB boot attempts.

If the drive never appears,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your PC model and USB details.
