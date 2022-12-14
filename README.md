
<h1 align="center">
  <br>
  <a href=""><img src="https://raw.githubusercontent.com/BeachtechRobotics/assets/ade7abf526c82bdbb3b55d8f304c73b7938eeca9/BEACHTECH%20logo.svg" alt="Beachtech" width="900"></a>
</h1>

<h4  Battle Bot Controller for Based on an ESP-32.</h4>




<a href=""><img src="https://raw.githubusercontent.com/BeachtechRobotics/assets/362690af1dc5d16088b6086bf795fb1e9b65fbf7/Madewitharduino.svg" alt="Markdownify" width="300"></a>

# Getting Started

PDF detailed guide at this [download](https://github.com/BeachtechRobotics/Battle-Bot-PS3-Code/blob/main/Programming%20ESP32%20Guide.pdf) link

## Installing the ESP32 board

In case you haven't yet, you can add the ESP32 boards to your Arduino IDE by adding them to the Boards Manager: 

Open `File -> Preferences`, and paste the following URL in the `Additional Boards Manager URLs` field:
```bash
https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
```
Open the Boards Manager with `Tools -> Board: "xxx" -> Boards Manager`, 
Search for `ESP32` and press install button for the `ESP32 by Espressif Systems`.Finally, select the ESP32 board you have with `Tools -> Board: DOIT ESP32 DEVKIT V1` under the section ESP32 Arduino 


## Installing the librares

You can install the Arduino librares from within the Arduino IDE. Open the Library Manager with `Sketch -> Include Library -> Manage Libraries...`.

Search for `PS3 Controller Host`, and click `Install`.

Search for `ESP32Servo`, and click `Install`.

## Using the the Code

In the sketch find Ps3.begin("00:00:00:00:00:00"); and replace with MAC address that is associated with in the PS3 Controller.

```bash
#include <Ps3Controller.h>

void setup()
{
    Ps3.begin("00:00:00:00:00:00");
}
```

> **Note**
> You can use [Sixaxis Pair Tool](https://sixaxispairtool.en.lo4d.com/download/mirror-hs1)  software is uesd to look up and update the MAC address of the controller.

    
## Download

You can [download](https://github.com/BeachtechRobotics/Battle-Bot-PS3-Code/blob/main/BATTLEBOT_ESP32_PS3.ino)  arduino code at this link

## Credits

I've had tremendous help developing this this guide and code by reading these sources:

- [jvpernis ESP-32 PS3 libary](https://github.com/jvpernis/esp32-ps3)
- [aed3 ESP-32 PS4 libary](https://github.com/openobjects/PS4-esp32)
- [randomnerdtutorials ESP32 Tutorial](https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-windows-instructions/)

