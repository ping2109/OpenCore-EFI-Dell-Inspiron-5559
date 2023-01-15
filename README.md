## OpenCore 0.8.8 for Inspiron 5559
Custom OpenCore EFI for Dell Inspiron 5559 on macOS
### Note: Repository is still in development, to get the EFI, please head to the appropriate branch and clone it.

## Navigate
- [BIOS setup](https://github.com/ping2109/Hackintosh-OpenCore-EFI-Dell-Inspiron-5559#bios-setup)
- [Basic installation](https://github.com/ping2109/Hackintosh-OpenCore-EFI-Dell-Inspiron-5559#basic-installation)
- [Vanilla OpenCore - Monterey and older](https://github.com/ping2109/Hackintosh-OpenCore-EFI-Dell-Inspiron-5559#vanilla-opencore---monterey-and-older)
- [Spoofed OpenCore - Ventura and newer](https://github.com/ping2109/Hackintosh-OpenCore-EFI-Dell-Inspiron-5559#spoofed-opencore---ventura-and-newer)
- [Basic fixes](https://github.com/ping2109/Hackintosh-OpenCore-EFI-Dell-Inspiron-5559#basic-fixes)

## BIOS setup
<details>

- Hyper-Threading
- UEFI boot
- DVMT Pre-Allocated(iGPU Memory): 64MB
- SATA Mode: AHCI

</details>


## Basic installation
<details>

- Install USB:
1. Download the zip at releases tab
2. Copy EFI folder to your installer USB's EFI partition
3. Boot and install
- Hard disk:
1. Download the zip at releases tab
2. Use ESP Mounter Pro to mount your disk's EFI parititon
3. Copy EFI folder to your hard disk's EFI partition
4. Reboot

</details>

# Vanilla OpenCore - Monterey and older
<details>

![Ảnh chụp Màn hình 2023-01-15 lúc 13 01 32](https://user-images.githubusercontent.com/75196272/212527020-44b96f69-1f49-436a-922f-f0d8ba4046e8.png)

A/N:**ignore that it says MBP 2017, im just testing my spoofing things, it will be the appropriate 2016 model for you guys on this branch**

| Specs | Info |
|----------|----------|
| **RAM** | 2x DDR3L 1600MHz 4GB |
| **CPU** | Intel Core i5-6200U (2 cores 2 threads) 2.4 GHz |
| **Wi-Fi Card** | Apple AirPort BCM943602CS2 + NGFF Adapter |
| **GPU** | Intel(R) HD Graphics 520 |
| **SMBIOS** | MacBookPro13,1 |

| Feature | Status | Notes |
| ------------- | ------------- | ------------- |
| **Intel iGPU** | ✅ Working |
| **Trackpad I2C** |  ✅ Working | Full gesture support| 
| **iMessages and App Store** | ✅ Working | Follow the OpenCore Guide (#ℹ️-changing-serial-number,-board-serial-number-and-smuuid) |
| **Speakers and Headphones** | ✅ Working | To permanently fix headphones follow this [link](https://github.com/hackintosh-stuff/ComboJack) |
| **Built-in Microphone** | ✅ Working |
| **Webcam** | ✅ Working  |
| **Wi-Fi/BT** | ✅ Working | Since this is an Apple card, it works OOB. You may need [itlwm](https://github.com/OpenIntelWireless/itlwm) for stock AC-3160 card. |
| **SDCard slot** | ✅ Working |
| **Ethernet** | ✅ Working |

</details>

# Spoofed OpenCore - Ventura and newer
- TBD

## Basic fixes
<details>

### 🔈 Audio
Without any modifications, the headphone jack is buggy. External microphones aren't detected and the audio output may randomly stop working or start making weird noises. Sometimes replugging the headphones works, but that's pretty annoying and unreliable. To permanently fix this issue you will have to install [this fork of ComboJack](https://github.com/lvs1974/ComboJack).

### 🔋 Power management
Hibernation is not supported on a Hackintosh and everything related to it should be completely disabled. Disabling additional features prevents random wakeups while the lid is closed. After every update, these settings should be reapplied manually.

```
sudo pmset -a hibernatemode 0
sudo rm -f /var/vm/sleepimage
sudo mkdir /var/vm/sleepimage
sudo pmset -a standby 0
sudo pmset -a autopoweroff 0
sudo pmset -a powernap 0
sudo pmset -a proximitywake 0
sudo pmset -b tcpkeepalive 0 (optional)
```
</details>

## Credits
- [Dortania's OpenCore Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [Tuan Anh](https://github.com/log1cs/) for the .README
