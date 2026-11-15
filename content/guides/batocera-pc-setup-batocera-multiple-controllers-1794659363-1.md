---
title: "Batocera Multiple Controllers Not Detected: Isolate the Input Path Before the Menu"
description: "Batocera boots from USB but no controller input reaches the menu when multiple controllers are connected. Isolate the input path, interpret results, and verify detection."
seo_title: "Batocera Multiple Controllers Not Detected: Fix No Input at Menu"
seo_description: "Batocera boots from USB but no controller input reaches the menu when multiple controllers are connected. Isolate the input path, interpret results, and verify detection."
keywords:
  - "batocera multiple controllers"
date: 2026-11-15T18:34:54+08:00
publishDate: 2026-11-15T18:34:54+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick with a controller plugged in, but the menu appears and nothing responds, leaving you stuck before any controlled diagnosis.

## Start with one controller only

Power off, unplug every controller, then connect just one by USB. Boot again. If that single controller works, the problem is contention or a bad second device, not Batocera itself. If it still fails, move to the next check.

## Check the input device list

At the menu, use a keyboard if you have one. Open the controller settings and look at the detected devices list. An empty list means the system never saw the device. A listed but unresponsive entry means detection happened but mapping failed. Write down which case you see, because the fix differs.

## Test ports and cables

Move the controller to a different USB port, preferably a rear port directly on the motherboard. Swap the cable. Reboot and repeat the device list check. If the entry appears only on one port, that port or hub is the fault. Avoid unpowered hubs when testing **batocera multiple controllers**, since they often drop devices during boot.

## Verification test

With one controller confirmed working, add the second controller one at a time, rebooting between each. After each boot, confirm both appear in the device list and that each responds in the menu. Stop at the first failure; that device or port is your culprit.

## Rollback and recovery

If changes make things worse, unplug all controllers, boot with a keyboard, and reset the controller configuration to defaults. Then reconnect only the known-good controller so you always have a working input path.

If the device list stays empty across ports and cables, the issue is deeper than mapping.

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your device list result and port test notes.
