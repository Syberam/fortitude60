# Fortitude60 Build Guide
## Parts List

The parts list below describes the list of parts required to build both sides of the keyboard. If you would like to build one side of the keyboard only (single-handed keyboard), please divide the quantity in half.

|Part Name|Model Number|Quantity|Comments|
|------|----|----|----|
|PCB|Fortitude60 Main|2 boards|Included in kit|
|PCB Plate|Fortitude60 Plate|2 plates| Included in kit |
|Microcontroller (MCU)|Beetle USB 32u4|2 pieces | Included in kit (Refer to the “Firmware Burning” section below to find out if you need to burn the firmware yourself.)|
|USB Type-C Connector|AE-USB2.0-TYPE-C|2 pieces |Included in kit |
|Diodes |1N4148 100V200mA|60 pieces| Through-hole (lead type) diodes are included in the kit. You can also use the SMD equivalent, if you prefer. |
|Tactile Switches|2.54mm Pitch|2 pieces| Included in kit|
|TRRS Jack|MJ-4PP-9|2 pieces|Included in kit|
|Rubber Feet|2 large feet + 2 small feet| 4 pieces total|Included in kit|
|TRRS Cable|4-core cable|1 cable|You may use a 3-core calbe if you do not wish to use the [^underglow]function|
|Keyswitches|Cherry MX-compatible|60 pieces|Please select “PCB Mount” option (with pins)|
|Keycaps|Cherry MX-compatible|60 pieces|Cherry-stem compatible|

[^underglow]: Underglow, etc. Backlight and Underglow are treated as separate functions in the MCU.

The parts listed below help you enable optional features, and are not required for basic operation of the keyboard.

|Part Name|Model Number|Quantity|Comments|
|------|----|----|----|
|LED|3mm Bullet Type (Vf=1.4V, 8mA)|60 Pieces|Required if you want to enable the Backlight function|
|Resistor|470ohm, Through Hole (Lead Type) or 3216 (Surface Mount)|60 Pieces|Required if you want to enable the Backlight function|
|Resistor|1kohm, Through Hole (Lead Type) or 3216 (Surface Mount)|2 Pieces|Required if you want to enable the Backlight function|
|Resistor|5.1kohm, Through Hole (Lead Type)|2 Pieces|Required if you are planning on using a USB Type-C to Type-C cable|
|FET|IRLML6344TRPbF(Nch MOSFET)|2 Pieces|Required if you want to enable the Backlight function|
|------|----|----|----|
|LED Tape Light|WS2812B(Full Color LED)|2 Units|Required if you want to enable the Underglow function|
|Wire|Soft(bendable) wire|A few centimeters (or as much as is needed to prevent stress on parts) |Required if you want to enable the Underglow function

## Required Tools

|Part Name|Comments|
|------|----|
|Soldering Iron| A “ceramic heater” type is easy to use. We recommend the “HAKKO FX-600” model|
|Solder|  We recommend “Sparkle Solder” (スパークルハンダ) from the brand “Senju Metals” (千住金属工業)|
|Nipper|We recommend a type that does not produce a gap when close the blade. You can confirm this by closing the blade and then holding it over a light. |
|Tweezers|HOZAN P-891 tweezers are thick and easy to use!|
|Multimeter|Choosing a multimeter with Continuity Check and Diode Testing functions will help make this job much easier.|
|Masking Tape|This can help you temporarily hold pieces in places during the building phase.|
|An Unbreakable Spirit|Please be careful to avoid injury during construction (especially burns from soldering) 👊|


## Assembly

