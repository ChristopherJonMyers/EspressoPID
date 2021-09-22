# EspressoPID
Add temperature control functionality to the Rancilio Silvia. 
_(sowftware should work for other machines, but hardware setup might be different.)_

## What You Will Need

### Hardware 

* [Raspberry Pi Zero Kit W](https://www.amazon.com/gp/product/B0748MPQT4/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1)
* [24-380V SSR Single Phase Solid State Relay](https://www.amazon.com/gp/product/B094VS4HQC/ref=ppx_yo_dt_b_asin_title_o00_s01?ie=UTF8&psc=1)
* [Adafruit Universal Thermocouple Amplifier MAX31856 Breakout](https://www.amazon.com/gp/product/B01LZBBI7D/ref=ppx_yo_dt_b_asin_title_o00_s02?ie=UTF8&psc=1)
* [K Type Thermocouple](https://www.amazon.com/gp/product/B00OLNZ6XI/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1)
* [Jumper Wires](https://www.amazon.com/gp/product/B01EV70C78/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1)
* [14 gauge wire](https://www.amazon.com/gp/product/B078YYLT5T/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1)
* Tools (Optional ish)
  * Flat and Philips screwdriver
  * Wirecutters/wire strippers
  * Electrical tape
  * Soldering Iron

### Software

* [Raspbery PI OS](https://www.raspberrypi.org/software/)
* [Python 3](https://projects.raspberrypi.org/en/projects/generic-python-install-python3)

## Hardware install

(Optional)
  Solder pins to the Pi and the MAX31655 like so.
  * [Pi](https://user-images.githubusercontent.com/36175788/134370773-940226f7-7d8e-46b8-ad97-4825b6295f77.png)
  * [MAX31856](https://user-images.githubusercontent.com/36175788/134371076-ff976a91-8eec-4232-9aa9-6d8ed39b2fb7.png)

Start by wiring the parts separately before connecting to the Pi and the machine.

  Solid State Relay (SSR)

   ![0922211122_HDR](https://user-images.githubusercontent.com/36175788/134373583-a2e1c237-97be-47ce-a087-7968363057cc.jpg)

  Thermocouple

   ![image](https://user-images.githubusercontent.com/36175788/134373933-0d860447-2abb-4747-8e4e-979007b17308.png)
   
Next install parts into the machine. 

I have placed the SSR and the PI behind the front plate above the drip tray. I ran the power cable and the jumpers for the thermocouple through the cutout behind the safety overpressure valve. I also ran the two red wires from the SSR up to the boiler chamber.

  ![0922211138_HDR](https://user-images.githubusercontent.com/36175788/134377188-b90efa48-52ad-47a4-9d1a-b6bd83ebe7fe.jpg)

For the thermocuple, I placed it between the pump and the center plate with the jumpers going through the cutout and the thermocouple wire going up to the boiler.

  ![0922211144_HDR](https://user-images.githubusercontent.com/36175788/134377822-fda81ca4-20c2-422b-ae09-c0332f16bd48.jpg)
  
Next we need to connect the SSR. What we are effectively doing is replaceing the thermocouple for the brew temperature with our won digital one. There are two thermocouple at the top of the boiler, one controls the temperature  for steaming (labled 140c) and the other for brewing(labeled 100c). We now need to disconnect the brew thermocouple.







