---
title: "Batocera USB Not Booting: Diagnose the Boot Order Before You Reflash"
description: "PC skips your Batocera USB and boots the existing OS? Follow this controlled diagnosis to check boot order, USB detection, and Secure Boot before reflashing."
seo_title: "Batocera USB Not Booting? Fix Boot Order and USB Detection"
seo_description: "PC skips your Batocera USB and boots the existing OS? Follow this controlled diagnosis to check boot order, USB detection, and Secure Boot before reflashing."
keywords:
  - "batocera usb not booting"
date: 2026-11-26T08:13:26+08:00
publishDate: 2026-11-26T08:13:26+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You plug in your Batocera USB, power on the PC with a controller connected, and instead of the Batocera menu the machine boots straight into Windows or returns to the existing OS. This is a boot-order or detection issue, not necessarily a bad image, so diagnose before reflashing.

## Check the one-time boot menu first

Restart and press the boot-menu key for your PC (often F12, F11, or Esc). Look for your USB drive by name. If it appears and boots Batocera, the drive is fine and the fix is in BIOS boot order. If it does not appear, move to the next check.

## Confirm the USB is detected at hardware level

Enter BIOS/UEFI setup and open the boot or storage section. Your USB should be listed as a bootable device. If it is absent, try another rear USB port (avoid hubs and front-panel ports) and recheck. A drive that never appears in BIOS is not a Batocera problem yet.

## Rule out Secure Boot and boot mode

If the USB appears in BIOS but is skipped, disable Secure Boot and set the boot mode to UEFI or Legacy to match how the image was written. Save and exit. This is the most common cause of **batocera usb not booting** when the drive is otherwise healthy.

## Verification test

With the USB set first in boot order, restart. You should reach the Batocera menu with controller input working. If it still returns to the existing OS, note whether the USB appears in the one-time menu; that result tells you whether to reflash or adjust firmware settings.

## Rollback note

Before changing BIOS settings, photograph each screen. If the PC fails to boot normally afterward, restore those settings and re-enable Secure Boot. If the diagnosis stalls,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
