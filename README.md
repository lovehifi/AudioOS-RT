AudioOS RT

Custom, real‑time Linux music‑server & player image that bundles Lyrion (Logitech Media Server) and Volumio on a PREEMPT_RT kernel for x86‑64 computers. Built for bit‑perfect, headless playback.

## Key capabilities – What’s inside?

- **Real-time audio core**  
  *PREEMPT_RT 6.12.17* tuned by the **Lyrion SQ** patch-set → lower latency, less jitter, cleaner sound.

- **Personal music library manager**  
  Scan and play files from internal SSD/HDD **or** household NAS (CIFS / NFS).

- **Streaming without ads / QC**  
  YouTube Music · YouTube · Tidal · Qobuz · Spotify – all playable directly from the LMS UI.

- **Server bridges**  
  • Roon Core Server  
  • HQPlayer NAA endpoint  
  • UPnP / GStreamer renderer (works with BubbleUPnP, mconnect Player, etc.).

- **Offline / Hotspot mode**  
  No Internet? Enable the PC’s own Wi-Fi AP and control everything from your phone.

- **Next-gen audio transports**  
  **Diretta** and **AoE Vsound Netmap** for bit-perfect, low-CPU LAN streaming  
  (lighter than HQPlayer’s network mode, keeps sound un-altered).

- **Universal web control**  
  Open **`http://<your-PC-IP>:9000`** on any phone, tablet or desktop → Material Skin UI.

- **Live-USB with persistence**  
  Boots directly from USB; when you’re happy, install to SSD/HDD with one menu click.


* [**Lyrion (Logitech Media Server)**](https://github.com/LMS-Community/slimserver)
* [**Volumio backend**](https://github.com/volumio/volumio3-backend)
* a real-time Linux kernel (**PREEMPT_RT**)
* the [**Material Skin**](https://github.com/CDrummond/lms-material/) web UI.

<p align="center">
  <img src="https://raw.githubusercontent.com/lovehifi/AudioOS-RT/refs/heads/main/Lyrion.png"  width="75%" alt="Material Skin UI"><br><br>
  <img src="https://raw.githubusercontent.com/lovehifi/AudioOS-RT/refs/heads/main/ontv.jpg"   width="75%" alt="AudioOS RT on TV"><br><br>
  <img src="https://raw.githubusercontent.com/lovehifi/AudioOS-RT/refs/heads/main/web_phone.png" width="60%" alt="Control on phone"><br><br>
  <img src="https://raw.githubusercontent.com/lovehifi/AudioOS-RT/refs/heads/main/Test_RT.png"  width="65%" alt="Real-time latency test"><br><br>
  <img src="https://raw.githubusercontent.com/lovehifi/AudioOS-RT/refs/heads/main/UI.png"       width="75%" alt="Extra UI view">
</p>

---

## 1  Download

| File                        | Link                                                                                                  |
|-----------------------------|--------------------------------------------------------------------------------------------------------|
| `LyrionRTVolumio_1.4f7.zip` | <https://drive.google.com/file/d/1PC2QoSamNL9-ymfToYjOjYkiGQWoRSUr/>                                   |

1. Download the **ZIP** archive.  
2. **Extract** → `LyrionRTVolumio_1.4f7.img`.

---

## 2  Flash to USB (≥ 16 GB)

### Windows — Rufus

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

The official build recipe is kept in **Volumio’s** platform tree:  
<https://github.com/volumio/build-platform-x64>.

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

Running PREEMPT_RT kernels, modifying firmware or power settings **may damage
hardware or void warranties**. Proceed at your own risk.

AudioOS RT is **not affiliated** with Logitech, Volumio SRL or any trademark owner.  
All trademarks remain the property of their respective holders.

---

## 6  Licensing & Credits

| Component                       | License       | Upstream                                                                                           |
|---------------------------------|---------------|----------------------------------------------------------------------------------------------------|
| Lyrion (Logitech Media Server)  | GPL-3.0       | <https://github.com/LMS-Community/slimserver>                                                      |
| Volumio backend & build scripts | GPL-3.0       | <https://github.com/volumio/volumio3-backend>                                                      |
| Volumio build-platform-x64      | GPL-3.0       | <https://github.com/volumio/build-platform-x64>                                                    |
| Material Skin UI                | MIT / GPL-2.0 | <https://github.com/CDrummond/lms-material/>                                                       |
| PREEMPT_RT patch-set            | GPL-2.0       | <https://wiki.linuxfoundation.org/realtime/start>                                                  |
| Integration, packaging & docs   | GPL-3.0       | © 2024-2025 Quatmo                                                                                 |

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

## 8  Thank you!
