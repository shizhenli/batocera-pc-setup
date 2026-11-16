---
title: "Batocera Multiple Controllers Not Detected: Fix No Input at the Menu"
description: "Fix Batocera when multiple controllers aren't detected at the menu. Step-by-step checks for USB boot setups, including port swaps, controller mode, and recovery."
seo_title: "Batocera Multiple Controllers Not Detected: Fix No Input at the Menu"
seo_description: "Fix Batocera when multiple controllers aren't detected at the menu. Step-by-step checks for USB boot setups, including port swaps, controller mode, and recovery."
keywords:
  - "batocera multiple controllers"
date: 2026-11-16T10:59:15+08:00
publishDate: 2026-11-16T10:59:15+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from USB with a controller connected, but the menu appears and no button presses register, leaving you stuck before you can even run a diagnosis.

## Check the controller connection and mode

Start by confirming the controller is actually seen by the PC, not just powered on. Unplug and replug it into a different USB port, preferably a rear port directly on the motherboard. If the controller has a mode switch (XInput, DirectInput, PS4, Switch), set it to XInput or the mode matching a standard gamepad. A controller in the wrong mode may light up but send no usable input.

Next, test with a single controller only. Disconnect every other controller and USB device except keyboard and mouse. Boot Batocera again and watch the first input screen. If one controller now works, the issue is port or hub contention rather than Batocera itself.

## Interpret the result

If the controller works alone but fails when others are connected, you are likely hitting a USB power or enumeration limit. Use a powered USB hub or spread controllers across separate root ports. If no controller works even alone, try a different cable or a known-good controller to rule out hardware.

For **batocera multiple controllers**, the key is isolating whether the failure is per-device or system-wide before changing settings.

## Verification test

With one controller connected directly, boot to the menu and press a direction on the d-pad. If the highlight moves, input is reaching Batocera. Then add a second controller one at a time, rebooting between additions, and confirm each responds before adding the next.

## Rollback and recovery

If a recent change caused this, revert it: remove any controller configuration you edited, or restore your previous Batocera configuration backup. If you cannot reach the menu at all, boot with only a keyboard to regain control, then reconnect controllers one by one. Still stuck?

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
