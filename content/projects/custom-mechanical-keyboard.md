+++
title = 'Custom Mechanical Keyboard'
slug = 'custom-mechanical-keyboard'
date = 2026-01-10T12:00:00Z
draft = false
summary = 'A custom Atreus-inspired ergonomic keyboard built with a stainless switch plate, walnut case, and Kailh Bronze switches.'
description = 'Design and fabrication log for a fully custom mechanical keyboard.'
cover_image = '/images/keyboard-cover.svg'
cover_alt = 'Illustration of a custom mechanical keyboard'
tech_stack = ['CNC milling', 'Laser cut steel', 'ATmega32U4', 'Hand wiring']
status = 'Complete'
+++

## Introduction

I spend a lot of time in front of a screen, and that means a lot of time typing. I wanted something smaller, more ergonomic, and more personal than an off-the-shelf keyboard. After researching options in the mechanical keyboard community, I chose an Atreus-style layout as the foundation.

## Design

I customized nearly every major component:

- **Switch plate:** 1.5mm stainless steel with custom cutouts for 2u thumb keys and LEDs.
- **Switches:** Kailh Bronze for short travel and a tactile click.
- **Controller:** Pololu A-Star 32U4 Micro for proven compatibility.
- **Case:** Custom walnut base designed for rigidity and visual contrast.

I also adjusted mounting points and spacing in the plate design to support my keycap/stabilizer decisions.

## Implementation

The build process included switch mounting, diode matrix soldering, hand-wired columns/rows, and controller firmware flashing. The most time-intensive part was finishing the walnut case: insert installation, progressive sanding, and oil/poly top-coat testing.

Once assembled and flashed, each key was tested against a text editor to validate matrix wiring and layer behavior.

## Final Thoughts

This project was a strong lesson in design-for-manufacturing and iteration. If I redo it, I would likely choose a switch where tactile feedback and actuation are better aligned to reduce mis-typing.
