---
title: "Batocera Controllers Not Detected at the Menu: A Step-by-Step Diagnosis"
description: "Batocera boots from USB but your controller gives no input at the menu? Follow these focused checks to confirm detection and restore control."
seo_title: "Batocera Controllers Not Detected: Fix No Input at the Menu"
seo_description: "Batocera boots from USB but your controller gives no input at the menu? Follow these focused checks to confirm detection and restore control."
keywords:
  - "batocera controllers"
date: 2026-11-16T09:59:17+08:00
publishDate: 2026-11-16T09:59:17+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller does nothing—so you are stuck at the controller is not detected step without a clear diagnosis.

## Confirm the controller is seen by the PC

Start with the physical layer. Unplug and replug the controller into a different USB port, preferably a rear port directly on the motherboard rather than a hub. Watch the controller's LED: if it never lights, the PC is not enumerating it at all. If it lights but Batocera still ignores it, move on.

## Rule out a mapping conflict

At the main menu, open the controller settings and look for a detected device list. If your controller appears but buttons do not register, the mapping is likely incomplete. Re-run the input mapping wizard and press each prompted button firmly. If the list is empty, the device is not reaching Batocera's input layer.

## Test with a known-good input

Connect a wired keyboard and confirm arrow keys move the menu. If the keyboard works, Batocera's input system is healthy and the fault is specific to your **batocera controllers** connection. If the keyboard also fails, the issue is broader than the controller.

## Verification test

After any change, reboot and press a direction on the controller at the menu. Success means the highlight moves without a keyboard. If nothing changes, the controller is still not detected.

## Rollback and recovery

If a recent mapping change caused this, restore your previous controller configuration from the backup or reset input mappings to defaults, then retest. Keep a keyboard attached so you can always navigate back.

If these checks leave you at the same point,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your controller model and port details.
