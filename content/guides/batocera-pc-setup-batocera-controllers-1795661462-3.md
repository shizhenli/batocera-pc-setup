---
title: "Batocera Controllers: Diagnose No Input at the Menu Before Reinstalling"
description: "Batocera boots from USB but your controller sends no input to the menu? Follow this controlled diagnosis to confirm detection, test input, and recover safely."
seo_title: "Batocera Controllers Not Detected: Step-by-Step Input Diagnosis"
seo_description: "Batocera boots from USB but your controller sends no input to the menu? Follow this controlled diagnosis to confirm detection, test input, and recover safely."
keywords:
  - "batocera controllers"
date: 2026-11-28T22:06:10+08:00
publishDate: 2026-11-28T22:06:10+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

## Start with the physical connection

You boot Batocera from a USB stick, the menu appears, but your controller does nothing. Before changing settings, confirm the controller is seen by the PC at all. Unplug and replug the controller, then watch the USB port or controller LED. If it never lights or vibrates, the problem is physical: try a different port (rear ports on a desktop), a different cable, or fresh batteries. A controller that powers on but still gives no input moves to the next check.

## Check detection in Batocera

From the main menu, open Controller Settings and look at the detected device list. If your controller appears but buttons do not register, the mapping is wrong; if nothing appears, Batocera is not receiving the device. Note the exact result: a listed device with dead buttons is a mapping issue, while an empty list points to connection or driver support. This distinction decides your next step and prevents unnecessary reinstalls.

## Verification test

Return to the main menu and press a direction and a confirm button. If the highlight moves and a selection opens, input is restored. If not, reboot once with the controller already connected, then repeat the Controller Settings check. Many **batocera controllers** are detected only when connected before boot.

## Rollback and recovery

If you changed mappings or controller profiles, restore the previous configuration from the backup you made, or reset the controller configuration to defaults. Keep your USB install untouched so you can return to a known working state.

If the controller still never appears, stop guessing and get a focused review of your setup:

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
