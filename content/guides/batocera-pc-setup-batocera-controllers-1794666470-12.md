---
title: "Batocera Controllers Not Working at the Menu: A Step-by-Step Diagnosis"
description: "Batocera boots but your controller doesn't respond at the menu? Follow this focused diagnosis to restore input and get back to gaming."
seo_title: "Batocera Controllers Not Detected: Fix No Input at the Menu"
seo_description: "Batocera boots but your controller doesn't respond at the menu? Follow this focused diagnosis to restore input and get back to gaming."
keywords:
  - "batocera controllers"
date: 2026-11-24T09:59:15+08:00
publishDate: 2026-11-24T09:59:15+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You've booted Batocera from USB, the menu appears, but your controller presses do nothing—leaving you stuck before you can even start a game.

## Confirm the controller is seen by the system

First, rule out a dead connection. Unplug and replug the controller, then watch the LED. If it never lights, try a different USB port—preferably one directly on the motherboard, not a hub. For wireless controllers, ensure the receiver is seated and the battery is charged. Next, press a button and check if Batocera's menu reacts at all. If nothing happens, the input isn't reaching the frontend.

## Check Batocera's controller configuration

Boot to the main menu using a keyboard if you have one. Navigate to Controller Settings and look for your device listed. If it's absent, the system isn't detecting it. If present but unresponsive, the mapping may be broken. Select the controller and choose to reconfigure, then follow the on-screen prompts. Pay attention to each button press—if a step doesn't register, the controller may be faulty or the profile corrupted.

## Verify with a simple test

After reconfiguring, return to the main menu and press a direction. If the highlight moves, input is restored. If not, try a different controller to isolate whether the issue is the device or Batocera. A second controller that works confirms the original is the problem.

## Rollback if needed

If changes made things worse, delete the controller profile from the settings and reboot. Batocera will recreate a default profile on next detection.

If these steps don't resolve your **batocera controllers** issue,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) for a guided diagnosis.
