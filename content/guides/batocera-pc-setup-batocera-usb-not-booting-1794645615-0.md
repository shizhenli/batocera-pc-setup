---
title: "Batocera USB Not Booting: Fix the PC Skipping Your USB Drive"
description: "Troubleshoot Batocera USB not booting when your PC skips the USB or returns to the existing OS. Step-by-step checks, verification, and rollback."
seo_title: "Batocera USB Not Booting: Fix PC Skipping USB Drive"
seo_description: "Troubleshoot Batocera USB not booting when your PC skips the USB or returns to the existing OS. Step-by-step checks, verification, and rollback."
keywords:
  - "batocera usb not booting"
date: 2026-11-14T19:16:21+08:00
publishDate: 2026-11-14T19:16:21+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You plug in your Batocera USB, press the boot key, and the PC either ignores it or drops back to Windows—so you're stuck before you can even diagnose why **batocera usb not booting** is happening. Let's fix that specific skip-to-OS failure.

## Confirm the USB is seen at the firmware level

Restart and enter your boot menu (often F12, F11, or Esc). If the USB isn't listed, the firmware isn't reading it. Try a different USB port—preferably a rear USB 2.0 port—and re-enter the menu. If it appears now, your front ports or USB 3.0 controller were the issue.

## Check the boot mode and partition scheme

Enter BIOS/UEFI setup and find the boot mode. Batocera images are typically written for UEFI. If your PC is set to Legacy/CSM only, it may skip the USB. Switch to UEFI (or UEFI with CSM) and save. Also confirm Secure Boot is disabled; enabled Secure Boot can silently reject the drive.

## Verify the USB was written correctly

On another computer, open the USB in a file manager. You should see a FAT partition with boot files such as EFI and boot. If the drive shows as unallocated or empty, rewrite the image with balenaEtcher or Rufus in DD mode. A corrupted write is a common cause of a skipped USB.

## Verification test

After adjusting BIOS and rewriting if needed, boot again and open the boot menu. Select the USB entry. Success means you reach the Batocera splash and menu. If it still returns to the existing OS, note whether the USB entry was present—that tells you firmware versus image.

## Rollback note

If changes make things worse, restore your previous BIOS boot mode and Secure Boot setting. Your existing OS remains untouched on its own drive. For guided diagnosis,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
