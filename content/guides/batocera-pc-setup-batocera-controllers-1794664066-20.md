---
title: "Batocera Controllers: No Input at Menu When Booting from USB"
description: "Controller not detected after booting Batocera from USB? Follow these step-by-step checks to restore input at the menu and get back to gaming."
seo_title: "Batocera Controllers Not Detected at Menu: USB Boot Fix"
seo_description: "Controller not detected after booting Batocera from USB? Follow these step-by-step checks to restore input at the menu and get back to gaming."
keywords:
  - "batocera controllers"
date: 2026-11-21T14:27:46+08:00
publishDate: 2026-11-21T14:27:46+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller does nothing—no cursor movement, no button presses.

## Check the physical connection first
Unplug the controller and try a different USB port, preferably one directly on the motherboard (rear ports on a desktop). Avoid unpowered hubs during diagnosis. If the controller has a mode switch (XInput/DInput), set it to XInput. Reboot and watch the boot text: if the controller's LED never lights, the system isn't seeing it at all.

## Confirm Batocera sees the device
At the main menu, plug in a USB keyboard and press F4 to open a terminal. Run `lsusb`. If your controller appears in the list, the hardware is detected but input mapping may be failing. If it does not appear, the issue is physical or port-related—try another cable or controller.

## Test input directly
Still in the terminal, run `evtest` and select the controller's event number. Press buttons and move sticks. If events appear, the controller works and the problem is Batocera's input configuration. Exit with Ctrl+C.

## Reset the controller configuration
From the terminal, run `batocera-config controllers` or navigate to Controller Settings in the menu using the keyboard. Remove any saved mapping for the device, then reboot. On restart, Batocera should prompt you to map buttons—follow the on-screen prompts.

## Verification test
After rebooting, return to the main menu and press a direction on the D-pad. The selection should move immediately. If it does, the fix is complete.

## Rollback note
If the controller still fails, revert any recent changes to `/userdata/system/configs/` by restoring a backup, or reflash the USB with a fresh image to rule out corruption.

If these steps don't restore input,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your `lsusb` output and controller model so we can diagnose further. For persistent issues with **batocera controllers**, a controlled check of the USB port and cable often reveals the culprit.
