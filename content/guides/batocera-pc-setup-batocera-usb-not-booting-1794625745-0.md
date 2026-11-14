---
title: "Batocera USB Not Booting: Fix the Missing Bootloader"
description: "Step-by-step fix when your Batocera USB drive won't boot because the bootloader is missing or misconfigured. Learn to check, repair, and verify."
seo_title: "Batocera USB Not Booting? Fix the Missing Bootloader"
seo_description: "Step-by-step fix when your Batocera USB drive won't boot because the bootloader is missing or misconfigured. Learn to check, repair, and verify."
keywords:
  - "batocera usb not booting"
date: 2026-11-14T11:11:19+08:00
publishDate: 2026-11-14T11:11:19+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You've flashed Batocera to a USB drive, but your PC ignores it and boots straight into Windows—or shows a blinking cursor. This usually means the bootloader is missing or not properly written.

## Check the USB Drive's Boot Files

First, verify the drive contains the bootloader. Insert the USB into a working computer and open it. You should see a folder named `boot` and, at the root, files like `bootloader` or `syslinux.cfg`. If these are absent, the image wasn't written correctly. Re-flash using BalenaEtcher or Rufus in DD mode—not ISO mode. In Rufus, select "DD Image" when prompted. After flashing, re-check for the `boot` folder. If it's still missing, your USB drive may be failing; try another drive.

## Confirm BIOS/UEFI Boot Order

If the files are present, reboot and enter your BIOS/UEFI settings (usually Del or F2). Ensure the USB is first in boot order. Also check if Secure Boot is enabled—disable it, as Batocera may not be signed. Save and exit. If the PC still skips the USB, try a different USB port (prefer rear ports on desktops).

## Verification Test

With the USB inserted, power on and watch for the Batocera splash screen. If you see it, the bootloader is working. If not, and you've confirmed the files and BIOS settings, the issue is likely the USB write process. Re-flash once more, then test.

## Rollback/Recovery Note

If re-flashing fails repeatedly, your USB may be corrupted. Use a different drive. Also, keep a backup of your Batocera `userdata` folder before re-flashing to avoid losing settings.

![Technician checking USB boot files on a laptop](/images/service-detail-960.webp "Checking USB boot files")

Still stuck with **batocera usb not booting**? [Ask for help](/#consult) and we'll guide you through advanced diagnostics.
