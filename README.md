### Created by Septian Triiriawan Parapak
### 13-June-2020 3.10AM
### Dell Inspiron 14 3459

### Specifications
- CPU : Intel Core i5 6200U Skylake U - Mobile
- GPU : Intel HD 520 ( Integrated )
- RAM : 2 x 4GB DDR3L
- Storage : 240GB SATA3 SSD
- Audio : ALC255
- Wifi : DW1707 ( Qualcomm Atheros AR9565 )
- Monitor : 1366 x 768 (60hz)
- OS : macOS Mojave 10.14.6 ( Olarila )

### What's working ?

- Start, Sleep, Shutdown
- Audio ( Output, Input )
- 3.5mm Jack Port
- Brightness Control
- HDMI ( Display + Audio )
- Network Adapter ( Wifi & Ethernet )
- Touchpad ( Gestures )
- Webcam
- USB Port
- Battery Indicator
- Volume Keys Fn ( F1, F2, F3 )
- Brightness Keys Fn ( S , B )

### What isn't working ?

- Bluetooth
- Dedicated GPU ( Radeon R5 M315 )

Run disablehibernate.command after fresh installation
to disable Hibernate.

Hibernate function not supported
P.S : Check Utility folder

- Fix HDMI ( Fix refresh rate )
Download Display Menu from App Store and set built-in
monitor's refresh rate to 48 and switch back to 60

- Mount EFI Partition
```sudo mkdir /Volumes/EFI```
```sudo mount -t msdos /dev/disk0s1 /Volumes/EFI```
( If you not sure about disk0s1, use ```diskutil list``` )

- Repair Kext Permission
Run Kext Utility everytime S/L/E has been modified

P.S : Kext Utility located at ```Utility``` folder
