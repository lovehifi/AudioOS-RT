# **AudioOS RT**  
*A custom, real-time Linux music-server & player image that bundles **Lyrion** and **Volumio** on a **PREEMPT_RT** kernel for x86-64 PCs/NUCs/MAC (Intel).*

If you're looking for a way to turn your computer into a music player with a familiar desktop interface — where you can hit play on YouTube Music, watch music videos or browse news websites while listening to music from Lyrion (connected to your hard drive or NAS), and enjoy many built-in features like Roon Server, HQPlayer, UPnP, and more — you've just found it.
AudioOS with a Desktop GUI.*

## Key capabilities – What’s inside?

- **Real-time audio core**  
  *PREEMPT_RT 6.12.17* tuned by the **Lyrion SQ** patch-set → lower latency, less jitter, cleaner sound.

- **Personal music library manager**  
  Scan and play files from internal SSD/HDD **or** household NAS (CIFS / NFS).

- **Streaming** 
  • YouTube Music · YouTube Video · Tidal · Qobuz · Spotify.

- **Server bridges**  
  • Roon Core Server
  • HQPlayer (port 8088, user name: hqplayer, pass: hqplayer)
  • UPnP GStreamer renderer (works with BubbleUPnP, mconnect Player, etc.).

- **Offline / Hotspot mode**  
  No Internet? Enable the PC’s own Wi-Fi AP and control everything from your phone.

- **Next-gen audio transports**  
  **Diretta Host** and **AoE Vsound Netmap** for bit-perfect, low-CPU LAN streaming.

- **Universal web control**  
  Open **`http://<your-PC-IP>:9000`** on any phone, tablet or desktop → Material Skin UI.

- **Live-USB with persistence**  
  Boots directly from USB; when you’re happy, install to SSD/HDD with one menu click.

- **Built-in real-time test web tool** – run *cyclictest* & *jitterdebugger* from the browser to verify kernel latency in-situ.



