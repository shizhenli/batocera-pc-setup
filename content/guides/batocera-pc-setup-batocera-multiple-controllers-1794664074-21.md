---
title: "Batocera Multiple Controllers: No Input at the Menu — A Step-by-Step Diagnosis"
description: "Controller not detected in Batocera? Follow this technician's step-by-step diagnosis for multiple controllers, with exact checks, a verification test, and a rollback note."
seo_title: "Batocera Multiple Controllers Not Working: Fix No Input at Menu"
seo_description: "Controller not detected in Batocera? Follow this technician's step-by-step diagnosis for multiple controllers, with exact checks, a verification test, and a rollback note."
keywords:
  - "batocera multiple controllers"
date: 2026-11-22T07:59:16+08:00
publishDate: 2026-11-22T07:59:16+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from USB, the menu appears, but your controller sends no input — and you haven't yet run a controlled diagnosis.

## Start with the physical layer
Unplug every controller except one. Use a rear USB port directly on the PC, not a hub or front-panel extension. Reboot. If the menu now responds, the fault is port or hub related. If it still doesn't, move to the next check.

## Check whether Batocera sees the device
Switch to a keyboard (arrow keys and Enter work in the menu). Open the main menu and look at the controller configuration screen. If the device is listed but unresponsive, the connection is fine and the mapping is wrong. If nothing is listed, the system isn't receiving the device at all — that points to cable, port, or compatibility.

## Isolate one controller before adding more
Test a single known-good controller first. Only after it works should you connect the second. When adding the second, watch whether the first stops responding. If it does, you have a conflict rather than two separate failures. This is the point where **batocera multiple controllers** setups usually go wrong: users connect everything at once and can't tell which device broke the chain.

## Verification test
With one controller connected and detected, open a game list and press a direction. The highlight should move. Then connect the second controller and repeat. Both should respond independently. If only one does, note which port and which controller failed — that's your evidence.

## Rollback note
If a configuration change made things worse, restore your previous controller profile from the backup you made before editing, or remove the last controller mapping and reboot. Don't stack more changes on a broken state.

If the checks above don't isolate the fault,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your port layout and controller models.
