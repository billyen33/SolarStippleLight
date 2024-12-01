# 	:crescent_moon: Solar-Powered Stipple Night Lamp 	:crescent_moon:
The Solar-Powered Stipple Night Lamp is a self-powered stipple light display that wonderfully commemorates a memory between you and your loved ones while functioning without external power, and it's sure to be a head-turner in any room! This project was inspired by the venerable [@matth215](https://github.com/matth215)'s [Trichrome Stipple Light project](https://github.com/matth215/Trichrome-Stipple-Light), which was developed as a Stanford [lab64](https://lab64.stanford.edu/home) workshop.
![collage](https://github.com/billyen33/SolarStippleLight/blob/main/img/collage.JPG?raw=true)

https://github.com/user-attachments/assets/7c8972f2-8ed2-4cd0-88ee-94a0132c39c3

![back](https://github.com/billyen33/SolarStippleLight/blob/main/img/back.jpg?raw=true)

I built this as a present for my beautiful grandmother after a family roadtrip (hence the words/engravings are in Chinese), and you can do the same for yours with this guide!

## About
[Stippling](https://www.artistsnetwork.com/art-mediums/drawing/get-started-with-stippling/) and [pointillism](https://www.britannica.com/art/pointillism) are both art forms that use dots to create images (black/white and color, respectively), and they can be thought of as the original electronic display. This project takes inspiration from the concept of overlapping dots in primary colors to create a full spectrum of colors perceived by the viewer. Instead of paint, we use red, green, and blue LEDs, paired with precisely laser-engraved points on three acrylic sheets, to produce full-color images. A fourth acrylic sheet, coated with black paint in its engraved cavities, enhances shadow details when the display is unlit. The image below shows a close-up of the stipple display for reference:

<p align="center">
<img src="https://github.com/billyen33/SolarStippleLight/blob/main/img/zoom.jpg?raw=true" alt="zoomed" width="30%" class="center">
</p>

This project builds on the laser-engraved acrylic stipple sheet and LED method from the [Trichrome Stipple Light workshop](https://github.com/matth215/Trichrome-Stipple-Light) and adds the following functionalities:
- Self-powered operation with solar cells, a LiPo battery, and a maximum power point tracking (MPPT) energy harvester
- Lower cost and power consumption with a fully analog circuit (no MCU)
- Automatically turns on in the dark and off when it's bright out to save energy
- Knobs to set RGB LED brightness and threshold light level to turn on
- Integrated battery voltage monitor to help users visualize how much juice is left
- Turbo charging port on the back in case solar isn't enough to charge it

## How Do I Generate These Cool Stipple Engravings?

[@matth215](https://github.com/matth215) figured it out. See his [TSL_Preprocessing_Guide](https://github.com/matth215/Trichrome-Stipple-Light/blob/main/TSL_Preprocessing_Guide.pdf) followed by [Section 4 of the TSL_Assembly_Guide](https://github.com/matth215/Trichrome-Stipple-Light/blob/main/TSL_Assembly_Guide%20(1).pdf). Just make your acrylic sheets 4" x 4" x 1/8" if you want to use the CAD files below.

## Bill of Materials
| Name | Description | Amount | Vendor |
| :---: | :---: | :---: | :---: |
| 60 x 60 mm 3 V solar panel | Solar panel for energy harvesting and light sensing | 1 | [xUmp](https://www.xump.com/science/hobby-solar-cell-3v-150mm-60x60mm.cfm?gad_source=1) |
| M3 x 6 mm screws | Fasteners for the lid and main circuit board | 6 | [Amazon](https://www.amazon.com/Kozelo-600pcs-Socket-Screws-Assortment/dp/B0DJ3L9RNK/ref=sr_1_1_sspa?sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1) |
| M2.5 x 4 mm screws | Fastener for the voltmeter display | 2 | [Amazon](https://www.amazon.com/Kozelo-560pcs-Socket-Screws-Assortment/dp/B0DKBYP2GR/ref=sr_1_2_sspa?sr=8-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1) |
| Heat-set threaded insert kit | For securing the M3 and M2.5 screws on the box, need **six** M3 inserts and **two** M2.5 inserts | 1 | [Amazon](https://www.amazon.com/Ktehloy-Threaded-Assortment-Printing-Components/dp/B0CLKDPN65/ref=sr_1_1_sspa?sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1) |
| Bayite digital mini voltmeter + display | Measures and displays battery voltage | 1 | [Amazon](https://www.amazon.com/dp/B00YALV0NG) |
| HAWK'S WORK 300 mAh 3.7 V LiPo battery and charger | Battery for the device | 1 | [Amazon](https://www.amazon.com/dp/B09R7F1VV5) |
| USB-C cable and outlet adapter | For the turbo charging port | 1 | [Amazon](https://www.amazon.com/Phone-Charger-Charging-20W-Block-Type-C/dp/B0CKZ7L8J4/ref=sr_1_1_sspa?sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1) |
| Large heat shrink tubing | For the turbo charger cable | 1 | [Amazon](https://www.amazon.com/Ginsco-580-pcs-Assorted-Sleeving/dp/B01MFA3OFA/ref=sr_1_3?sr=8-3) |
| BQ25570 breakout board | Solar energy harvesting circuit with built-in buck regulator | 1 | [Amazon](https://www.amazon.com/dp/B0BBLV85L8) |
| MDee 5 V red LED strip | Red LED light | 1 | [Amazon](https://www.amazon.com/dp/B0C991NNP2) |
| MDee 5 V green LED strip | Green LED light | 1 | [Amazon](https://www.amazon.com/dp/B0C991MNTP) |
| MDee 5 V blue LED strip | Blue LED light | 1 | [Amazon](https://www.amazon.com/dp/B0C98Z5FH5) |
| USB-C port (chassis mount) | Connector for USB-C charging cable | 1 | [Amazon](https://www.amazon.com/dp/B0C7CPYL79) |
| 1/8" Thick Acrylic Sheet | For lid and stipple light material | 1 | [Amazon](https://www.amazon.com/12-Clear-Acrylic-Sheet-Plexiglass/dp/B0899K949Z/ref=sr_1_1_sspa?crid=11Z2CKLK9HV9E&keywords=1%2F8%22+acrylic+sheet&qid=1660278591&sprefix=1%2F8+acrylic+sheet%2Caps%2C80&sr=8-1-spons&psc=1) |
| Mini push buttons | For jumpstart button and view voltage button | 2 | [Amazon](https://www.amazon.com/DAOKI-Miniature-Momentary-Tactile-Quality/dp/B01CGMP9GY/ref=sr_1_5?sr=8-5) |
| DPDT slide switch | Power switch (Link TBD) | 1 | [Amazon](https://www.amazon.com/Micro-Traders-Electronics-8-5x9x3-3mm-Positions/dp/B0CNP77C43/ref=sr_1_10?s=industrial&sr=1-10) |
| 1Meg potentiometer | Knobs to set threshold lighting level | 1 | [Mouser](https://www.mouser.com/ProductDetail/Bourns/3362P-1-101LF?qs=me8TqzrmIYW7oAkP8ZuVYw%3D%3D&mgh=1&gad_source=1) |
| 20k potentiometer | Knobs to adjust the RGB lighting levels | 3 | [DigiKey](https://www.digikey.com/en/products/detail/same-sky-formerly-cui-devices/PT01-D120D-B203/15903925) |
| TLV3691IDCKR | Ultra-low power comparator to set threshold lighting level for the device to turn on at | 1 | [DigiKey](https://www.digikey.com/en/products/detail/texas-instruments/TLV3691IDCKR/4555468) |
| STLQ020C33R | Ultra-low power 3.3 V LDO with enable pin | 1 | [DigiKey](https://www.digikey.com/en/products/detail/stmicroelectronics/STLQ020C33R/10414574) |
| 0603 resistors | To reset the BQ25570 board's voltage levels, I used 332k x 1, 178k x 2, 316k x 2, 261k x 1, 10k x 1, doesn't need to be 1% but higher precision will let you set more accurate voltages | 6 total, see [BQ25570](https://github.com/billyen33/SolarStippleLight#bq25570) section | [DigiKey](https://www.digikey.com/en/products/detail/vishay-dale/LTW964TPW06030DB00/4766476?gclsrc=aw.ds&&utm_adgroup=&utm_source=google&utm_medium=cpc&utm_campaign=Pmax_Shopping_DK%2B%20Supplier_ITECH&utm_term=&utm_content=&utm_id=go_cmp-21147141757_adg-_ad-__dev-c_ext-_prd-4766476_sig-CjwKCAiAxqC6BhBcEiwAlXp456aNC652d7kM-kg3F-Dsiou1Lz9xqLb6ytIdaKu2HpGIT2dvs1ZSPhoC474QAvD_BwE&gad_source=1&gclid=CjwKCAiAxqC6BhBcEiwAlXp456aNC652d7kM-kg3F-Dsiou1Lz9xqLb6ytIdaKu2HpGIT2dvs1ZSPhoC474QAvD_BwE&gclsrc=aw.ds) |
| 100 nF capacitors | Decoupling capacitor for the STLQ020C33R | 2 | [Mouser](https://www.mouser.com/ProductDetail/KYOCERA-AVX/KAM15AR71H104KM?qs=Jm2GQyTW%2FbgzS5FHJWrFzQ%3D%3D) |
| Double row header pins | DIY edge-mount connectors for the main circuit board | 1 | [Amazon](https://www.amazon.com/uxcell-Straight-Connector-Arduino-Prototype/dp/B07DJVHXY8/ref=sr_1_3?s=industrial&sr=1-3) |
| Dupont and JST-XH connector kit | Cable and edge mount connectors for the main circuit board | 1 | [Amazon](https://www.amazon.com/Qibaok-Crimping-Ratcheting-Connectors-0-1-0-5mm%C2%B2/dp/B07ZK5F8HP/ref=sr_1_1_sspa?s=industrial&sr=1-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1) |
| Velcro strip with adhesive backing | Connects the LED light panel to main box | 1 | [Amazon](https://www.amazon.com/Art3d-Sticky-Double-Sided-Command-Adhesive/dp/B0B58FGF8H/ref=sr_1_4?s=industrial&sr=1-4) |
| Single-sided FR4 board | Substrate material for DIY PCB | 1 | [Amazon](https://www.amazon.com/uxcell-100x70mm-Double-Sided-Thickness-Prototyping/dp/B07R585RVN/ref=sr_1_1_sspa?s=industrial&sr=1-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1) |
| Thin copper tape | Use with non-copper side of FR4 board to make traces | 1 | [Amazon](https://www.amazon.com/PATIKIL-Conductive-Shielding-Electronics-Grounding/dp/B0BZ51LC5Z/ref=sr_1_3?s=industrial&sr=1-3) |
| 36 AWG enameled wire | Use for generic jumper connections on FR4 board, **much** easier to solder than standard 24 AWG wires since the insulation can be melted off instead of stripped | 1 | [Amazon](https://www.amazon.com/BNTECHGO-AWG-Magnet-Wire-Transformers/dp/B07K4415HM/ref=sr_1_4?s=industrial&sr=1-4) |
| 24 AWG stranded wire | Use for high-current jumper traces the 36 AWG wires can't take | 1 | [Amazon](https://www.amazon.com/Fermerry-Stranded-Electrical-Silicone-Cables/dp/B089CRSLG8/ref=sr_1_4?s=industrial&sr=1-4) |

Most of these will be available in typical prototyping/electronics workspaces, so take a look and see what you are missing before you place an order!

### Tools Needed:
- Hot glue and super glue
- FDM 3D printer (alongside different color PLA plastics and TPU for the legs)
- Laser cutter
- Wire stripper/cutter
- Sharp X-Acto blades to cut copper tape
- Tweezers
- Soldering iron and solder
- M2.5 and M3 screwdrivers (or equivalent if using different fasteners from the one above)
- Electronics/Kapton tape (optional but recommended)

_Recommended but not essential:_ flux and a microscope

## Electronics

### Circuit Diagram

![circuit diagram](https://github.com/billyen33/SolarStippleLight/blob/main/img/circuit.png?raw=true)

The entire circuit with the exception of the BQ25570 energy harvestor is turned off when the power DPDT switch is toggled to OFF, so nothing will happen but the battery will still be getting charged by the solar panel/charger. When the switch is toggled to AUTO, the circuit will operate according to the following logic:

- BAT+ < VBAT_OK_PROG (set by Rok1 and Rok2 on BQ25570)
  - V_OK and V_EN pulled to ground
  - OUT+ is disabled and everything is off
- BAT+ > VBAT_OK_HYST (set by Rok1, Rok2, and Rok3 on BQ25570)
  - V_OK and V_EN pulled to VSTOR
  - OUT+ is enabled (voltage set by Rout1 and Rout2 on BQ25570), TLV3691IDCKR and the 1Meg potentiometer are both on
  - If V+ (output of the potentiometer swiper, set by user's threshold knob) > IN+ (output of the solar panel)
    - STLQ020C33R (the 3.3 V LDO) is enabled, RGB LEDs turn on according to the currents set by their respective 20k potentiometers
  - If V+ < IN+
    - STLQ020C33R (the 3.3 V LDO) is disabled, RGB LEDs are off

The battery is always charging from the solar panel as long as there is sufficient ambient light, and the solar panel doubles as a light sensor to turn off the LEDs when it is bright out (IN+ rises above V+). The voltmeter only powers on/read voltage/displays voltage when the push button connecting it to GND is pressed to save power, as it pulls around 51 mW when BAT+ = 4.1 V.

### Wiring Diagram

![wiring diagram](https://github.com/billyen33/SolarStippleLight/blob/main/img/wiring_diagram.jpg?raw=true)

### IRL

![IRL circuit](https://github.com/billyen33/SolarStippleLight/blob/main/img/inside_battery.jpg?raw=true)

A lot of people ask why I used copper tape, FR4, and thin 36 gauge enameled wire to build the circuit with tiny surface mounted parts instead of using large through-hole components or a PCB. It's to show that I care (definitely not because I'm a SMD elitist or I'm too cheap to pay the $20 JLCPCB shipping fee). If you would like to learn this method, check out [this guide](https://halestrom.net/darksleep/blog/039_coppertape/) and [this video](https://www.youtube.com/watch?v=xTkDDCnEdA4). The wiring you see above is likely not optimal, but it works. Feel free to explore any method you choose as long as you stick to the circuit diagram above, the circuit's not too sensitive to parasitics since everything is in DC. If you do use tiny 36 gauge wires like I did, I'd avoid using them where the main LED drive current goes through as they are only rated up to [35 mA for power transmission](https://www.powerstream.com/Wire_Size.htm) and we can get >100 mA when all the LEDs are on maximum brightness. I would recommend cutting out the FR4 board and drilling its mounting holes according to the dimension of the main enclosure box (make sure to include enough room on the sides for the connectors) before soldering on components. I also found it useful to drill an extra hole near the BAT- and BAT+ pins to be able to tape the LiPo battery on the back of the board (see the IRL image above).

### BQ25570

The [BQ25570](https://www.ti.com/lit/ds/symlink/bq25570.pdf?ts=1732850844213&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FBQ25570) is an energy harvester with MPPT and an integrated buck regulator that gives us an adjustable output voltage. To set the output voltage and the minimum/maximum voltage thresholds for our specific battery, we need to swap the 7 SMD resistors on the board. See the image below for where the resistors are (Rov1, Rov2, Rok1, Rok2, Rok3, Rout1, Rout2):

![bq25570](https://github.com/billyen33/SolarStippleLight/blob/main/img/BQ25570.jpg?raw=true)

See the [calculations](https://github.com/billyen33/SolarStippleLight/blob/main/Calculations.xlsx) spreadsheet for how to determine the resistor values, and you can use the values I did as-is for the board to work (though manual tuning may be required to get more exact voltages). You can refer to the [datasheet for the BQ25570 chip](https://www.ti.com/lit/ds/symlink/bq25570.pdf?ts=1732850844213&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FBQ25570) for more detail. If the battery is disconnected from the main circuit board for too long, it is possible for VSTOR to drop below the coldstart voltage and stay there even after the battery is reconnected, making the device take a long time to restarting operation. In that case, just ensure the battery is fully charged and press the jump start push button to quickly make VSTOR = BAT+, and the light should start functioning normally.

### Turbo Charger

If the night lamp is placed in an unfortunate location where it's always in the dark or you want to charge it in a hurry, a USB-C charging port is made available on the back of the device. The charger is the same one that came with the battery from the Amazon link above, but the small 2-pin connector was cut off and replaced with the USB-C cable from the Bill of Materials to create a more user-friendly connector interface. I pried open the USB-A connector box to access the wires and desoldered the original cable before stripping and soldering on the new USB-C one, and covered the circuit with a large heatshrink (ideally use something transluscent so you can see the internal LED) alongside plenty of hot glue to seal everything up. The internal LED light will shine when the battery is charging (see bottom right) and turn off when the battery is full (nominally 4.2 V). If the night lamp is near an outlet it can be permanently plugged in, and the solar cell will just function as a photodiode for light sensing in this case. It should only take a couple hours to fully charge the 300 mAh battery using the charger.

![charger](https://github.com/billyen33/SolarStippleLight/blob/main/img/charger.JPG?raw=true)

## Mechanical

### 3D Printing + Laser Cutting Files

<p align="center">
<img src="https://github.com/user-attachments/assets/87d82aa1-e939-448d-aed1-ec6c13aeaebe" alt="exploded" width="30%" class="center">
</p>

See the [CAD](https://github.com/billyen33/SolarStippleLight/tree/main/CAD) folder for the stl files needed for 3D printing (most parts are in PLA except for the [legs](https://github.com/billyen33/SolarStippleLight/tree/main/CAD/3DPrint/TPU), which are in TPU but can technically be done in PLA as well). The laser cut files' footprints (lines that need to be cut through) are in the [LaserCut](https://github.com/billyen33/SolarStippleLight/tree/main/CAD/LaserCut) folder, and the engravings can be added separately on InkScape after they are generated via [@matt215's instructions](https://github.com/matth215/Trichrome-Stipple-Light/blob/main/TSL_Preprocessing_Guide.pdf). I recommend printing the main enclosure box facing down with tree supports (enabled on build plate only) and 0.1 mm nozzle size, and the others can be done without support. 

### Details for Assembly

The voltmeter's ON button (see Wiring Diagram) is super glued to the inside of the lid, and the button extension (in [CAD/3DPrint/PLA](https://github.com/billyen33/SolarStippleLight/tree/main/CAD/3DPrint/PLA)) is glued to top of the standard push button to make it pressable across the thick acrylic sheet (otherwise a pin or a pencil will be necessary to push it). The LED strips are stuck to the LED mount using the adhesive tape they come with, and the mounting piece adheres to the main box with Velcro strips so it can be removed later if necessary (can replace Velcro with hot glue if you don't want to make it removable). All of the holes on the main enclosure box uses M3 threaded inserts, and the two holes on the LED mount for the voltmeter uses M2.5 inserts. Be careful with how much super glue you add to the button to avoid getting it stuck, and super glue can also be used to keep the other components (potentiometers, switches, etc.) secured if a press fit is not enough (the threshold knob especially would be useful to glue onto the 1Meg potentiometer to prevent it from falling out).

Happy building :)
