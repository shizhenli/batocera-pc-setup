---
title: "Batocera Controller Not Detected: Isolate the Input Fault Before You Reconfigure"
description: "A step-by-step diagnosis for when Batocera boots from USB but your controller is not detected at the menu, with checks, a verification test, and recovery notes."
seo_title: "Batocera Controller Not Detected: Fix No Input at the Menu"
seo_description: "A step-by-step diagnosis for when Batocera boots from USB but your controller is not detected at the menu, with checks, a verification test, and recovery notes."
keywords:
  - "batocera controller not detected"
date: 2026-11-16T08:59:18+08:00
publishDate: 2026-11-16T08:59:18+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You booted Batocera from USB, reached the menu, and your controller sends nothing, leaving you stuck before any controlled diagnosis.

## Confirm the controller is seen by the PC, not just by Batocera

Start at the hardware layer. Unplug the controller, wait five seconds, and reconnect it to a different USB port, preferably one directly on the motherboard rather than a hub or front-panel extension. Reboot into Batocera. If the menu now responds, the original port or hub was the fault; keep the working port and stop here.

If there is still no input, check whether the controller reports itself at all. On a PC, watch the controller's LED: a light that never comes on suggests a cable or power problem, while a steady light with no menu movement points to a mapping or driver issue inside Batocera.

## Rule out the USB boot environment

Because you are running from USB, verify the drive itself is healthy. A slow or failing stick can boot the menu but drop input devices during initialisation. Reflash the same Batocera image to a different USB drive and boot again. If input works on the second drive, the first stick is unreliable and should be replaced.

## Verification test

With the controller connected directly, reboot and press a button at the menu. Success means the selection highlight moves immediately. If it does not, this confirms a **batocera controller not detected** condition rather than a display or boot fault, so you can move on to checking the controller configuration rather than reinstalling the system.

## Rollback and recovery

If you changed controller settings before this happened, restore the previous configuration from your backup, or rename the controller configuration file so Batocera regenerates defaults on the next boot. Keep your working USB drive untouched while testing so you always have a known-good boot.

If these checks leave you without input,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your controller model and port details.
