---
title: "Batocera Black Screen After Boot: Fix the Splash-to-Black Display on USB"
description: "Troubleshoot Batocera black screen after boot when booting from USB with a controller. Step-by-step checks for display output, video mode, and recovery."
seo_title: "Fix Batocera Black Screen After Boot on USB (Splash Then Black)"
seo_description: "Troubleshoot Batocera black screen after boot when booting from USB with a controller. Step-by-step checks for display output, video mode, and recovery."
keywords:
  - "batocera black screen after boot"
date: 2026-11-18T11:59:17+08:00
publishDate: 2026-11-18T11:59:17+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from USB, see the splash, then the display goes black and stays that way.

## Confirm the symptom and rule out a dead session

First, check whether the system is still running. Press a controller button or move a stick. If you hear menu sounds, the PC is alive and only video output is lost. If there is no sound and no controller response, treat it as a full hang. Also watch the USB activity light: steady blinking means the system is still loading; no activity suggests a stall.

## Check the display path

Power off, then reseat the video cable at both ends. Try a different port on the GPU or motherboard, and if possible a different cable or monitor. Boot again. If the splash returns and then goes black, the handoff from bootloader to the graphics driver is failing. That is the classic **batocera black screen after boot** pattern on USB installs.

## Force a safe video mode

At the boot menu, edit the boot entry and add `nomodeset` to the kernel line, then boot. If you reach the menu, the default video mode is the problem. Remove the edit afterward and set a fixed resolution in the Batocera video settings instead.

## Verification test

Boot normally without edits. You should see the splash, then the main menu within about 30 seconds, and the controller should navigate it. If the screen stays black but controller sounds work, the video mode is still wrong.

## Rollback and recovery

If an edit makes things worse, re-edit the boot entry and remove your change, or restore the previous `batocera.conf` from backup. Keep the USB unchanged until you confirm the menu appears.

If these checks do not restore the menu,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your GPU model and boot log.
