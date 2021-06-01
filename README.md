## PDAC Specification

#### Design

PDAC design is based around a Raspberry Pi 4 computer with a 5mm laser-cut acrylic case.

**Iterations**

* *home (1st iteration)* - tripod and accesories, taken home by performers
* *stage (2nd iteration)* - stage version with additional TPU (Tensor Processing Unit)

Improvements on the case leg structure are an inspiration for [laserquest](http://autr.github.io/laserquest).

**Diagrams**

* [PDF](https://github.com/RegieKI/pdac-specification/blob/main/case.pdf)
* [PNG](https://github.com/RegieKI/pdac-specification/blob/main/case.pdf)
* [SVG](https://github.com/RegieKI/pdac-specification/blob/main/case.svg)

!!!include(../pdac-specification/case.svg)!!!

**Components**

Priority is for delivery inside EU - where possible alternatives to Amazon are given.

#### Core

**Singleboard Computer** 

*Use:* core singleboard w. Raspberry Pi OS \
*Product:* Raspberry Pi 4, with 2GB or 4GB RAM \
*Details:* Raspberry Pi OS with kernel update to 5.6 - for stage PDACs we upgrade to 4GB RAM \
*Sources:* [Reichelt](https://www.reichelt.de/raspberry-pi-4-b-4x-1-5-ghz-4-gb-ram-wlan-bt-rasp-pi-4-b-4gb-p259920.html?search=pi+4) / [BerryBase (4GB)](https://www.berrybase.de/raspberry-pi-co/raspberry-pi/boards/raspberry-pi-4-computer-modell-b-4gb-ram)

---

**DC Power** 

*Use:* powers device \
*Product:* Raspberry Pi USB-C Power Supply (Official) \
*Details:* Must be official power supply to handle powering extra peripherals (5.1V 3A) \
*Sources:* [BerryBase](https://www.berrybase.de/raspberry-pi-co/raspberry-pi/stromversorgung/netzteile-fuer-die-steckdose/offizielles-raspberry-pi-usb-c-netzteil-5-1v/3-0a-eu-schwarz)

---

**SD Card** 

*Use:* storage for OS (static) \
*Product:* SanDisk Ultra A1 SD Card, 32GB \
*Details:* Standard Class 10 SD card for booting OS \
*Sources:* [BerryBase](https://www.berrybase.de/raspberry-pi-co/raspberry-pi/speicherkarten/sandisk-extreme-micro-sdhc-a1-uhs-i-u3-speicherkarte-43-adapter-32gb)

---

**USB Stick** 

*Use:* disk storage for recorded videos and mutable data \
*Product:* Disk storage for recorded videos and mutable data \
*Details:* Class 10 USB stick plugged into USB 3.0 port. All configuration files and written / live-recorded data goes here. \
Sources: [BerryBase](https://www.berrybase.de/raspberry-pi-co/raspberry-pi/usb-geraete/sandisk-cruzer-ultra-fit-usb-3.1-stick-64gb)

---

**Touchscreen** 

*Use:* touchscreen user interface \
*Produc*t: 3.2" JoyIt 3B or Waveshare V2 (same product) \
*Detail*s: Runs via SPI and GPIO (leaving CVBS / HDMI free). For Raspberry Pi 4 and Buster, (https://github.com/autr/*LCD-sho*w)see updated drivers</a> \
Sources: [Conrad](https://www.conrad.de/de/p/joy-it-rb-tft3-2-v2-touchscreen-modul-8-1-cm-3-2-zoll-320-x-240-pixel-passend-fuer-raspberry-pi-mit-hintergrundbeleuch-1380381.html) / [Reichelt](https://www.reichelt.de/raspberry-pi-shield-display-lcd-touch-3-2-320x240-pixel-xp-rasp-pi-3-2td-p192140.html)

---

#### Video

**Camera Sensor** 

*Use:* MISI/CSI camera input \
*Product:* Raspberry Pi HiQ Sensor (IMX477) \
*Details:* Driver must be enabled in config.txt \
*Sources:* [BerryBase](https://www.berrybase.de/raspberry-pi-co/raspberry-pi/kameras/raspberry-pi-high-quality-kamera)

---

**CCTV Lense** 

*Use:* wide-angle camera lense for home use \
*Product:* 2.8-12mm / 1:1.4 1/2.5" CS-mount 3MP Lense \
*Details:* Variable wide-angle lense for tight viewing angles (ie. 1-3 metres indoors), with low-light aperture \
*Sources:* [Qualicam](https://www.qualicam.de/) / [Email](mailto:qcone@ueberwachung.tv)

---

#### Sound

**Microphone** 

*Use:* audio input \
*Product:* Rode VideoMicro \
*Details:* High quality passive microphone \
*Sources:* [Rode](http://www.rode.com/microphones/videomicro)

---

**Soundcard** 

*Use:* microphone input \
*Product:* Sabrent USB Soundcard \
*Details:* Any USB port - optionally set as default sound I/O \
*Sources:* [Sabrent](https://www.sabrent.com/product/AU-MMSA/usb-external-stereo-3d-sound-adapter-black/#description) / [Amazon](https://www.amazon.de/Sabrent-Soundkarte-External-erforderlich-AU-MMSA/dp/B00IRVQ0F8)

---

**Hotshoe Mount** 

*Use:* mounting microphone to case \
*Product:* Affixed to block spacer on topside of PDAC. \
*Details:* Movo HM-S5 Universal Female Hot Shoe (5 pack) \
*Sources:* [Movo](https://www.movophoto.com/products/movo-5-pack-hm-s5-universal-female-hot-shoe-to-male-1-4-tripod-mount-adapt) / [Amazon](https://www.amazon.de/Movo-HM-S5-Universal-Befestigen-Mikrofonen/dp/B01LDVLBP2/ref=sr_1_1?dchild=1&keywords=Movo+HM-S5+Universal+Female+Hot+Shoe&qid=1596985245&s=diy&sr=1-1)

---

#### Biometrics

**Bio-Sensor** 

*Use:* heartrate via bluetooth \
*Product:* Miband 3 \
*Details:* Must be updated to latest firmware (circa: mid-to-late 2020) via smartphone, then disconnected \
*Sources:* [MiBand](https://www.mi.com/in/mi-band-3/) \

---

#### ML

**Tensor Procressing Unit** 

*Use:* extra computation for TensorFlow \
*Product:* Google Coral USB Accelerator \
*Details:* Optional extra for upping FPS on computer vision tasks - using USB 3.0 port, and bundled USB extension cable. \
*Sources:* [Coral](https://coral.ai/products/accelerator) / [Mouser](https://www.mouser.de/ProductDetail/Coral/G950-06809-01?qs=u16ybLDytRbcxxqFKdbhgQ==&amp;vip=1)

---

#### Misc

**Fan** 

*Use:* cooling the CPU \
*Product:* Seamuing Raspberry Pi 4 Fan \
*Details:* General cooling, especially for ML / CV tasks. \
*Sources:* [Banggood](https://www.banggood.com/1-Set-2-Pieces-Transparent-4010-Cooling-Fan-Blue-Light-RGB-LED-for-Raspberry-Pi-4B-3B-3B-p-1613882.html) / [Amazon](https://www.amazon.de/-/en/gp/product/B0836CDZXG/ref=ppx_yo_dt_b_asin_title_o08_s00?ie=UTF8&amp;psc=1)

---

**USB Pin Breakout** 

*Use:* powering fan \
*Product:* USB-Steckverbinder A, Male, Durchsteckmontage \
*Details:* Powers the fan without needing to modify or re-solder ribbon cable (5V USB power). \
*Sources:* [RS-Online](https://de.rs-online.com/web/p/usb-steckverbinder/1792865)

---

**GPIO Ribbon** 

*Use:* connects GPIO pins to 3.5" LCD \
*Product:* Kuman Breadboard Jumper Wires 40pin Male to Female GPIO Cable (15 - 20cm) \
*Details:* Must be M2F for unusual LCD connector \
*Sources:* [PiSupply](https://uk.pi-supply.com/products/40-pin-gpio-male-to-female-ribbon-cable-150mm?lang=de) / [Amazon](https://www.amazon.de/-/en/gp/product/B01L6THEE8/ref=ppx_yo_dt_b_asin_title_o05_s00?ie=UTF8&amp;psc=1)

---

**Pin Jumpers** 

*Use:* connecting GPIO to fans and buzzer \
*Product:* AZDelivery (see details) \
*Details:* Recommended: rounded housing type, and not fragile square housing (which are easily broken, and rusty inside) \
*Sources:* Any

---

#### Case

**Back and Front Plate (Pair)** 

*Use:* main body of case shell \
*Product:* CNC'd transluscent acrylic 3mm thick \
*Details:* [pdac-specification](https://github.com/RegieKI/pdac-specification) \
*Sources:* N/A

---

**Block Legs** 

*Use:* holds front and back panels in each corner - comes in set of 4 legs \
*Product:* Drilled wood or acrylic blocks \
*Details:* Recomended to do with easier material than acrylic \
*Sources:* N/A

---

**Block Spacers** 

*Use:* attaches Hotshoe Mount (on top-side), and tripod mount (on bottom-side) - comes in a set of 4 blocks \
*Product:* Drilled wood or acrylic blocks, with threaded holes \
*Details:* Affixed centrally on top and bottom \
*Sources:* N/A

---

**Nuts + Bolts** 

*Use:* assembling PDAC \
*Product:* M2.5x6 Bolts, M2.5x8 Bolts, M2.5 Nuts, M2.5 Washers, M3x12 Bolts, M3x16 Bolts, M3 Nuts, M3 Washers, M5 Bolts, M5 Washers, M5 Nuts \
*Details:* Selection of different nuts, bolts and washers for different components. \
*Sources:* Any


#### License

[MIT](https://github.com/RegieKI/regieki-docs/blob/main/LICENSE-MIT.md)
