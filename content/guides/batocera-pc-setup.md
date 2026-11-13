---
title: 'Batocera USB Boot Fails: Check the Image, Mode, and Drive'
description: 'A practical sequence for a Batocera USB that is ignored or black-screens: verify the image, rewrite the drive, match UEFI or legacy mode, then test a controller and one game.'
seo_title: Batocera USB Not Booting? Image and Boot Mode Checks
seo_description: 'A practical sequence for a Batocera USB that is ignored or black-screens: verify the image, rewrite the drive, match UEFI or legacy mode, then test a controller and one game.'
keywords:
- batocera usb not booting
- batocera x86 pc setup
- batocera controller not detected
date: '2026-11-13'
draft: false
categories:
- Game Console Boot
category_slug: game-console-boot
---

<p>A Batocera boot failure is usually in the boot chain, not inside Batocera. Work from the image outward so you can tell whether the PC ever reached the bootloader.</p>
<h2>Before you start</h2><ul>
<li>The exact PC or mini PC model and firmware version</li>
<li>A spare 8 GB or larger USB drive you can erase</li>
<li>The Batocera x86 image and its checksum</li>
<li>One wired controller and one game you own</li>
</ul>
<h2>Step-by-step checks</h2>
<h3>Step 1: Confirm the download and checksum</h3>
<p>Download the x86_64 image from the Batocera release page and compare its published checksum. A truncated download can look like a bad USB even when the writer reports success.</p>
<p><strong>Check:</strong> The checksum matches exactly before you write anything.</p>
<h3>Step 2: Rewrite the drive, do not copy the ISO</h3>
<p>Use balenaEtcher or Raspberry Pi Imager to write the image block by block. In Windows Disk Management, confirm the USB is the disk you are erasing, then let the writer finish and verify its final validation step.</p>
<p><strong>Check:</strong> The writer reports a completed write and validation without errors.</p>
<h3>Step 3: Choose the matching firmware mode</h3>
<p>Open the one-time boot menu and note whether the USB entry is UEFI or legacy. Test UEFI first on a modern PC. If it is ignored, disable Secure Boot and Fast Boot, then retry; only test legacy/CSM when the hardware supports it.</p>
<p><strong>Check:</strong> The Batocera splash or EmulationStation appears instead of Windows.</p>
<h3>Step 4: Test the controller before a game</h3>
<p>With one controller connected, open Controller Settings and map the d-pad, face buttons, start, and hotkey. Save the mapping, then restart the front end and confirm it persists.</p>
<p><strong>Check:</strong> The same controller still navigates after a reboot.</p>
<h3>Step 5: Launch one game and verify output</h3>
<p>Start one known-good game, leave it running for two minutes, and check image, sound, and exit. If it fails, record the emulator and the last on-screen message before changing another setting.</p>
<p><strong>Check:</strong> The game starts, plays with sound, and returns to EmulationStation cleanly.</p>
<h2>Verify the result</h2>
<p>Repeat the boot with the network disconnected and the same controller attached. The PC should reach EmulationStation, recognize the controller, and launch the test game without a second firmware change.</p>
<h2>Rollback</h2>
<p>Restore the original boot order and Secure Boot/Fast Boot settings after testing. Keep the Batocera drive separate so the internal Windows installation is untouched.</p>
<p><a href="/#consult">Ask for help with this exact symptom</a> · <a href="/guides/">All troubleshooting guides</a></p>