* [**Lyrion (Logitech Media Server)**](https://github.com/LMS-Community/slimserver)
* [**Volumio backend**](https://github.com/volumio/volumio3-backend)
* a real-time Linux kernel (**PREEMPT_RT**)
* the [**Material Skin**](https://github.com/CDrummond/lms-material/) web UI.

<p align="center">
  <img src="https://raw.githubusercontent.com/lovehifi/AudioOS-RT/refs/heads/main/images/desktop.jpg"  width="75%" alt="Material Skin UI"><br><br>
 <img src="https://raw.githubusercontent.com/lovehifi/AudioOS-RT/refs/heads/main/images/audio-out.jpg"  width="75%" alt="Material Skin UI"><br><br>
  <img src="https://raw.githubusercontent.com/lovehifi/AudioOS-RT/refs/heads/main/images/web_phone.png" width="60%" alt="Control on phone"><br><br>
  <img src="https://raw.githubusercontent.com/lovehifi/AudioOS-RT/refs/heads/main/images/Test_RT.png"  width="65%" alt="Real-time latency test"><br><br>
  <img src="https://raw.githubusercontent.com/lovehifi/AudioOS-RT/refs/heads/main/images/UI.png"       width="75%" alt="Extra UI view">
</p>

---

## 1  Download

| File                        | Link                                                                                                  |
|-----------------------------|--------------------------------------------------------------------------------------------------------|
| `LyrionRTVolumio_1.5.02.zip` | <https://drive.google.com/file/d/1jw50qbKKp5P1nQnIEZ1vhNg21kZhKbRS/>                                   |

---

1. Download the **ZIP** archive.  
2. **Extract** → `LyrionRTVolumio_1.5.02.img`.
Enjoy it!


## 2  Flash to USB (≥ 16 GB)

### Windows — Rufus or balenaEtcher

1. *Device* ▸ select USB stick  
2. **SELECT** ▸ open `LyrionRTVolumio_1.4f7.img`  
3. Keep GPT + UEFI defaults → **START**  
4. Wait for **READY** → eject stick

### Linux / macOS — balenaEtcher

1. **Flash from file** ▸ choose `LyrionRTVolumio_1.4f7.img`  
2. **Select target** ▸ USB stick  
3. **Flash** → eject when done

---

## 3  First boot & network

1. Boot PC from USB (F8 / F12 / ESC)  
2. **Menu ▸ Network Settings** → plug Ethernet or join Wi-Fi  
3. Note IP in **Network Info**  
4. On another device open `http://<ip>:9000`

### Install to internal drive (optional)

*Menu ▸ System ▸ Install to Disk* — **erases the chosen drive**.

---

## 4  Source & build tools

- **Volumio build recipe:** <https://github.com/volumio/build-platform-x64>  
- **Real-time test GUI (cyclictest + jitterdebugger):** <https://github.com/lovehifi/audio-rt-tester>


---

### Enjoy it!
<p align="left">
  <a href="https://buymeacoffee.com/lovehifi" target="_blank">
    <img src="https://img.shields.io/badge/Buy%20me%20a%20coffee-ffdd00?logo=buymeacoffee&logoColor=black"
         alt="Buy Me a Coffee">
  </a>
  <br><br>
<a href="https://buymeacoffee.com/lovehifi" target="_blank">
  <img src="images/bmc_qr.png" width="140" alt="Buy Me a Coffee QR">
  </a>
</p>

---

## 5  Disclaimer & Limitation of Liability  
*(GPL-3.0 §§ 15 – 16, reproduced verbatim)*

> **15. Disclaimer of Warranty.**  
> **THERE IS NO WARRANTY FOR THE PROGRAM**, TO THE EXTENT PERMITTED BY APPLICABLE LAW.  
> EXCEPT WHEN OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER  
> PARTIES PROVIDE THE PROGRAM “AS IS” WITHOUT WARRANTY OF ANY KIND,  
> EITHER EXPRESSED OR IMPLIED, INCLUDING, BUT NOT LIMITED TO,  
> THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.  
> THE ENTIRE RISK AS TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU.  
> SHOULD THE PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY  
> SERVICING, REPAIR OR CORRECTION.  
>
> **16. Limitation of Liability.**  
> IN NO EVENT, UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING,  
> SHALL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MODIFIES AND/OR  
> CONVEYS THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES,  
> INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES  
> ARISING OUT OF THE USE OR INABILITY TO USE THE PROGRAM  
> (INCLUDING BUT NOT LIMITED TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE  
> OR LOSSES SUSTAINED BY YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM  
> TO OPERATE WITH ANY OTHER PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY  
> HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.


AudioOS RT is **not affiliated** with Lyrion, Volumio SRL or any trademark owner.  
All trademarks remain the property of their respective holders.

---

## 6  Licensing & Credits

| Component                       | License       | Upstream                                                                                           |
|---------------------------------|---------------|----------------------------------------------------------------------------------------------------|
| Lyrion (Logitech Media Server)  | GPL-3.0       | <https://github.com/LMS-Community/slimserver>                                                      |
| Volumio backend & build scripts | GPL-3.0       | <https://github.com/volumio/volumio3-backend>                                                      |
| Volumio build-platform-x64      | GPL-3.0       | <https://github.com/volumio/build-platform-x64>                                                    |
| Material Skin UI                | MIT / GPL-2.0 | <https://github.com/CDrummond/lms-material/>                                                       |
| Youtube-music plugin            | MIT           | <https://github.com/th-ch/youtube-music>                                                           |
| Tidal-hifi (HiFi streaming )    | GPL-3.0       | <https://github.com/Mastermindzh/tidal-hifi>                                                       |
| Gmrender-resurrect (UPnP)       | GPL-2.0       | <https://github.com/hzeller/gmrender-resurrect>                                                    |
| PREEMPT_RT patch-set            | GPL-2.0       | <https://wiki.linuxfoundation.org/realtime/start>                                                  |
| Integration                     | GPL-3.0       | © 2024-2025 Quatmo                                                                                 |

See each repository for complete licence texts.

---

## 7  System info

| Item         | Value                              |
|--------------|------------------------------------|
| Base OS      | Debian 12 (bookworm)               |
| Kernel       | 6.12.17-rt9-volumio-1 (PREEMPT_RT) |
| Architecture | x86-64                             |
| Maintainer   | Quatmo — <https://github.com/lovehifi> |

---

## Thank you!
