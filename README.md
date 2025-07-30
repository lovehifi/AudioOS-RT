# AudioOS RT

**AudioOS RT** is a customized, open-source audio operating system built from the sources of [Lyrion (Logitech Media Server)](https://github.com/LMS-Community/slimserver) and [Volumio](https://github.com/volumio/volumio3-backend), using a real-time Linux kernel for ultra-low-latency audio playback.

This system integrates the open-source [Material Skin](https://github.com/CDrummond/lms-material/) web interface, providing a modern and responsive UI for music control.

<p align="center">
  <img src="https://raw.githubusercontent.com/lovehifi/AudioOS-RT/refs/heads/main/ontv.jpg" alt="AudioOS RT UI Screenshot" style="max-width:80%; border-radius: 1rem; box-shadow: 0 2px 16px rgba(0,0,0,0.2);">
</p>
<p align="center">
  <img src="https://raw.githubusercontent.com/lovehifi/AudioOS-RT/refs/heads/main/web_phone.png" alt="On phone" style="max-width:80%; border-radius: 1rem; box-shadow: 0 2px 16px rgba(0,0,0,0.2);">
</p>
<p align="center">
  <img src="https://raw.githubusercontent.com/lovehifi/AudioOS-RT/refs/heads/main/Test_RT.png" alt="Real-time Test" style="max-width:80%; border-radius: 1rem; box-shadow: 0 2px 16px rgba(0,0,0,0.2);">
</p>
---

## Licensing & Credits

- **Lyrion (Logitech Media Server):** GPLv3 license  
- **Volumio Backend:** GPLv3 license  
- **Material Skin for LMS:** MIT & GPLv2 dual-license  
- All modifications and integrations by Quatmo follow the respective open-source licenses of the original projects.

---

## System Information

- **Base:** Debian GNU/Linux 12 (bookworm)
- **Kernel:** 6.12.17-rt9-volumio-1 (PREEMPT_RT)
- **Architecture:** x86_64
- **Maintainer:** Quatmo [@lovehifi](https://github.com/lovehifi)

---

**AudioOS RT** is intended for high-fidelity audio playback and research purposes.  
For details, see the respective licenses of each project.
