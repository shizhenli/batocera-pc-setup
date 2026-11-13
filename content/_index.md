---
title: Batocera PC Setup
seo_title: Batocera x86 PC Setup Help | USB Boot and Controller Checks
seo_description: 'Remote Batocera help for x86 PCs: USB boot, firmware mode, controller detection, audio, and one game test.'
keywords:
- batocera usb not booting
- batocera x86 pc setup
- batocera controller not detected
hero_kicker: BATOCERA ON X86 HARDWARE
hero_h1: Batocera USB boot fails on your PC?
hero_lead: Get one x86 PC or mini PC booting Batocera from an external drive, then verify the controller, audio, and one game you already own.
hero_proof:
- One x86 PC and one external drive
- Controller and audio checked in Batocera
- Written rollback and boot notes
hero_alt: Batocera game running on a monitor with a controller and mini PC
hero_title: Batocera game running on a monitor with controller and mini PC
body_alt: A mini PC, controller, and monitor running a Batocera game
body_title: Batocera x86 PC and television test setup
body_caption: A successful handover needs a real boot, a detected controller, and one playable game.
failures_kicker: THE THREE FAILURES WE SEE
failures_heading: What is going wrong?
test_kicker: HOW WE TEST
test_heading: Find the failing layer, then prove the fix.
scope_kicker: SERVICE SCOPE
scope_heading: What is included
scope_note: The session covers one agreed device and one verified path. Anything outside the written scope is quoted separately before work starts.
faq_kicker: FAQ
faq_heading: Before you book
consult_heading: Tell us what is happening.
consult_lead: Send the device, software, exact symptom, and what you have already tried. We will confirm scope and a fixed quote before booking.
form_placeholder: Device, software version, exact symptom, and what you have tried.
first_guide_url: /guides/batocera-pc-setup/
symptoms:
- title: The USB drive is ignored
  text: The PC goes straight to Windows or shows a black screen, even when the drive is selected in the boot menu.
- title: Batocera boots, but controls fail
  text: The front end opens, yet the controller is not detected or the buttons map to the wrong actions.
- title: A game will not start
  text: The system list is visible, but the selected game exits to the menu or starts without sound.
checks:
- title: Record the exact boot path
  text: Note the PC model, firmware key, boot-menu entry, and whether the screen stays black or returns to Windows.
- title: Verify the image and writer
  text: Re-download the correct x86 image, compare its checksum, and write it with balenaEtcher or Raspberry Pi Imager. A copied ISO file is not a bootable image.
- title: Match firmware mode
  text: Test UEFI and, only if the PC supports it, legacy/CSM boot. Disable Secure Boot and Fast Boot for the first test, then restore your normal settings after the session.
- title: Prove one game and controller
  text: Boot with one controller attached, configure it in EmulationStation, and launch one known-good game. Confirm video and audio before calling it finished.
included:
- One compatible x86 PC or mini PC
- Boot-media and firmware-mode diagnosis
- One controller and audio check
- One self-supplied game test
excluded:
- Building a complete game library
- ROM acquisition or copyright advice
- Overclocking or hardware repair
- Guaranteed support for every emulator
faqs:
- q: Will this erase my PC?
  a: No. The session uses an external drive and firmware settings. We do not reinstall or wipe the internal Windows drive.
- q: Do I need a specific controller?
  a: Use the controller you already own. A wired Xbox-style controller is the simplest first test; Bluetooth can be checked after the basic boot works.
- q: Can you supply games?
  a: No. You provide one game you are legally entitled to use; the test is only to prove launch, video, audio, and controls.
---
