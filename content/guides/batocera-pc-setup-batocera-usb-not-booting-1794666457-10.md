---
title: "Batocera USB Not Booting: Diagnose the Skip Before Reimaging"
description: "Troubleshoot Batocera USB not booting when the PC skips the drive or returns to the existing OS. Check boot order, USB mode, and boot files with clear tests."
seo_title: "Batocera USB Not Booting: Fix PC Skipping USB Drive"
seo_description: "Troubleshoot Batocera USB not booting when the PC skips the drive or returns to the existing OS. Check boot order, USB mode, and boot files with clear tests."
keywords:
  - "batocera usb not booting"
date: 2026-11-24T08:59:18+08:00
publishDate: 2026-11-24T08:59:18+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You plugged in your Batocera USB, restarted the PC with a controller connected, but the machine skips the drive and returns to the existing OS. This is a controlled diagnosis for that exact skip, before you reimage anything.

## Confirm the PC sees the USB at power-on

Enter the firmware boot menu (often F12, F11, or Esc at the manufacturer splash). Look for the USB entry by name or as a UEFI/legacy device. If it is absent, power off, move the stick to a rear USB 2.0 port, and retry. If it appears only after that change, the original port or hub was the problem.

## Match the boot mode to the image

In firmware settings, check whether the USB entry is listed under UEFI or legacy/CSM. A UEFI-only image will not appear in legacy mode. Set the firmware to the mode that matches your image, disable fast boot, and save. If the entry still does not appear, the bootloader is likely missing or the write was incomplete.

## Verify the boot files on the stick

Mount the USB on another computer. Confirm the expected boot files exist at the root of the correct partition. If they are missing, rewrite the image with a known-good tool and verify the write completed without errors. This is the most common cause of **batocera usb not booting** when the firmware otherwise sees the drive.

## Verification test

Boot again and select the USB entry manually. Success means the Batocera menu appears and your controller responds. If the screen stays black or returns to the existing OS, note the exact behavior and stop repeating the same attempt.

## Rollback and recovery

Before changing firmware settings, record the original boot order and mode so you can restore them. If a rewrite fails, keep the previous working image or a backup stick so the PC remains usable. For a guided diagnosis of your specific firmware and image combination,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
