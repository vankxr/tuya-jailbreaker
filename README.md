# tuya-jailbreaker
This small module aims to replace the original Wi-Fi module present in Tuya/Elivco smart plugs. The pin connections were reverse engineered from the base PCB traces, and the pad dimensions/spacing was measured from the original module.

## Pictures
The original module in blue, the ESP8285 module in green.

![modules](https://github.com/vankxr/tuya-jailbreaker/blob/master/media/modules.png)
![module](https://github.com/vankxr/tuya-jailbreaker/blob/master/media/module.png)

## Software
The jailbreaker was flashed with [Tasmota](https://tasmota.github.io/docs/), and it was configured with the correct pinout for the Energy Metering IC that is present in the base PCB.

![tasmota](https://github.com/vankxr/tuya-jailbreaker/blob/master/media/tasmota.png)
