---
title: "Batocera Multiple Controllers Not Detected: Diagnose Input Before the Menu"
description: "Batocera boots from USB but no controller input reaches the menu. Run these practical checks to diagnose a controller not detected and restore input."
seo_title: "Batocera Multiple Controllers Not Detected: Fix No Menu Input"
seo_description: "Batocera boots from USB but no controller input reaches the menu. Run these practical checks to diagnose a controller not detected and restore input."
keywords:
  - "batocera multiple controllers"
date: 2026-11-14T19:16:21+08:00
publishDate: 2026-11-14T19:16:21+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You booted Batocera from a USB stick with a controller connected, but the menu appears and nothing responds.

## Confirm the controller is actually seen

Unplug and replug the controller, then watch the boot screen. If any button press skips the splash or changes the menu highlight, input is working and the issue is timing, not detection. If nothing changes, continue.

Try a different USB port, preferably a rear port directly on the motherboard rather than a hub. Reboot. If the menu responds now, the original port or hub was the fault.

## Check power and pairing state

For wired controllers, confirm the cable carries data, not charge only. For wireless ones, confirm the battery is charged and the receiver is seated. A controller that lights up is not proof that Batocera receives input.

## Test with one controller only

Disconnect every other controller and receiver, then reboot with just one. If that single controller works, the problem is how **batocera multiple controllers** are being enumerated at boot. Reconnect them one at a time, rebooting between each, and note which addition breaks input.

## Verification test

After each change, reboot fully and press a direction on the d-pad at the menu. Success means the highlight moves without delay. Repeat with the second controller connected. If both respond, the fix holds.

## Rollback and recovery

If a change makes things worse, return to the last working setup: original port, original cable, one controller. Keep a second USB stick with your previous working Batocera image so you can boot and compare behavior without losing progress.

If the controller still never registers after these checks, stop guessing and get a controlled diagnosis:

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult).
