## Microsoft Audio Stack – Historical Timeline

### 1981 – PC Speaker (BEEPER)
- Present in the first IBM PC 5150
- Magnetic or piezoelectric speaker
- Generates tones by toggling a frequency (PWM)
- No digital audio, no mixing

---

### 1989 – First Widespread Consumer Sound Card
- Sound Blaster 1.0
- Introduced digital audio playback and recording

---

### 1991 – MME (Microsoft Multimedia Environment)
- First standardized Windows audio API
- WaveIn / WaveOut interfaces
- Supports multiple formats (including 44.1 kHz, 16-bit)
- Software-based mixing
- High latency and poor synchronization
- Still supported today for legacy compatibility

---

### 1995 – DirectSound (DirectX Audio)
- Part of Microsoft DirectX
- Designed for low-latency audio (games, multimedia)
- Initially allowed hardware acceleration
- Later routed through system mixer on most systems

---

### 1997 – AC’97 (Audio Codec ’97)
- Standardized PC onboard audio hardware
- Widely adopted on motherboards

---

### 1998 – USB Audio Class
- Introduced with USB 1.1
- Enabled standardized external audio devices

---

### 1998 – WDM Audio (Windows Driver Model)
- Unified driver model for Windows audio
- Introduced Kernel Streaming (KS)
- Included system software mixer (KMixer)
- Miniport driver models:
  - WaveCyclic
  - WavePci

---

### 2004 – High Definition Audio (HDA)
- Successor to AC’97
- Used for onboard, HDMI, and DisplayPort audio
- Generic driver architecture
- Hardware-specific quirks still required

---

### 2004–2005 – UAA (Universal Audio Architecture)
- Standardized HDA driver framework
- Reduced vendor-specific drivers
- Fully integrated starting with Windows Vista

---

### 2007 – Windows Core Audio (Windows Vista)
- Major redesign of the Windows audio stack
- Introduced user-mode audio engine
- New APIs:
  - MMDevice API
  - WASAPI (Windows Audio Session API)
    - Shared mode (system-mixed)
    - Exclusive mode (low-latency, direct access)
  - DeviceTopology API
  - EndpointVolume API
- Per-application volume control

---

### 2007 – WaveRT (Wave Real-Time)
- Low-latency audio driver model
- Designed for modern hardware
- Reduced buffering and CPU usage
- Preferred driver model for pro audio devices

---

### 2008 – XAudio2
- High-level audio engine API
- Designed for games and real-time audio
- Provides:
  - Mixing
  - DSP
  - 3D audio
- Backend evolution:
  - DirectSound (Windows XP)
  - WASAPI (Windows Vista and later)
- Used on Xbox 360, Xbox One, and Windows

---

### 2023 – XAudio2 (Version 2.9)
- Current version on Windows 11
- Fully integrated with modern Windows audio stack
