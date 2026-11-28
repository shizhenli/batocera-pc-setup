---
title: "Batocera USB Not Booting: Confirm the Drive Is Seen Before You Change BIOS"
description: "Fix Batocera USB not booting when the PC skips the drive or returns to the existing OS. Check USB detection, boot order, and run a quick verification test."
seo_title: "Batocera USB Not Booting: Check If the PC Sees the Drive"
seo_description: "Fix Batocera USB not booting when the PC skips the drive or returns to the existing OS. Check USB detection, boot order, and run a quick verification test."
keywords:
  - "batocera usb not booting"
date: 2026-11-28T22:06:10+08:00
publishDate: 2026-11-28T22:06:10+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You plugged in your Batocera USB, restarted the PC with a controller connected, and it either skipped the drive or went straight back to your existing OS. Before changing BIOS settings, confirm the PC can actually see the USB drive. This is the first controlled diagnosis for **batocera usb not booting**.

## Check physical detection first

With the PC powered off, plug the USB into a rear port directly on the motherboard, not a front-panel hub or extension cable. Power on and enter the boot menu. The exact key varies by vendor: often F12, F11, F8, or Esc. Look for the USB drive by name or capacity in the boot menu list.

Interpretation: if the drive appears, the hardware is detected and the issue is boot order or boot mode. If it does not appear, the USB is not being read at the firmware level, so stop changing OS settings and inspect the drive and port.

## Check boot order and mode

Enter BIOS/UEFI setup. Confirm the USB is above the internal disk in boot priority. Check whether the system is set to UEFI only, Legacy only, or both. Try the mode that matches how the Batocera image was written. Save and exit.

## Verification test

Reboot with the USB still in the rear port and open the boot menu again. Select the USB entry manually. A successful result is the Batocera boot menu or splash appearing. If the PC still returns to the existing OS, the firmware is not handing off to the USB.

## Rollback and recovery

If you changed boot order or mode and the PC no longer starts its existing OS, re-enter BIOS, restore the previous boot order, and set the original boot mode. Remove the USB before rebooting to confirm the internal system still starts.

If the drive never appears in the boot menu after these checks, the image or the USB itself needs attention. For a guided next step,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
