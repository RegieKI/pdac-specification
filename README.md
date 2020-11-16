# PDAC Specification

Details of PDAC components and build.

* [case PDF](https://github.com/RegieKI/pdac-specification/blob/main/case.pdf)
* [case PNG](https://github.com/RegieKI/pdac-specification/blob/main/case.pdf)

<table>
<thead>
<tr>
<th>Category</th>
<th>Item</th>
<th>Use</th>
<th>Product</th>
<th>Details</th>
<th>Links</th>
</tr>
</thead>
<tbody>
<tr>
<td>Core</td>
<td>Singleboard Computer</td>
<td>Core computer running Linux</td>
<td>Raspberry Pi 4, with 2GB or 4GB RAM</td>
<td>Raspberry Pi OS with kernel update to 5.6 - for stage PDACs we upgrade to 4GB RAM</td>
<td><a href="https://www.reichelt.de/raspberry-pi-4-b-4x-1-5-ghz-4-gb-ram-wlan-bt-rasp-pi-4-b-4gb-p259920.html?search=pi+4" target="_blank">Reichelt</a> / <a href="https://www.berrybase.de/raspberry-pi-co/raspberry-pi/boards/raspberry-pi-4-computer-modell-b-4gb-ram" target="_blank">BerryBase (4GB)</a></td>
</tr>
<tr>
<td>Core</td>
<td>DC Power</td>
<td>Powers device</td>
<td>Raspberry Pi USB-C Power Supply (Official)</td>
<td>Must be official power supply to handle powering extra peripherals (5.1V 3A)</td>
<td><a href="https://www.berrybase.de/raspberry-pi-co/raspberry-pi/stromversorgung/netzteile-fuer-die-steckdose/offizielles-raspberry-pi-usb-c-netzteil-5-1v/3-0a-eu-schwarz" target="_blank">BerryBase</a></td>
</tr>
<tr>
<td>Core</td>
<td>SD Card</td>
<td>Disk storage for operating system</td>
<td>SanDisk Ultra A1 SD Card, 32GB</td>
<td>Standard Class 10 SD card for booting OS</td>
<td><a href="https://www.berrybase.de/raspberry-pi-co/raspberry-pi/speicherkarten/sandisk-extreme-micro-sdhc-a1-uhs-i-u3-speicherkarte-43-adapter-32gb" target="_blank">BerryBase</a></td>
</tr>
<tr>
<td>Core</td>
<td>USB Stick</td>
<td>Disk storage for recorded videos and mutable data</td>
<td>Disk storage for recorded videos and mutable data</td>
<td>Class 10 USB stick plugged into USB 3.0 port. All configuration files and written / live-recorded data goes here.</td>
<td><a href="https://www.berrybase.de/raspberry-pi-co/raspberry-pi/usb-geraete/sandisk-cruzer-ultra-fit-usb-3.1-stick-64gb" target="_blank">BerryBase</a></td>
</tr>
<tr>
<td>Core</td>
<td>Touchscreen</td>
<td>For interacting with PDAC user interface</td>
<td>3.2" JoyIt 3B or Waveshare V2 (same product)</td>
<td>Runs via SPI and GPIO (leaving CVBS / HDMI free). For Raspberry Pi 4 and Buster, <a href="https://github.com/autr/LCD-show" target="_blank">see updated drivers</a></td>
<td><a href="https://www.conrad.de/de/p/joy-it-rb-tft3-2-v2-touchscreen-modul-8-1-cm-3-2-zoll-320-x-240-pixel-passend-fuer-raspberry-pi-mit-hintergrundbeleuch-1380381.html" target="_blank">Conrad</a> / <a href="https://www.reichelt.de/raspberry-pi-shield-display-lcd-touch-3-2-320x240-pixel-xp-rasp-pi-3-2td-p192140.html" target="_blank">Reichelt</a></td>
</tr>
<tr>
<td>Video</td>
<td>Camera Sensor</td>
<td>Camera input</td>
<td>Raspberry Pi HiQ Sensor (IMX477)</td>
<td>Driver must be enabled in config.txt</td>
<td><a href="https://www.berrybase.de/raspberry-pi-co/raspberry-pi/kameras/raspberry-pi-high-quality-kamera" target="_blank">BerryBase</a></td>
</tr>
<tr>
<td>Video</td>
<td>CCTV Lense</td>
<td>Wide-angle video</td>
<td>2.8-12mm / 1:1.4 1/2.5" CS-mount 3MP Lense</td>
<td>Variable wide-angle lense for tight viewing angles (ie. 1-3 metres indoors), with low-light aperture</td>
<td><a href="https://www.qualicam.de/" target="_blank">Qualicam</a> / <a href="mailto:qcone@ueberwachung.tv" target="_blank">Email</a></td>
</tr>
<tr>
<td>Sound</td>
<td>Microphone</td>
<td>Audio input</td>
<td>Rode VideoMicro</td>
<td>High quality passive microphone</td>
<td><a href="http://www.rode.com/microphones/videomicro" target="_blank">Rode</a></td>
</tr>
<tr>
<td>Sound</td>
<td>Soundcard</td>
<td>Microphone input</td>
<td>Sabrent USB Soundcard</td>
<td>Any USB port - optionally set as default sound I/O</td>
<td><a href="https://www.sabrent.com/product/AU-MMSA/usb-external-stereo-3d-sound-adapter-black/#description" target="_blank">Sabrent</a> / <a href="https://www.amazon.de/Sabrent-Soundkarte-External-erforderlich-AU-MMSA/dp/B00IRVQ0F8" target="_blank">Amazon</a></td>
</tr>
<tr>
<td>Sound</td>
<td>Hotshoe Mount</td>
<td>Mounts microphone to PDAC</td>
<td>Affixed to block spacer on topside of PDAC.</td>
<td>Movo HM-S5 Universal Female Hot Shoe (5 pack)</td>
<td><a href="https://www.movophoto.com/products/movo-5-pack-hm-s5-universal-female-hot-shoe-to-male-1-4-tripod-mount-adapt" target="_blank">Movo</a> / <a href="https://www.amazon.de/Movo-HM-S5-Universal-Befestigen-Mikrofonen/dp/B01LDVLBP2/ref=sr_1_1?dchild=1&keywords=Movo+HM-S5+Universal+Female+Hot+Shoe&qid=1596985245&s=diy&sr=1-1" target="_blank">Amazon</a>
</tr>
<tr>
<td>Biometrics</td>
<td>Bio-Sensor</td>
<td>Capturing heartrate via Bluetooth</td>
<td>Miband 3</td>
<td>Must be updated to latest firmware (circa: mid-to-late 2020) via smartphone, then disconnected</td>
<td><a href="https://www.mi.com/in/mi-band-3/" target="_blank">MiBand</a></td>
</tr>
<tr>
<td>ML</td>
<td>Tensor Procressing Unit</td>
<td>Extra computation for machine learning with TensorFlow</td>
<td>Google Coral USB Accelerator</td>
<td>Optional extra for upping FPS on computer vision tasks - using USB 3.0 port, and bundled USB extension cable.</td>
<td><a href="https://coral.ai/products/accelerator" target="_blank">Coral</a> / <a href="https://www.mouser.de/ProductDetail/Coral/G950-06809-01?qs=u16ybLDytRbcxxqFKdbhgQ==&amp;vip=1" target="_blank">Mouser</a></td>
</tr>
<tr>
<td>Misc</td>
<td>Fan</td>
<td>Cooling the CPU</td>
<td>Seamuing Raspberry Pi 4 Fan</td>
<td>General cooling, especially for ML / CV tasks.</td>
<td><a href="https://www.amazon.de/-/en/gp/product/B0836CDZXG/ref=ppx_yo_dt_b_asin_title_o08_s00?ie=UTF8&amp;psc=1" target="_blank">Amazon</a></td>
</tr>
<tr>
<td>Misc</td>
<td>USB Pin Breakout</td>
<td>Powering the fan</td>
<td>USB-Steckverbinder A, Male, Durchsteckmontage</td>
<td>Powers the fan without needing to modify or re-solder ribbon cable (5V USB power).</td>
<td><a href="https://de.rs-online.com/web/p/usb-steckverbinder/1792865?cm_mmc=DE-PLA-DS3A-_-google-_-CSS_DE_DE_Steckverbinder_Whoop-_-(DE:Whoop!)+USB+Steckverbinder-_-1792865&amp;matchtype=&amp;pla-333251409342&amp;gclsrc=ds&amp;gclsrc=ds" target="_blank">RS-Online</a></td>
</tr>
<tr>
<td>Misc</td>
<td>GPIO Ribbon</td>
<td>Connects GPIO pins to 3.5" LCD</td>
<td>Kuman Breadboard Jumper Wires 40pin Male to Female GPIO Cable (15 - 20cm)</td>
<td>Must be F-2-F for unusual LCD connector</td>
<td><a href="https://uk.pi-supply.com/products/40-pin-gpio-male-to-female-ribbon-cable-150mm?lang=de" target="_blank">PiSupply</a> / <a href="https://www.amazon.de/-/en/gp/product/B01L6THEE8/ref=ppx_yo_dt_b_asin_title_o05_s00?ie=UTF8&amp;psc=1" target="_blank">Amazon</a></td>
</tr>
<tr>
<td>Misc</td>
<td>Pin Jumpers</td>
<td>Connecting fan powers and buzzer</td>
<td>See Extra Details</td>
<td>Recommended: rounded housing type, and not fragile square housing (which are easily broken, and rusty inside)</td>
<td>Any</td>
</tr>
<tr>
<td>Case</td>
<td>Back and Front Plate (Pair)</td>
<td>Main body of PDAC shell</td>
<td>CNC'd transluscent acrylic 3mm thick</td>
<td><a href="https://github.com/RegieKI/pdac-specification" target="_blank">See specification PDF</a></td>
<td>N/A</td>
</tr>
<tr>
<td>Case</td>
<td>Block Legs (x 4)</td>
<td>Holds front and back panels in each corner</td>
<td>Drilled wood or acrylic blocks</td>
<td>Recomended to do with easier material than acrylic</td>
<td>N/A</td>
</tr>
<tr>
<td>Case</td>
<td>Block Spacers (x 2 or x 4)</td>
<td>Attaches Hotshoe Mount (on top-side), and tripod mount (on bottom-side)</td>
<td>Drilled wood or acrylic blocks, with threaded holes</td>
<td>Affixed centrally on top and bottom</td>
<td>N/A</td>
</tr>
<tr>
<td>Case</td>
<td>Nuts + Bolts</td>
<td>Assembling PDAC</td>
<td>M2.5x6 Bolts<br />M2.5x8 Bolts<br />M2.5 Nuts<br />M2.5 Washers<br />M3x12 Bolts<br />M3x16 Bolts<br />M3 Nuts<br />M3 Washers<br />M5 Bolts<br />M5 Washers<br />M5 Nuts</td>
<td>Selection of different nuts, bolts and washers for different components.</td>
<td>Any</td>
</tr>
</tbody>
</table>
