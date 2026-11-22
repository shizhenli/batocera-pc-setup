---
title: "Batocera Controllers Not Detected: Diagnose Input Before the Menu"
description: "Troubleshoot Batocera controllers not detected at the menu when booting from USB. Step-by-step checks to restore input and verify the controller works."
seo_title: "Batocera Controllers Not Detected: Fix No Input at the Menu"
seo_description: "Troubleshoot Batocera controllers not detected at the menu when booting from USB. Step-by-step checks to restore input and verify the controller works."
keywords:
  - "batocera controllers"
date: 2026-11-22T11:59:18+08:00
publishDate: 2026-11-22T11:59:18+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick, the menu appears, but your controller does nothing—no cursor movement, no button presses—so you are stuck before you can even run a proper diagnosis.

## Check the physical connection first

Unplug the controller and plug it into a different USB port, preferably a rear port directly on the motherboard rather than a hub or front-panel extension. If it is a wireless dongle, move it to another port and remove any USB hub. Then reboot Batocera and watch the menu. If the controller now responds, the original port or hub was the problem.

## Interpret what Batocera reports

If there is still no input, look at the controller configuration screen. A controller listed there but unresponsive usually means a mapping or driver issue; a controller not listed at all points to a connection or power problem. Try a different cable if the controller is wired, and confirm the controller works on another device. If it fails there too, the controller itself is the fault.

## Verification test

After any change, reboot and press a direction on the D-pad at the main menu. The highlight should move immediately. Open the controller settings and confirm the device appears and responds to button presses. If both pass, input is restored.

## Rollback and recovery

If a change makes things worse, reconnect the controller to its original port and reboot. For persistent mapping problems, remove the controller configuration for that device and let Batocera recreate it on the next boot.

If these checks leave you stuck,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your controller model and port details. For more on **batocera controllers**, confirm the device is seen before changing settings.
