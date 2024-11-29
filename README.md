# Solar-Powered Stipple Light Display
This project was inspired by the venerable [@matth215](https://github.com/matth215)'s [Trichrome Stipple Light project](https://github.com/matth215/Trichrome-Stipple-Light), which was developed as a Stanford [lab64](https://lab64.stanford.edu/home) workshop.
![collage](https://github.com/billyen33/SolarStippleLight/blob/main/img/collage.JPG?raw=true)

https://github.com/user-attachments/assets/7c8972f2-8ed2-4cd0-88ee-94a0132c39c3

![back](https://github.com/billyen33/SolarStippleLight/blob/main/img/back.jpg?raw=true)

## About
[Stippling](https://www.artistsnetwork.com/art-mediums/drawing/get-started-with-stippling/) and [pointillism](https://www.britannica.com/art/pointillism) are both art forms that use dots to create images (black/white and color, respectively), and they can be thought of as the original electronic display. This project borrows from the idea of overlapping dots of different primary colors to create full spectrum of colors in the viewer's eyes. However, instead of using paint, we leverage red, green, and blue LEDs with carefully laser-engraved points on three acrylic sheets to generate full-color images. A fourth acrylic sheet with black paint in the engraved cavities is used to emphasize shadows when the display is unlit. See the image below for a zoomed-in version of the stipple display:

<p align="center">
<img src="https://github.com/billyen33/SolarStippleLight/blob/main/img/zoom.jpg?raw=true" alt="zoomed" width="30%" class="center">
</p>

This project builds on the laser-engraved acrylic stipple sheet and LED method from the [Trichrome Stipple Light workshop](https://github.com/matth215/Trichrome-Stipple-Light) and adds the following functionalities:
- Self-powered operation with solar cells, a LiPo battery, and a maximum power point tracking (MPPT) energy harvester
- Lower cost and power consumption with a fully analog circuit (no MCU)
- Autonmatically turns on in the dark and off when it's bright out to save energy
- Knobs to set RGB LED brightness and threshold light level to turn on
- Integrated battery voltage monitor to help user visualize how much juice is left
- Turbo charging port on the back in case solar isn't enough to charge it

## Bill of Materials
| Name | Description | Amount | Vendor |
| :---: | :---: | :---: | :---: |
| M3 x 6 mm screws | Fasteners for the lid and main circuit board | 6 | [Amazon](https://www.amazon.com/Kozelo-600pcs-Socket-Screws-Assortment/dp/B0DJ3L9RNK/ref=sr_1_1_sspa?sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1) |
| M2.5 x 4 mm screws | Fastener for the voltmeter display | 2 | [Amazon](https://www.amazon.com/Kozelo-560pcs-Socket-Screws-Assortment/dp/B0DKBYP2GR/ref=sr_1_2_sspa?sr=8-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1) |
| Heat-set threaded insert kit | For securing the M3 and M2.5 screws on the box, need **six** M3 inserts and **two** M2.5 inserts | 1 | [Amazon](https://www.amazon.com/Ktehloy-Threaded-Assortment-Printing-Components/dp/B0CLKDPN65/ref=sr_1_1_sspa?sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1) |
| Bayite digital mini voltmeter + display | Measures and displays battery voltage | 1 | [Amazon](https://www.amazon.com/dp/B00YALV0NG) |
| HAWK'S WORK 300 mAh 3.7 V LiPo battery | Battery for the device | 1 | [Amazon](https://www.amazon.com/dp/B09R7F1VV5) |
| BQ25570 breakout board | Solar energy harvesting circuit with built-in buck regulator | 1 | [Amazon](https://www.amazon.com/dp/B0BBLV85L8) |
| MDee 5 V red LED strip | Red LED light | 1 | [Amazon](https://www.amazon.com/dp/B0C991NNP2) |
| MDee 5 V green LED strip | Green LED light | 1 | [Amazon](https://www.amazon.com/dp/B0C991MNTP) |
| MDee 5 V blue LED strip | Blue LED light | 1 | [Amazon](https://www.amazon.com/dp/B0C98Z5FH5) |
| USB-C port (chassis mount) | Connector for USB-C charging cable | 1 | [Amazon](https://www.amazon.com/dp/B0C7CPYL79) |
| 1/8" Thick Acrylic Sheet | For lid and stipple light material | 1 | [Amazon](https://www.amazon.com/12-Clear-Acrylic-Sheet-Plexiglass/dp/B0899K949Z/ref=sr_1_1_sspa?crid=11Z2CKLK9HV9E&keywords=1%2F8%22+acrylic+sheet&qid=1660278591&sprefix=1%2F8+acrylic+sheet%2Caps%2C80&sr=8-1-spons&psc=1) |
| Mini push buttons | For jumpstart button and view voltage button | 2 | [Amazon](https://www.amazon.com/DAOKI-Miniature-Momentary-Tactile-Quality/dp/B01CGMP9GY/ref=sr_1_5?sr=8-5) |
| 6-pin slide switch | Power switch (Link TBD) | 1 | [Amazon](https://www.amazon.com/Micro-Traders-Electronics-8-5x9x3-3mm-Positions/dp/B0CNP77C43/ref=sr_1_10?s=industrial&sr=1-10) |
| 1Meg potentiometer | Knobs to set threshold lighting level | 1 | [Mouser](https://www.mouser.com/ProductDetail/Bourns/3362P-1-101LF?qs=me8TqzrmIYW7oAkP8ZuVYw%3D%3D&mgh=1&gad_source=1) |
| 20k potentiometer | Knobs to adjust the RGB lighting levels | 3 | [DigiKey](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices/PT01-D120D-B203/15903925) |
| TLV3691IDCKR | Ultra-low power comparator to set threshold lighting level for the device to turn on at | 1 | [DigiKey](https://www.digikey.com/en/products/detail/texas-instruments/TLV3691IDCKR/4555468) |
| STLQ020C33R | Ultra-low power 3.3 V LDO with enable pin | 1 | [DigiKey](https://www.digikey.com/en/products/detail/stmicroelectronics/STLQ020C33R/10414574) |
| 0603 resistors | To reset the BQ25570 board's voltage levels, I used 332k x 1, 178k x 2, 316k x 2, 261k x 1, 10k x 1, doesn't need to be 1% but higher precision will let you set more accurate voltages | 6 total, see description | [DigiKey](https://www.digikey.com/en/products/detail/vishay-dale/LTW964TPW06030DB00/4766476?gclsrc=aw.ds&&utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=Pmax_Shopping_DK%2B%20Supplier_ITECH&utm_term=&utm_content=&utm_id=go_cmp-21147141757_adg-_ad-__dev-c_ext-_prd-4766476_sig-CjwKCAiAxqC6BhBcEiwAlXp456aNC652d7kM-kg3F-Dsiou1Lz9xqLb6ytIdaKu2HpGIT2dvs1ZSPhoC474QAvD_BwE&gad_source=1&gclid=CjwKCAiAxqC6BhBcEiwAlXp456aNC652d7kM-kg3F-Dsiou1Lz9xqLb6ytIdaKu2HpGIT2dvs1ZSPhoC474QAvD_BwE&gclsrc=aw.ds) |
| 100 nF capacitors | Decoupling capacitor for the STLQ020C33R | 2 | [Mouser](https://www.mouser.com/ProductDetail/KYOCERA-AVX/KAM15AR71H104KM?qs=Jm2GQyTW%2FbgzS5FHJWrFzQ%3D%3D) |
| Double row header pins | DIY edge-mount connectors for the main circuit board | 1 | [Amazon](https://www.amazon.com/uxcell-Straight-Connector-Arduino-Prototype/dp/B07DJVHXY8/ref=sr_1_3?s=industrial&sr=1-3) |
| Dupont and JST-XH connector kit | Cable and edge mount connectors for the main circuit board | 1 | [Amazon](https://www.amazon.com/Qibaok-Crimping-Ratcheting-Connectors-0-1-0-5mm%C2%B2/dp/B07ZK5F8HP/ref=sr_1_1_sspa?s=industrial&sr=1-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1) |
| Velcro strip with adhesive backing | Connects the LED light panel to main box | 1 | [Amazon](https://www.amazon.com/Art3d-Sticky-Double-Sided-Command-Adhesive/dp/B0B58FGF8H/ref=sr_1_4?s=industrial&sr=1-4) |
| Single-sided FR4 board | Substrate material for DIY PCB | 1 | [Amazon](https://www.amazon.com/uxcell-100x70mm-Double-Sided-Thickness-Prototyping/dp/B07R585RVN/ref=sr_1_1_sspa?s=industrial&sr=1-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1) |
| Thin copper tape | Use with non-copper side of FR4 board to make traces | 1 | [Amazon](https://www.amazon.com/PATIKIL-Conductive-Shielding-Electronics-Grounding/dp/B0BZ51LC5Z/ref=sr_1_3?s=industrial&sr=1-3) |
| 36 AWG enameled wire | Use for generic jumper connections on FR4 board | 1 | [Amazon](https://www.amazon.com/BNTECHGO-AWG-Magnet-Wire-Transformers/dp/B07K4415HM/ref=sr_1_4?s=industrial&sr=1-4) |
| 24 AWG stranded wire | Use for high-current jumper traces | 1 | [Amazon](https://www.amazon.com/Fermerry-Stranded-Electrical-Silicone-Cables/dp/B089CRSLG8/ref=sr_1_4?s=industrial&sr=1-4) |

### Tools Needed:
- Hot glue
- 3D printer (alongside different color PLA plastics and TPU for the legs)
- Laser cutter
- Wire stripper/cutter
- Sharp X-Acto blades to cut copper tape
- Tweezers
- Soldering iron and solder
- M2.5 and M3 screwdrivers (or equivalent if using a different fastener from the one above)
- Electronics/Kapton tape (optional but recommended)
- Recommended but not essential: flux and a microscope
