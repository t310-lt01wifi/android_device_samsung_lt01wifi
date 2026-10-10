# LineageOS 14.1 for Samsung Galaxy Tab 3 8.0 Wi-Fi (SM-T310 / lt01wifi)

Custom LineageOS 14.1 (Android 7.1.2 Nougat) build for the Samsung Galaxy Tab 3 8.0 Wi-Fi (`SM-T310` / `lt01wifi`) featuring native **USB MIDI Gadget & Host** support, **Android Open Accessory (AOA)**, and **Simultaneous OTG Charging (ACA mode)**.

---

## 📱 Device Specifications

| Feature | Specification |
| :--- | :--- |
| **Model** | Samsung Galaxy Tab 3 8.0 Wi-Fi (`SM-T310` / `lt01wifi`) |
| **SoC** | Samsung Exynos 4212 Dual-core 1.5 GHz Cortex-A9 |
| **GPU** | Mali-400 MP4 |
| **RAM** | 1.5 GB |
| **Display** | 8.0" WXGA (1280x800) TFT LCD |
| **Kernel** | Linux 3.0.101 (smdk4x12) |
| **Android Version** | 7.1.2 (LineageOS 14.1 UNOFFICIAL) |

---

## ✨ Key Features & Enhancements

1. **USB MIDI Gadget & Host Support**:
   - **Gadget Mode (Device)**: Connect your tablet directly to a PC/Mac/DAW via USB and select **MIDI** in USB preferences or Developer Options. The tablet enumerates as an ALSA MIDI soundcard/controller.
   - **Host Mode**: Connect USB MIDI keyboards, sequencers, or controllers via an OTG adapter.
   - Full Android MIDI API support (`android.software.midi.xml` declared).

2. **Android Open Accessory (AOA) & Automotive Integration**:
   - Integrated init triggers for `accessory`, `accessory,adb`, and `audio_source`.
   - Compatible with **OpenHeadUnit** and Android Auto vehicle setups.

3. **Simultaneous OTG Host & Battery Charging (ACA Mode / Y-Cable)**:
   - Patched MAX77693 MUIC driver (`drivers/muic/max77693-muic.c`) to maintain VBUS charging active when OTG Host mode is active.
   - Perfect for in-dash automotive mounts and fixed DAW studio docks using a powered micro-USB Y-cable.

---

## 📥 Downloads & Installation

Download the latest build from the [GitHub Releases](https://github.com/t310-lt01wifi/android_device_samsung_lt01wifi/releases) page.

### Installation Instructions (TWRP):
1. Boot into TWRP Recovery (Power + Volume Up + Home).
2. Create a full backup of your current partitions (recommended).
3. Perform a **Wipe** -> **Advanced Wipe** (select System, Data, Cache, Dalvik / ART Cache).
4. **Install** -> Select `lineage-14.1-*-UNOFFICIAL-lt01wifi.zip`.
5. *(Optional)* Install OpenGApps (`ARM` -> `Android 7.1` -> `Pico`).
6. Reboot to System.

---

## 🔨 Building from Source

Refer to [t310-lt01wifi/local_manifests](https://github.com/t310-lt01wifi/local_manifests) for full manifest and compilation instructions.

---

## 👥 Credits & Acknowledgements

- **LineageOS Team** & CyanogenMod
- **retiredtab** & **gr8nole** for base device and kernel trees
- Exynos 4212 / SM-T310 community contributors
