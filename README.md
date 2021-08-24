# Bootloader-Pic18F2550
Build a bootloader board with the Pic 18f2550, which you will able to program your microcontroller directly from your PC to the board.
This is a small board which use the well know Pic18F2550, this microcontroller is easy to find in the electronic stores and most of the electronics hobbyist have one of them in their stock. So in this opportunite We are going to build a develpment board, which means that will have all the neccesary to work and test our codes and projects.

The board module, with the Bootloader firmware, can work in two modes of operation: "Bootloader" mode in which it is ready to be programmed, and "User" mode in which the application program is automatically executed. Both modes are availableautomaticallyonceweconnectedtheboard.

# MAIN FEATURES
* USB support is the most important feature of self PIC 18f2550; you can have a quick communication with your computer via USB
* Power Led: indicates whether the + 5v USB Supply
* Push button integrated for reset
* Very affordable to find the componets
* Programming by a small aplication from our PCB
* Interfacing via USB HID (Human interface devide)

# SCHEMATIC DIAGRAM
Let's start with the first step which is the circuit diagram, We should consider this schematic circuit as the base, with the minimal required components, so We are free to add other devices to complete our board according our project's needs.
All the components used are very common and easy to find in our local electronic stores.
►The first part of the schematic is the Pic18F2550, which has the Usb interface, that We are doing to use. As you can see most of the pin has tags or names, it will help to identlfy the important pats or errores.
►Also as We well know, when we work with microcontrolers We need to connect the corresponding oscilator circuit (which consist on 2 capacitors 22pF, 1 oscicaltor 20 MHz)
►The other part of the circuit are the capacitor for the USB interface in this oportunity 220nF (the capacitor should be market with the number )
►We have to add now the pin header in our PCB, these header will let us to connect the microcontroller pins with external devices.
►Finally We should consider a tactile button for reseting the board, and also a led indicator in this case the led indicate that the USB conector is suppling +5v.

# PCB LAYOUT
Before We continue with the PCB layout, it is important to indicate that You can use any software for PCB Desing, believe me there are many options, even if you use the best software it will not mean that you are the best pcb desinger, so in this case We are going to use The Altium Designer highly recommended if you want to enter in the pcb design world like a professional.
So after We finished and check our schematic circuit We need to switch from schematic to PCB layout. We can see the PCB with the Ground Plane, this helps for noise filter on the pcb. Also is important to remember that in the case of the microcontroller is necesary to place the crystal and the capacitor the closest possible.
Here after we finish the pcb layout We can get the Gerber files, there are two kind of gerber files we have to pay attention to it, the first GerberX2 and the other Gerber RS274X, most of the manufacturer use the second one Gerber RS274X, in some software we will just GerberX2 and Gerber (In the case of Altium Designer).

# 3D MODEL
One of the features of Altium Designer is the 3D visualization, the 3d visualization is important and it give us the posibility to see and check our PCB and how it would be in real, also it can show us the components distribution and dimensions. Before I did not consider this feature so important, but the 3d visualization can show us if our footprint dimensions are ok, if all the components will be places without touching each other by mistake.
► Also very important to remember, if you are going to add 3d models, be carefull that you add in the Step AP214 format, the others extensions and formats can not work correctly.

# PDF 3D
According to the software that you are using, You can also get the 3d Models, as I commented you before, this board was desinged On the Altium Designer Software who has this nice option to get the 3d pdf, so later you can share with your coworkers or clients to show the advances of the pcb, without the software installed.

# PCB MANUFACTURE
Once we finished our development board; it is time to bring it to life. In order to manufacture our board, We are going to use JLCPB Services.In case that you do not have an account yet, check out the bellow link
►JLCPCB: https://jlcpcb.com/IAT

**How to Order our PCB in JLCPCB?**
Once We are register, and We logged in our account, We are ready to submit an order and receive our board in a very short time. In this case We need to update first the gerber files, which contains all the necesary information to build the pcb, You can get the gerber files in the link bellow.

**Upload your gerber files**

**Indicatethefeatures**
After the upload of our gerber files, We need to indicate the features of the board, in the next picture you can see the options available.

**Add your shipping address** This part is very important, here you should write your currently address, where you would like to receive your pcb prototypes. It is not common but sometimes very rarely, you will need to pay extra feeds, but as I told you, it is very rarely.

**Make the payment and finish the order** After you indicates this information, We continue with the payment section, These is the section where you can apply your coupons or discount codes. Basically We can complete the paymente by two general ways, Paypal or Credit card.

**Receive your PCB** Days later, 7 days or few more, according to your location and custom broker process, You will receive your pcb prototypes.

# Why JCLPCB?
JLCPCB has been at the fore front of the PCB industry. With over 14-year continuous innovation and improvement based on customers' need, we have been growing fast, and becoming a leading global PCB manufacturer, who provides the rapid production of high-reliability and cost-effective PCBs and creates the best customer experience in the industry.In case that you do not have an account yet, check out the bellow link►JLCPCB: https://jlcpcb.com/IAT

Most Efficient, Economic, Innovative PCB Solutions
Higher Quality
Lower Cost
Faster Delivery
JLCPCB provides a rapid production of high-reliability and cost-effective PCBs and create the best customer experience in the indrustry.

# BUILDING THE BOARD
Attached you will find the BOM (bill of materials) needed to build the PCB, as you can see in the list you can use the designator and You can check also with the schematic circuit.

# THE BOOTLOADER
The 18F2550 microcontroller has the possibility to modify its own FLASH memory under the control of a firmware, in a similar way to how the locations in its EEPROM are modified. This firmware is called “Bootloader” and it should be uploaded before to use the board, after uploaded the firmware, We can program directly from our PC to the board. Through this firmware bootloader you will be able to transfer executable programs.hex from the PC to the 18F2550 FLASH memory through the USB cable and using the software application USB HID from Mikroelektronika. This software already has its necessary drivers and automatically detects, through the USB cable, the presence of the board module with the bootloader loaded.

# UPLOADING THE FIRMWARE WITH PICKIT 2
For the first and only time, We are going to use the Pickit 2 Programmer to upload the firmware of our bootloader, once we loaded the.hex firmware, We do not need the pickit 2 again. You can use the Pickit 2, Pickit 3, Pickit 3.5, Pickit 4 or another programmer board available.

# PROGRAMMING THE BOARD
Now we are ready to program and work with our board, in the below videos You can see how to use our board, basically after We connect, We have 5 seconds to link the board with the bootloader aplications, if we pass the 5 seconds we need to press reset button or connect again the USB cable.
https://youtu.be/kzl8o4mRO8c

# THANKS
Thank to:
►JLCPCB: https://jlcpcb.com/IAT
► Bootloader developers for the Pic18F2550

