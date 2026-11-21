---
title: "Controller Not Detected in Batocera: Diagnose Input Before the Menu"
description: "Troubleshoot a Batocera controller not detected when booting from USB. Follow checks for USB ports, controller mode, and verification tests to restore input at the menu."
seo_title: "Batocera Controller Not Detected: Fix No Input at the Menu"
seo_description: "Troubleshoot a Batocera controller not detected when booting from USB. Follow checks for USB ports, controller mode, and verification tests to restore input at the menu."
keywords:
  - "batocera controller not detected"
date: 2026-11-21T14:27:46+08:00
publishDate: 2026-11-21T14:27:46+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, but the menu appears and your controller does nothing.

## Check physical connection and controller mode
First, confirm the controller is fully seated in a rear USB port on the PC, not a front-panel hub. Unplug it, wait five seconds, and reconnect. If it is a wireless dongle, move it to another port and avoid USB 3.0 ports if the dongle is USB 2.0 only. Next, check the controller mode: many gamepads have a switch for XInput, DirectInput, or PS mode. Set it to XInput or the mode recommended for PC. If the controller has a pairing button, press it once; the LED should stop blinking and stay solid. If the LED keeps blinking, the controller is not paired and Batocera cannot see it.

## Interpret what you see
If the controller LED is solid but Batocera still shows no input, the issue is likely the USB port or cable. Try a different cable and a different rear port. If the LED is off, the controller has no power; test the cable on another device. If the controller works on another device but not in Batocera, the problem is Batocera's input detection, not the hardware.

## Verification test
Reboot Batocera and watch the controller LED during boot. Once the menu loads, press the D-pad and a face button. If the menu highlight moves or a sound plays, input is restored. If nothing happens, repeat the port and mode checks before changing any settings.

## Rollback and recovery
If you changed controller settings in Batocera, revert them by booting without the controller, then reconnect it. If the system still ignores input, use a keyboard to navigate to the controller configuration menu and reset to defaults.

If these steps do not resolve your **batocera controller not detected** issue,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your controller model and LED behavior.
