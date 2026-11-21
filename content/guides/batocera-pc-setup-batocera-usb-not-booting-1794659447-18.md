---
title: "Batocera USB Not Booting: Diagnose Before You Reflash"
description: "Fix a Batocera USB that the PC skips or returns to the existing OS. Check boot order, UEFI/legacy mode, and USB integrity with a clear verification test."
seo_title: "Batocera USB Not Booting: Diagnose Before You Reflash"
seo_description: "Fix a Batocera USB that the PC skips or returns to the existing OS. Check boot order, UEFI/legacy mode, and USB integrity with a clear verification test."
keywords:
  - "batocera usb not booting"
date: 2026-11-21T14:21:31+08:00
publishDate: 2026-11-21T14:21:31+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You're at the PC with your controller ready, but the machine skips your Batocera USB and boots straight back into the existing OS.

## Confirm the PC sees the USB at all

Power on and open the one-time boot menu (often F12, F11, or Esc). If the USB appears, select it and watch what happens: a brief flash then return to the old OS usually means the firmware rejected the drive's boot files, while no entry at all points to the USB not being enumerated. If it's absent, move the drive to a rear USB 2.0 port and retry; front ports and hubs can fail to enumerate during POST.

## Check firmware mode against the image

Enter firmware setup and note whether it boots UEFI, legacy/CSM, or both. A UEFI-only image won't appear in legacy mode, and vice versa. Set the mode to match how you wrote the image, disable Secure Boot if it's on, then save and retry the boot menu. If the drive now appears but stalls, the bootloader is present and the problem is further along.

## Rule out a bad write

On another machine, verify the USB's partition table and that the boot files exist. Reflash with a known-good imager and confirm the write completes without errors. This is the point where many people reflash blindly; only do it after the checks above, so you know whether you're fixing the firmware or the media.

## Verification test

Boot the USB and confirm you reach the Batocera menu with the controller responding. If it still skips, try a different USB stick before changing any more firmware settings.

## Rollback note

Record your original boot mode and Secure Boot state before changing them, and restore those values if Batocera still won't start so your existing OS keeps booting normally. For a guided diagnosis of **batocera usb not booting**,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
