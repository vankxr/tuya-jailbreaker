# tuya-jailbreaker
This small module aims to replace the original Wi-Fi module present in Tuya/Elivco smart plugs. The pin connections were reverse engineered from the base PCB traces, and the pad dimensions/spacing was measured from the original module.

## Pictures
The original module in blue, the ESP8285 module in green.

![modules](https://github.com/vankxr/tuya-jailbreaker/blob/master/media/modules.png)
![module](https://github.com/vankxr/tuya-jailbreaker/blob/master/media/module.png)

## Hardware
These modules are kind of impossible to disassemble without leaving some marks behind. Fortunately, after almost destroying the case of the first one I disassembled, I was able to figure out how they are put together and further teardowns were much easier.
Basically the trick is to drill three very small holes, and prying the two parts apart with a small screwdriver inserted into the holes. One hole for each side of the case, the side that has the push-button should not have a hole.
After hearing a click sound, the two parts can easily be separated, taking care not to rip apart the Earth connection.

Re-assembly is then performed by attaching everything and filling the previously mentioned holes with hot glue.

TODO: Add pictures

## Software
The jailbreaker was flashed with [Tasmota](https://tasmota.github.io/docs/), and it was configured with the correct pinout for the Energy Metering IC that is present in the base PCB.

![tasmota](https://github.com/vankxr/tuya-jailbreaker/blob/master/media/tasmota.png)

## Tasmota configuration
The first module I ordered back in June 2021 used the BL0937 energy metering IC, so naturally I designed this PCB taking this insto account after figuring out the pinout.
Later though, I ordered more modules, and realised they were slightly different. Modules ordered in November 2021 came with the BL0942 energy metering IC, which seems to be better since it does not require calibration. Even though I only figured this out after removing the original module and installing a jailbreak module, I was able to figure out which pins are connected to the energy metering IC and fortunately everything worked after configuring them correctly. Below are screenshots of Tasmota configuration for both versions of the base PCB.
### v1 (version with BL0937)
![tasmota](https://github.com/vankxr/tuya-jailbreaker/blob/master/config/tuya_v1.png)
### v2 (version with BL0942)
![tasmota](https://github.com/vankxr/tuya-jailbreaker/blob/master/config/tuya_v2.png)