---
title: "Batocera Multiple Controllers Not Detected: Isolate the Fault Before the Menu"
description: "Fix Batocera multiple controllers not detected at the menu. Isolate the faulty controller, verify input, and recover your USB setup safely."
seo_title: "Batocera Multiple Controllers Not Detected: Fix No Input at Menu"
seo_description: "Fix Batocera multiple controllers not detected at the menu. Isolate the faulty controller, verify input, and recover your USB setup safely."
keywords:
  - "batocera multiple controllers"
date: 2026-11-23T07:59:16+08:00
publishDate: 2026-11-23T07:59:16+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from USB with a controller, but the menu appears and no input reaches it, leaving you stuck at the controller is not detected step.

## Isolate the controller and port

Unplug every controller except one. Use a wired connection or a known-good USB cable, and plug it directly into a rear motherboard port, not a hub or front-panel extension. Reboot and watch the menu. If input works, the original problem is one of the other controllers or a shared hub. If it still fails, move the working controller to a different USB port and reboot again. No input on any port points to the controller or cable; input on one port only points to that port or hub.

## Check what Batocera sees

At the menu, switch to a keyboard if you have one and open the controller configuration screen. If the controller appears but buttons do not register, the mapping is incomplete. If nothing appears, the system is not receiving the device at all. This distinction matters for **batocera multiple controllers**: adding a second device cannot work until the first is recognized reliably.

## Verification test

With one controller connected directly, reboot and press a direction on the menu. The highlight should move immediately. Then connect the second controller and repeat. If the first still works and the second does not, the second controller or its cable is the fault. If both fail together, return to a single controller and test each port.

## Rollback and recovery

If a configuration change caused the loss, restore your previous controller mapping from the backup you made before editing, or remove the last added controller profile and reboot. Keep the USB drive unchanged until input is restored so you can compare behavior.

If these checks do not isolate the fault,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your port map and controller models.
