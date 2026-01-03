# Linux Professional Audio Stack

This repository documents the **history, architecture, and evolution of the Linux audio stack**, from early PC hardware to the modern PipeWire-based ecosystem.

It is intended for:
- Linux users
- Audio enthusiasts
- Developers
- Professional audio (pro-audio) users

---

## Overview

Linux audio has evolved from simple beeps to a unified, low-latency, professional-grade system.

Today’s stack is the result of **40+ years of hardware and software evolution**, combining:
- Kernel-level drivers
- User-space audio servers
- Desktop and professional audio needs

---

## Historical Timeline

### 1981 – PC Speaker (BEEPER)
- Present in the IBM PC 5150
- Magnetic or piezoelectric speaker
- Generates tones by toggling a frequency (PWM)
- No digital audio, no mixing

---

### 1989 – First Widespread Consumer Sound Card
- Sound Blaster 1.0
- Introduced digital audio and FM synthesis to PCs

---

### 1991 – Linux Kernel
- Linux kernel released by Linus Torvalds
- Early audio support relied on OSS

---

### 1992 – OSS (Open Sound System)
- Early Unix and Linux audio subsystem
- Audio exposed via `/dev/dsp`
- Limited mixing and routing
- Originally limited to one sound card
- Default Linux audio system until kernel 2.4

---

### 1997 – AC’97 (Audio Codec ’97)
- Standardized onboard audio hardware
- Widely adopted on PC motherboards

---

### 1998 – USB Audio Class
- Introduced with USB 1.1
- Enabled standardized external audio devices

---

### 1998 – ALSA (Advanced Linux Sound Architecture)
- Development started in 1998
- Merged into Linux kernel 2.5 (2002)
- Fully replaced OSS in kernel 2.6
- Provides:
  - Kernel drivers
  - Low-level audio APIs
- Still used today as the kernel audio layer

---

### 2002 – JACK (Jack Audio Connection Kit)
- Designed for professional, low-latency audio
- Sample-accurate audio routing
- Popular in music production and studios

---

### 2004 – Polypaudio
- Early desktop audio server
- Focused on usability rather than low latency

---

### 2004 – HDA (High Definition Audio)
- Successor to AC’97
- Used for onboard, HDMI, and DisplayPort audio
- Generic drivers with hardware-specific quirks

---

### 2006 – PulseAudio
- Polypaudio renamed to PulseAudio
- Desktop-oriented sound server
- Features:
  - Per-application volume control
  - Network audio
  - Bluetooth support
  - Multi-user capability
- Became the dominant desktop audio server

---

### 2015 – Pinos
- Media routing system
- Initially focused on video

---

### 2017 – PipeWire
- Pinos renamed and extended to support audio
- Unified audio and video server
- Designed to replace:
  - PulseAudio (desktop audio)
  - JACK (professional audio)
- Supports:
  - JACK API
  - PulseAudio API
  - ALSA
  - GStreamer

---

## After 2017 – Modern Linux Audio Era

### 2018–2020 – PipeWire Maturation
- Stable audio support
- Low-latency processing
- JACK and PulseAudio compatibility layers
- Early adoption by pro-audio users and Wayland

---

### 2020 – Wayland & Sandbox Integration
- PipeWire becomes essential for:
  - Wayland screen sharing
  - Secure audio/video capture
- Used by Flatpak and modern browsers

---

### 2021 – First Major Default Adoption
- Fedora 34 switches from PulseAudio to PipeWire
- PipeWire handles:
  - Desktop audio
  - Bluetooth
  - Professional audio workloads

---

### 2022 – PipeWire Becomes the Standard
- Arch Linux recommends PipeWire by default
- Ubuntu begins transition (22.10+)
- WirePlumber introduced as default session manager
- Improved Bluetooth codec support

---

### 2023–Present – Consolidation Phase
- PipeWire considered production-ready
- JACK and PulseAudio enter maintenance mode
- ALSA remains the kernel driver layer
- Focus on:
  - Performance
  - Power efficiency
  - Embedded and mobile use cases

---

## Modern Linux Audio Stack (2025+)

