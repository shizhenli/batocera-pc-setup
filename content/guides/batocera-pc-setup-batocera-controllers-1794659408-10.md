---
title: "Batocera Controller Not Detected: Restore Input at the Menu"
description: "Fix Batocera controllers not detected at the menu when booting from USB. Step-by-step checks for USB port, cable, mode, and a verification test."
seo_title: "Batocera Controllers Not Detected: Fix No Input at the Menu"
seo_description: "Fix Batocera controllers not detected at the menu when booting from USB. Step-by-step checks for USB port, cable, mode, and a verification test."
keywords:
  - "batocera controllers"
date: 2026-11-17T09:59:18+08:00
publishDate: 2026-11-17T09:59:18+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller does nothing, and you are stuck before any controlled diagnosis.

## Check the physical connection first
Unplug the controller and try a different USB port, preferably one directly on the PC rather than a hub. If it is wireless, replace the batteries or charge it, then re-pair. For wired pads, swap the cable if it detaches. Result to expect: the controller's LED should light or stay solid, and Batocera should show a brief input prompt when you press a button. If nothing lights, the fault is power or cable, not Batocera.

## Confirm the controller mode
Many pads default to a mode Windows prefers. Hold the mode or home button until the LED changes, or use the manufacturer's combo to switch to XInput or DirectInput. Then press a button at the menu. If the menu responds, the mode was the issue. If it still does not, move on.

## Rule out the USB boot environment
Shut down, remove the USB stick, and boot the same PC into its normal OS. Connect the controller there. If it works, the hardware is fine and the problem is Batocera's input detection during USB boot. If it fails there too, replace the controller or cable before changing any settings.

## Verification test
Reboot Batocera from USB, wait for the menu, and press a directional button. The highlight should move. Then press the confirm button and open a submenu. If both work, input is restored. If only some buttons work, reconfigure the pad in the controller settings.

## Rollback note
If you changed controller settings, return them to default before retesting. Keep a second known-good controller handy so you can always reach the menu and undo changes. For deeper diagnosis,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).

If input still fails, the issue is likely **batocera controllers** detection at the USB boot stage, not your pad.
