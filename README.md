# Hackintosh-OpenCore-EFI-Dell-Inspiron-5559
Custom OpenCore EFI for Dell Inspiron 5559 (base model) on macOS Hackintosh systems

![image](https://user-images.githubusercontent.com/75196272/162144439-d57de26f-a2c8-4433-9a57-b9bd4e7c4a90.png)

# System's Configuration:
> Base model Dell Inspiron 5559

| Specifications | Details                                                         |
| -------------- | --------------------------------------------------------------- |
| Laptop Model   | Dell Inspiron 5559                                              |
| Processor      | Intel Core i5-6200U @ 2.40GHz dual-core                         |
| RAM            | 4GB (DDR3L 1600MHz)                                 |
| Storage        | Seagate 2.5 inch 500GB Sata III HDD                      |
| Graphics       | Intel HD Graphics 520                                           |
| Display        | 15.6 inches HD+ LCD (1366x768)                       |
| Network Card   | Intel Dual Band Wireless-AC 3160 |

## Tested on:
'macOS Big Sur 11.5.2'

# Basic guides:
- Install USB:
1. Download the zip at releases tab
2. Copy EFI folder to your installer USB's EFI partition
3. Boot and install
- Hard disk:
1. Download the zip at releases tab
2. Use ESP Mounter Pro to mount your disk's EFI parititon
3. Copy EFI folder to your hard disk's EFI partition
4. Reboot and enjoy, no need to re-Snapshot

# Basic fixes:
## Bad earphone quality:
- Go to `System Preferences -> Sound -> Output` and pull the Balance slider to either side, they both work

![Screen Shot 2022-02-18 at 16 33 38](https://user-images.githubusercontent.com/75196272/154656844-c3162ed0-a6dd-4246-b29b-d80845b782b2.png)

## Reversed scrolling on trackpad & mouse:
- This is actually not a bug nor huge issue, it's just a default setting on macOS, you can revert it back by going to `System Preferences -> Trackpad -> Scroll & Zoom -> Scroll direction: Natural` and `System Preferences -> Mouse -> Scroll direction: Natural`

![Screen Shot 2022-02-18 at 15 45 06](https://user-images.githubusercontent.com/75196272/154649088-7de7dbbc-3589-4d20-bceb-5c1977a6098f.png)
![Screen Shot 2022-02-18 at 15 45 12](https://user-images.githubusercontent.com/75196272/154649164-404cf4af-f34b-4727-8392-771332847be2.png)

## ~~Wifi~~
- Fixed on [v2](https://github.com/ping2109/Hackintosh-OpenCore-EFI-Dell-Inspiron-5559/releases/tag/v2)



# Find me at [Telegram](https://t.me/ping2109official) if you have any inquire, feel free to create issues
## Credits goes to [tamht298](https://github.com/tamht298) and [OpenCore](https://dortania.github.io/OpenCore-Install-Guide)
