# A Super Cool Hub

This project implements a budget and cool USB Hub thanks to the OTG USB feature that ESP32 S2/S3 brings on! On [BOM.md](https://github.com/hyduez/sch/blob/master/BOM.md) u can find each component with its own link to Aliexpress/Mouser. Due to expensive carriers fees and the niche market of Ecuador, it could be more than 20$ USD. The only firmware u are gonna need, is based on the brain of this PCB; if u want to do something when a state is detected, change the switch to flash the ESP32 and start coding. Anyways, this project aimed to be more; include OLED displays with tact buttons and commands to toggle data traveling, power on ports and show stats on the displays.

![](images/rendered.png)

Here is the schematic:

![](images/schematic.png)

You can see a lot of stuff that maybe u dont know where to start. But, as always, start where the power arises. Focus on the CH334F, it's the Mini Hub with 4 ports and another one for the host to manage, in this case, ESP32 S3 WROOM. It provides almost all the energy on the PCB, we are interesed on the 5V-A net label; it's gonna be merged with another line, 5V-B from SparkFun DEV-14050 (based on CH340G), this last one serve as auxiliar line, if u need more power available. Merged, they produce 5V-C, who is in charge of the USBs VBUS and ESP32 S3 WROOM power.

> [!IMPORTANT]
> Notice that this schematic is working with an ESP32 S3 WROOM, that's the reason why there's an AMS1117-3.3 that decrease the voltage from 5V to 3.3V; that's not neccesary with ESP32 S3 Devkit, since it brings its own regulator.

The idea is that u'd add another coproccesor and create an useful artcraft hardware made by your hands, something to be proud. It's cool. You're not flexing something u bought on a minimarket, it's something u built and that's what matters.
