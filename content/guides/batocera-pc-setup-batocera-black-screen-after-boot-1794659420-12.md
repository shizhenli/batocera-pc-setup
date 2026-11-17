---
title: "Batocera Black Screen After Boot: Diagnose the Splash-to-Black Freeze"
description: "Troubleshoot Batocera stuck on a black screen after the splash when booting from USB with a controller. Step-by-step checks, verification, and recovery."
seo_title: "Batocera Black Screen After Boot: Fix the Splash-to-Black Freeze"
seo_description: "Troubleshoot Batocera stuck on a black screen after the splash when booting from USB with a controller. Step-by-step checks, verification, and recovery."
keywords:
  - "batocera black screen after boot"
date: 2026-11-17T11:59:18+08:00
publishDate: 2026-11-17T11:59:18+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick with your controller connected, the splash appears, and then the display goes black—leaving you stuck before you can diagnose anything. This guide walks you through one specific failure: the splash-to-black transition that never reaches the menu.

## Check the display output first

Power off, then reconnect the video cable to the primary output on your GPU (not the motherboard). Many PCs default to onboard video during boot, then switch to the discrete card—causing a black screen. Reboot and watch the display. If the splash returns but still goes black, move to the next check.

## Isolate the controller

Unplug the controller and reboot. If Batocera reaches the menu without it, the controller is triggering the issue. Reconnect it to a different USB port (rear ports are more reliable) and reboot again. If the black screen returns only with the controller attached, try a different cable or controller to confirm.

## Test with a minimal boot

Remove any extra USB devices except the Batocera stick and controller. Reboot. A successful menu means a peripheral was interfering. If the screen stays black, the problem is likely the video mode or the USB image itself.

## Verification test

After each change, reboot and observe: does the splash appear, and does the menu load within 60 seconds? A menu means the fix worked. A persistent black screen means you need to re-flash the USB or try a different display cable.

## Rollback and recovery

If a recent config change caused the issue, restore the previous batocera.conf from backup. If you cannot reach the menu, re-flash the USB image to a spare stick and boot from it to confirm hardware health. This is your safe rollback point.

If these steps do not resolve your **batocera black screen after boot**,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your hardware details and what you observed at each check.
