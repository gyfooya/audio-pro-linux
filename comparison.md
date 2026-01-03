# Audio Stack Comparison – ASIO / Windows / Linux

This table compares the key characteristics of **ASIO**, the **Windows audio stack**, and **Linux audio stack**, focusing on latency, layers, and typical use cases.

| Feature / API | ASIO | Microsoft Audio Stack | Linux Audio Stack |
|---------------|------|--------------------|-----------------|
| **OS** | Windows only | Windows | Linux |
| **API Type** | Direct hardware driver interface | Layered APIs: MME → DirectSound → WASAPI → WaveRT → XAudio2 | Layered APIs: ALSA → JACK → PulseAudio → PipeWire |
| **Latency** | 1–3 ms (round-trip) | Shared mode: 20–50 ms <br> Exclusive mode: 3–15 ms | ALSA: 1–5 ms <br> JACK: 1–2 ms <br> PipeWire: 2–3 ms |
| **Mixing** | No (direct hardware access) | Shared: Yes <br> Exclusive / WaveRT: No | ALSA direct: No <br> PulseAudio / PipeWire: Yes <br> JACK: No |
| **Hardware Access** | Direct to sound card buffers | Kernel + system mixer layers | Kernel via ALSA; user-space servers via JACK / PipeWire |
| **Multi-channel Support** | Yes | Limited in early APIs; fully supported in WASAPI / WaveRT / XAudio2 | Yes (JACK, ALSA, PipeWire) |
| **Real-time / Low-latency** | Yes | WASAPI Exclusive / WaveRT only | JACK / PipeWire |
| **Desktop Integration** | None (pro-audio focused) | Full Windows desktop support | PulseAudio / PipeWire integrates with desktop; JACK optional for pro audio |
| **Typical Use Cases** | Professional recording, DAWs, live monitoring | Desktop audio, multimedia apps, games | Desktop audio, pro audio, recording, broadcasting |
| **Session / Volume Control** | Handled by DAW / app | WASAPI / Core Audio | PulseAudio / PipeWire |
| **Compatibility** | Requires ASIO driver (hardware or ASIO4ALL) | Built-in to Windows, backward compatible | ALSA universal; JACK / PipeWire optional |

---

### Key Insights

1. **ASIO** is the **benchmark for low-latency professional audio** on Windows.
2. **Windows audio stack** evolved from **high-latency MME → DirectSound → WASAPI → XAudio2**, balancing desktop compatibility and gaming support.
3. **Linux audio stack** is layered: **ALSA** handles kernel drivers, **JACK / PipeWire** handle low-latency audio, **PulseAudio / PipeWire** handle desktop integration.
4. **PipeWire** now unifies Linux desktop + pro audio, providing **similar low-latency behavior to ASIO** while keeping desktop features.