![Printed Circuit Boards](https://i.imgur.com/zFJ0plE.jpg)

Please arrange the circuit boards as indicated in the photograph to identify the left and right sides. In this guide, we will refer to the surface of the PCB to which the keyswitches will be attached to as the "Switch Side" and the surface to which the diodes will be attached  as the "Parts Side".

### Attaching the Diodes

![Diodes（Through-Hole / Lead Type）](https://i.imgur.com/fr5uVkG.jpg)  

![Diodes（SMD）](https://i.imgur.com/vgTHEJx.jpg)

Begin by attaching the diodes to the Parts Side of the PCB, in the mounting locations indicated in Red. For through-hole (lead type) diodes, the part will sit on the Parts Side and the solder should be applied on the Switch Side. For surface-mount diodes, both the solder and part should be applied on the Parts Side. Diodes require the correct polarity to function, so please install the diodes in accordance with the direction markings printed on the circuit board.  In the case that some of the markings are not not fully visible, please be assured that all of them are printed in the same direction on a single board.
(If you are lining up with your board with the photograph, please make sure the marks are pointing downwards.)

You can check that you soldered the diodes to the board correctly by using the "Diode Check" function on your multimeter.

### Attaching the TRRS Jack and Tactile Switch

![TRRS&Switch](https://i.imgur.com/o5jTdhK.jpg)

Align the TRRS jack and tactile switch with their markings on the Parts Side of the board and apply the solder on the Switch Side.

On the v1.0 revision of the PC, the footprint is too small, so you will need to mount the part with one of the pins bent. Begin soldering from the bent pin and then verify all of the connections. On the v1.1 revision of the PCB, this problem has been fixed, so you do not need to bend any pins. On the left-hand half of the keyboard, you can find the PCB version on the Switch Side. On the right hand side, you can find it on the bottom left of the Parts Side.

### (Optional) adding the LEDs for the Backlight

![Backlight Parts](https://i.imgur.com/Do3gXGw.jpg)

Start by attaching the resistors for the LEDs to the Parts Side of the PCB. For Through-Hole (Lead Type) resistors, you will apply the solder from the Switch Side. For SMD resistors, both the part and the solder will be attached to the Parts Side. Resistors do not have polarity, so you do not need to worry about the direction they are placed in. Please note that the resistance value will be different only in one position.

After you have finished soldering the resistors, please use your multimeter to verify their resistance.

Next, you need to attach the FET driver for the LEDs. Since it is a Surface Mount Device, it will be hard to attach. We suggest soldering one leg in place first, then getting to the others. 

### Attaching the Pin Headers

![MCU Pin Header](https://i.imgur.com/oPl7QHQ.jpg)

![MCU Soldered Pin Header](https://i.imgur.com/c0q57L4.jpg)

![USB Pin Header](https://i.imgur.com/N8x93Hu.jpg)

The MCU (Microcontroller) and USB Connector will be attached directly to the pin headers. You will need to separate the pin headers so that each section has enough pins to match the number of holes on each device. You will apply the solder on the Switch Side of the PCB. On each PCB, you will need to solder 3 sets of 6 pins for the MCU, and 2 sets of 2 pins for the USB connector.

``[Caution] Please do not solder the MCU yet!!! You still have a few more steps to complete first.``

### Attaching the Keyswitches

![Attaching the Keyswitches](https://i.imgur.com/TzgloSK.jpg)

You may now begin attaching the keyswitches. Bring the keyswitches through the plate and then align them with the Switch Side of the main PCB. The keystem should extend out of the top of the plate. Please make sure you can see the legs of the switches through the holes on the Parts Side of the PCB, and that they are not bent. As shown in the photograph, during this stage, if you if you also attach part of the case to the PCB  (lightly), soldering will become much easier. Please note: If you attach all of the case at this point, later disassembly will become very difficult. 

Once you have completed checking everything, you can begin soldering the keyswitches from the Parts Side of the PCB.

（Optional）If you will be installing LEDs for the Backlight, the round holes are for the Anode (+) and the square-shaped holes are for the cathode (-). 

### Preparing the MCU

![Identifying the MCUs](https://i.imgur.com/rGWsc2V.jpg)

In the C94 Limited Edition version of the kit (v1.0), the MCU come with the Test Firmware already burned on the device. To keep track of which part will be used for the left-hand side of the keyboard, we attach a yellow sticker to one of the MCUs, as indicated in the photograph.

At this point, you are ready to solder the USB connector to the MCU. To begin, cut out 4 wires that are approximately 5~6cm in length. On both pieces, strip the coating by about 2mm and tin the wires ("tinning" is the process of preparing wires for soldering by applying a small amount of solder to them directly). After this, you will solder the USB Connector to the MCU, with the wires in the middle, as shown in the photograph. Be very careful to confirm that the correct pins are connected to the USB Connector, as a mistake could damage your PC. Perform this check on the MCU as well, since the same error is possible there too.  

For final confirmation, use the "Continuity Test" function on your multimeter to verify that the USB Connector's GND pin is continuous with the MCU's GND pin.

（Optional）A Power LED is attached to the MCU at the position on its circuit board marked with the letter "P". This could be quite bright. If you decide to install the other LEDs on this surface of the keyboard, the colors could interfere with each other. If you would like to prevent this effect, you can remove the Power LED from the MCU's circuit board. 

### Attaching the USB Connector to the MCU

Solder the USB Connector to the Parts Side of the PCB. The USB Connector does not require any specific mounting direction.

Begin by aligning the markings on the Main PCB (ex, 3V3) in the same directions as the markings on the MCU. The footprint of the keyboard is tight, so it is possible to attach the two without solder, however you may run into issues arising from loose or failing contacts. To fix these problems, please consider soldering the connection.

### Optional) Attaching LED Tape for the Underglow Function

If you would like to add Underglow to the unit, please wire LED Tape onto the Main PCB.

### Assembling the Case

The acrylic case is designed with tight fittings, in order to increase its strength when fully assembled (and reduce the need for screws. To begin installation, remove the protective sheets from the acrylic pieces and begin putting together the pieces as shown in the assembly diagram. The longer, mostly flat edges should be at the top of the keyboard, while the uneven edges (the ones with the teeth) should be at the bottom. None of the pieces have the same shape, so it should be difficult to make a mistake when assembling the pieces. If you still feel uncomfortable, try to fit the pieces lightly (without strong force). You may also use a file or sandpaper to adjust the pieces, if you feel it is necessary. Please pay extra attention to pieces that connect to each other, as they can break easily. (The connection for pieces A and B is particularly sensitive, so please attach these pieces first). 

You can now attach the bottom cover of the case. 
By attaching the rubber feet to the cover, you can produce a slight inclination in the keyboard. When you need to disassemble the keyboard, you can do as by inserting a small, dull, pointed object in the gap around the USB connector. This should be one of the easier ways to remove the case.

### Complete!

## Burning the QMK Firmware

A Test Version of the Firmware is available, and you may use it without modification. For the v1.0 revision, it comes pre-burned on the MCU's. For later revisions, you will need to burn it yourself. 

 If you would like to use the optional functions or customize the keymappings, you will need to modify the firmware, as indicated below. You can find the FORTITUDE60 version of the QMK firmware here: 
[https://github.com/qmk/qmk_firmware/tree/master/keyboards/fortitude60](https://github.com/qmk/qmk_firmware/tree/master/keyboards/fortitude60)

To learn how to build and customize QMK, please follow the official guide: [docs.qmk.fm](https://docs.qmk.fm/) 

2. Customizing the Keymap

Please use the values in  ` ` `keymap.c` ` ` in the ` ` `/keymaps/default/` ` ` folder as reference for editing your own keymap. 

2. Enabling the Backlight Function

Add ` ` `BACKLIGHT_ENABLE = yes` ` ` to ` ` `/keymaps/[your keymap]/rules.mk` ` `

This can't be used at the same time as the Underglow function.

2. Enabling the Underglow Function

Add ` ` `RGBLIGHT_ENABLE = yes` ` ` to 
` ` `/keymaps/[your keymap]/rules.mk` ` `

This can not be used at the same time as the Backlight function.
