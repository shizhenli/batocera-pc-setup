---
title: "Batocera Controller Not Detected: A Step-by-Step Diagnosis Before the Menu"
description: "Batocera boots from USB but your controller doesn't respond at the menu? Follow this focused diagnosis to restore input and verify the fix."
seo_title: "Batocera Controller Not Detected: Fix No Input at the Menu"
seo_description: "Batocera boots from USB but your controller doesn't respond at the menu? Follow this focused diagnosis to restore input and verify the fix."
keywords:
  - "batocera controller not detected"
date: 2026-11-22T10:59:18+08:00
publishDate: 2026-11-22T10:59:18+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller is silent—no cursor movement, no button presses—and you're stuck before any controlled diagnosis.

## Confirm the controller is seen by the system

First, rule out a dead connection. Unplug and replug the controller into a different USB port, preferably a rear port directly on the motherboard. Avoid hubs during this test. If the controller has a mode switch (XInput/DInput), toggle it and replug. Watch for any LED activity on the controller itself. No light at all suggests a cable or port problem, not a Batocera problem.

## Check Batocera's input detection

At the menu, press F4 to open a terminal. Type `lsusb` and press Enter. Look for your controller's vendor name in the list. If it appears, the hardware is detected and the issue is mapping or mode. If it does not appear, try another cable or port before continuing. Next, run `cat /proc/bus/input/devices` and scan for your controller's name. A missing entry here means the kernel isn't registering it.

## Verification test

Reboot with the controller connected before power-on. At the controller configuration screen, press a button. If Batocera prompts you to map inputs, detection is working. Complete the mapping and confirm the menu responds.

## Rollback and recovery

If changes to controller settings caused the problem, boot without the controller, then reconnect it after the menu loads. If Batocera still shows **batocera controller not detected**, stop repeating the same steps and gather your `lsusb` output for a targeted review.

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with those details rather than reinstalling blindly.
