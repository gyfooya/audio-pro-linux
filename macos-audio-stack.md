# Macintosh / macOS Audio Stack – Historical Timeline

The macOS audio stack has evolved over decades, from early Macintosh computers to modern Core Audio.  
It balances **low-latency pro audio**, multimedia support, and desktop integration.

---

### 1984 – Macintosh 128K
- First Macintosh computers
- Sound hardware limited to **one-channel 8-bit output** (built-in speaker)
- No standard audio APIs for developers
- Tone generation via simple system calls

---

### 1989 – Sound Manager 1.0
- Early Macintosh audio API
- Supported playback of sampled audio and system sounds
- Limited to **one audio channel per device**
- Targeted multimedia applications and games

---

### 1991 – Sound Manager 2.0
- Added support for **multi-channel output**
- Introduced **system-level mixing**
- Enabled playback of multiple sounds simultaneously
- Still high-latency for professional audio

---

### 1998 – QuickTime Audio
- Integration with **QuickTime multimedia framework**
- Provided standardized audio I/O for applications
- Supported multiple formats, compression, and streaming
- Enhanced synchronization with video

---

### 2000 – Core Audio Introduced (Mac OS X 10.0)
- Major architectural overhaul
- Provides **low-latency, high-quality audio**
- Features:
  - Per-application audio streams
  - Real-time mixing
  - Multi-channel support
  - MIDI integration
- Designed for both **professional audio** and **desktop multimedia**

---

### 2004–2010 – Core Audio Maturation
- Introduced support for **Audio Units (AU)** plugins
- Enhanced **hardware abstraction**
- Full support for:
  - USB audio devices
  - FireWire audio interfaces
  - Built-in soundcards
- Became the **standard for DAWs on macOS** (Logic Pro, GarageBand, Pro Tools)

---

### 2011 – OS X 10.7 Lion and Later
- Continued low-latency improvements
- Enhanced **64-bit support**
- Support for **aggregate devices** (combine multiple interfaces)
- Full integration with **Core MIDI**

---

### 2015 – Metal and Modern Audio Stack
- Core Audio supports **real-time processing**
- Improved **buffer handling and driver stability**
- Used extensively in professional recording, live performance, and media production

---

### Key Features of macOS Core Audio
- Low-latency, high-fidelity audio
- Real-time system mixing
- Multi-channel I/O
- Audio Units (AU) plugin support
- MIDI support and timing synchronization
- Aggregate device support for multiple audio interfaces

---

### Practical Notes
- **Professional DAWs** on macOS rely on Core Audio (Logic Pro, Ableton Live, Pro Tools)
- **No need for third-party low-latency drivers**; Core Audio provides native low-latency access
- macOS **aggregate devices** allow combining multiple audio interfaces into one logical device

---
