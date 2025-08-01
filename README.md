
# AudioOS RT

**AudioOS RT** is a customised, open-source audio-player OS for x86-64 PCs/NUCs.  
It is built from

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

| File                            | Link                                                                                                          |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| `LyrionRTVolumio_1.4f7.zip`     | <https://drive.google.com/file/d/1PC2QoSamNL9-ymfToYjOjYkiGQWoRSUr/>                                          |

1. Download the **ZIP** archive above.  
2. **Extract** it – you will get `LyrionRTVolumio_1.4f7.img`.  


---

## 2  Flash to USB (≥ 16 GB)

### Windows — Rufus

1. *Device* ▸ choose your USB stick  
2. **SELECT** ▸ open the extracted `LyrionRTVolumio_1.4f7.img`  
3. Keep GPT + UEFI defaults → **START**  
4. Wait for **READY**, then eject the stick

### Linux / macOS — balenaEtcher

1. **Flash from file** ▸ select `LyrionRTVolumio_1.4f7.img`  
2. **Select target** ▸ pick the USB stick  
3. **Flash** → eject when done

---

## 3  First boot & network

1. Boot the PC from the stick (F8/F12/ESC)  
2. **Menu ▸ Network Settings** → connect Ethernet or join Wi-Fi  
3. Note the IP shown in **Network Info**  
4. On another device open `http://<ip>:9000`

### Install to internal drive (optional)

*Menu ▸ System ▸ Install to Disk* — **erases the chosen drive**.

---

## 4  Build the image yourself

```bash
# build host: Debian/Ubuntu with Docker
sudo apt install git curl docker docker-compose
git clone https://github.com/volumio/build-platform-x64
cd build-platform-x64
./mkplatform.sh audioos-rt     # adds PREEMPT_RT + Lyrion patches

# build host: Debian/Ubuntu with Docker
sudo apt install git curl docker docker-compose
git clone https://github.com/volumio/build-platform-x64
cd build-platform-x64
./mkplatform.sh audioos-rt     # adds PREEMPT_RT + Lyrion patches
````

Reference projects:

* [https://github.com/moode-player/moode](https://github.com/moode-player/moode)
* [https://github.com/moode-player/imgbuild](https://github.com/moode-player/imgbuild)

---

## 5  Disclaimer & Limitation of Liability

*(GPL-3.0 §§ 15–16, reproduced verbatim)*

> **15. Disclaimer of Warranty.**
> **THERE IS NO WARRANTY FOR THE PROGRAM**, TO THE EXTENT PERMITTED BY APPLICABLE LAW.
> … *(full text unchanged)* …
>
> **16. Limitation of Liability.**
> … *(full text unchanged)* …

Using PREEMPT\_RT kernels, modifying firmware, or disabling power-management
**may damage hardware or void warranties**. Proceed at your own risk.

AudioOS RT is **not affiliated** with Logitech, Volumio SRL, or any trademark owner.
All trademarks remain property of their respective holders.

---

## 6  Licensing & Credits

| Component                       | License       | Upstream                                                                                           |
| ------------------------------- | ------------- | -------------------------------------------------------------------------------------------------- |
| Lyrion (Logitech Media Server)  | GPL-3.0       | [https://github.com/LMS-Community/slimserver](https://github.com/LMS-Community/slimserver)         |
| Volumio backend & build scripts | GPL-3.0       | [https://github.com/volumio/volumio3-backend](https://github.com/volumio/volumio3-backend)         |
| Volumio build-platform-x64      | GPL-3.0       | [https://github.com/volumio/build-platform-x64](https://github.com/volumio/build-platform-x64)     |
| Material Skin UI                | MIT / GPL-2.0 | [https://github.com/CDrummond/lms-material/](https://github.com/CDrummond/lms-material/)           |
| PREEMPT\_RT patch-set           | GPL-2.0       | [https://wiki.linuxfoundation.org/realtime/start](https://wiki.linuxfoundation.org/realtime/start) |
| Integration, packaging & docs   | GPL-3.0       | © 2024-2025 Quatmo                                                                                 |

See each repository for complete licence texts.

---

## 7  System info

| Item         | Value                                                               |
| ------------ | ------------------------------------------------------------------- |
| Base OS      | Debian 12 (bookworm)                                                |
| Kernel       | 6.12.17-rt9-volumio-1 (PREEMPT\_RT)                                 |
| Architecture | x86-64                                                              |
| Maintainer   | Quatmo — [https://github.com/lovehifi](https://github.com/lovehifi) |

---

## 8  Thank you!


```
```
