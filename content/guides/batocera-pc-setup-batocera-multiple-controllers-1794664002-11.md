---
title: "Batocera Multiple Controllers Not Working: Fix No Input at the Menu"
description: "Batocera boots from USB but multiple controllers give no input at the menu. Follow these checks to diagnose detection and restore controller input."
seo_title: "Batocera Multiple Controllers Not Detected: Fix No Input at Menu"
seo_description: "Batocera boots from USB but multiple controllers give no input at the menu. Follow these checks to diagnose detection and restore controller input."
keywords:
  - "batocera multiple controllers"
date: 2026-11-21T14:24:39+08:00
publishDate: 2026-11-21T14:24:39+08:00
draft: false
categories:
  - "Game Console Boot"
category_slug: "game-console-boot"
---

You boot Batocera from a USB stick with your controllers connected, but the menu appears and none of them respond.

## Confirm the symptom

First, verify whether Batocera sees any controller at all. Unplug every controller except one, then reboot. If that single controller works, the issue is likely how multiple devices are enumerated or powered. If it still fails, treat it as a single-controller detection problem before continuing.

## Check physical and power basics

Use wired connections or a powered USB hub for testing. Unpowered hubs and front-panel ports often fail to deliver enough current for several controllers. Move the receiver or cable to a rear USB 2.0 port. Result interpretation: if input returns only with the hub or rear port, the original port or hub was the limiting factor.

## Isolate the controller count

Connect one controller, boot, and confirm menu navigation. Then add a second controller and reboot again. If the first works alone but both fail together, the system is not handling **batocera multiple controllers** during input initialization. Test each controller individually to rule out a faulty device.

## Verification test

After any change, reboot fully and press a button on each controller at the menu. Success means every connected controller moves the selection. If only one responds, note which port and connection type work, then repeat with the others.

## Rollback and recovery

If a configuration change causes a regression, restore your previous batocera.conf or controller profile from backup, or reflash the USB image and re-add ROMs. Keep a known-good USB stick unchanged so you can compare behavior.

If these steps do not restore input,

![A mini PC, controller, and monitor running a Batocera game](/images/service-detail-960.webp "Batocera x86 PC and television test setup")

[Ask for help](/#consult) with your controller models, connection types, and port layout.
