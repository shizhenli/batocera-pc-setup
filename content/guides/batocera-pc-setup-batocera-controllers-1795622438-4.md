---
title: "Batocera Controllers Not Working: A Step-by-Step Diagnosis for USB Boot"
description: "Controller not detected when booting Batocera from USB? Follow these practical checks to diagnose and restore input at the menu."
seo_title: "Batocera Controllers Not Detected: Fix No Input at the Menu"
seo_description: "Controller not detected when booting Batocera from USB? Follow these practical checks to diagnose and restore input at the menu."
keywords:
  - "batocera controllers"
date: 2026-11-26T10:13:22+08:00
publishDate: 2026-11-26T10:13:22+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller does nothing—no cursor movement, no button presses. This guide helps you diagnose why **batocera controllers** aren't being detected and restore input.

## Check Physical Connection and Mode

First, verify the controller is properly connected. If wired, try a different USB port—preferably one directly on the motherboard, not a hub. If wireless, ensure the receiver is plugged in and the controller is paired and charged. Check the controller's mode switch: some have a switch for XInput, DirectInput, or Switch mode. Set it to XInput (or the mode recommended for PC). After any change, reboot Batocera and see if input works.

## Interpret Detection Results

If the controller still doesn't work, look for LED indicators. A solid light usually means it's powered but not communicating; a blinking light often indicates pairing mode. On the Batocera menu, if you see no response at all, the system isn't receiving input. Try a different controller if available—if that works, the issue is with the original controller. If not, proceed to the next check.

## Verify with a Keyboard

Connect a USB keyboard. If the keyboard works in the menu, the system is responsive, and the problem is isolated to the controller. Use the keyboard to navigate to the controller settings and see if any device is listed. If nothing appears, the controller isn't being recognized at the hardware level.

## Rollback and Recovery

If you recently changed controller configurations or updated Batocera, revert to a previous backup. Batocera stores configurations in /userdata/system/configs; restoring a backup from before the issue can help. If you're unsure, consult the documentation or

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).

## Verification Test

After adjustments, reboot and test the controller in the menu. If it responds, the issue is resolved. If not, repeat the checks or try a different USB port or controller.
