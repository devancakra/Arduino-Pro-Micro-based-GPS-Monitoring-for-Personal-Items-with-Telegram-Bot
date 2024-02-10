[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Arduino-Pro-Micro-based-GPS-Monitoring-for-Personal-Items-with-Telegram-Bot)
![Project](https://img.shields.io/badge/Project-Arduino-light.svg?style=flat&logo=arduino&logoColor=white&color=%23F7DF1E)

# Arduino-Pro-Micro-based-GPS-Monitoring-for-Personal-Items-with-Telegram-Bot
This project was created as an effort to increase security on personal belongings. The position of the items can be monitored at any time through the telegram bot, so that the items will not be easily stolen. If someone loses an item, as long as the GPS is still installed and can function properly, then its position will be tracked immediately.

<br><br>

## Project Requirements
| Part | Description |
| --- | --- |
| Development Board | Arduino Pro Micro Leonardo ATMEGA32U4 |
| Supporting Board | Wemos D1 Mini |
| Code Editor | Arduino IDE |
| Application Support | Telegram Bot |
| Driver | USB-Serial CH340 |
| Programming Language | C/C++ |
| Arduino Library | • TinyGPS++<br>• SoftwareSerial<br>• CTBot |
| Sensor | GPS NEO6MV2 (x1) |
| Other Components | • Micro USB cable - USB type A (x1)<br>• Jumper cable (1 set)<br>• Adaptor DC 5V (x1) |

<br><br>

## Download & Install
1. Arduino IDE

   ```
   https://www.arduino.cc/en/software
   ```
<br>

2. USB-Serial CH340

   ```
   https://bit.ly/CH340_Driver
   ```
   
<br><br>

## Project Designs
<table>
<tr>
<th width="420">Block Diagram</th>
<th width="420">Pictorial Diagram</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/Arduino-Pro-Micro-based-GPS-Monitoring-for-Personal-Items-with-Telegram-Bot/assets/54527592/586d6f7d-764b-44a7-9121-cfd8e4d45f57" alt="Block-Diagram"></td>
<td><img src="" alt="Pictorial-Diagram"></td>
</tr>
</table>
<table>
<tr>
<th width="840">Wiring</th>
</tr>
<tr>
<td><img src="" alt="Wiring"></td>
</tr>
</table>

<br><br>

## Arduino IDE Setup
1. Open the ``` Arduino IDE ``` first, then open the project by clicking: ``` File ``` -> ``` Open ``` :

   <table><tr><td width="840">
   
      • ``` APmicro_gpstracker.ino ```
      
      • ``` WD1mini_bot.ino ```

   </td></tr></table><br>
   
2. Fill in the ``` Additional Board Manager URLs ``` in Arduino IDE

   <table><tr><td width="840">
      
      Click ``` File ``` -> ``` Preferences ``` -> enter the ``` Boards Manager Url ``` by copying the following link:
   
      ```
      http://arduino.esp8266.com/stable/package_esp8266com_index.json
      ```

   </td></tr></table><br>
   
3. ``` Board Setup ``` in Arduino IDE

   <table>
      <tr><th>
         
      i
         
      </th><th width="810">
            
      How to setup the ``` Arduino Pro Micro ``` board
   
      </th></tr>
      <tr><td colspan="2" width="810">

      Click ``` Tools ``` -> ``` Board ``` -> ``` Arduino AVR Boards ``` -> ``` Arduino Micro ```.
              
      </td></tr>
   </table><br><table>
      <tr><th>
         
      ii
         
      </th><th width="810">

      How to setup the ``` Wemos D1 Mini ``` board
            
      </th></tr>
      <tr><td colspan="2" width="810">

      • Click ``` Tools ``` section -> ``` Board ``` -> ``` Boards Manager ``` -> Install ``` esp8266 ```.

      • Then click ``` Tools ``` -> ``` Board ``` -> ``` ESP8266 Boards ``` -> ``` Wemos D1 Mini ```.
            
      </td></tr>
   </table><br>
   
4. ``` Change the Board Speed ``` in Arduino IDE

   <table>
      <tr><th>
         
      i
         
      </th><th width="810">
            
      How to change the speed of ``` Arduino Pro Micro ``` board
   
      </th></tr>
      <tr><td colspan="2" width="810">

      Click ``` Tools ``` -> ``` Upload Speed ``` -> ``` 9600 ```.
              
      </td></tr>
   </table><br><table>
      <tr><th>
         
      ii
         
      </th><th width="810">

      How to change the speed of ``` Wemos D1 Mini ``` board
            
      </th></tr>
      <tr><td colspan="2" width="810">

      Click ``` Tools ``` -> ``` Upload Speed ``` -> ``` 115200 ```.
            
      </td></tr>
   </table><br>
   
5. ``` Install Library ``` in Arduino IDE

   <table><tr><td width="840">
         
      Download all the library zip files. Then paste it in the: ``` C:\Users\Computer_Username\Documents\Arduino\libraries ```.

   </td></tr></table><br>

6. ``` Port Setup ``` in Arduino IDE

   <table><tr><td width="840">
         
      Click ``` Port ``` -> Choose according to your device port ``` (you can see in device manager) ```.

   </td></tr></table><br>

7. Change the ``` WiFi Name ```, ``` WiFi Password ```, and so on according to what you are currently using.<br><br>

8. Before uploading the program please click: ``` Verify ```.<br><br>

9. If there is no error in the program code, then please click: ``` Upload ```<br><br>

10. If there is still a problem when uploading the program, then try checking the ```driver ``` / ``` port ``` / ``` others ``` section.

<br><br>

## Telegram Bot Setup
1. Open <a href="https://t.me/botfather">@BotFather</a>.<br><br>

2. Type ``` /newbot ```.<br><br>

3. Type the desired bot name, for example: ``` personalgps_bot ```.<br><br>

4. Type the desired bot username, for example: ``` personalgps_bot ```.<br><br>

5. Also do it for bot image settings, bot descriptions, and so on according to your needs.<br><br>

6. Copy ``` your telegram bot API token ``` -> then paste it into the ``` #define BOTtoken "YOUR_API_BOT_TOKEN" ``` section. 

   <table><tr><td width="840">
   For example :<br><br>

   ```
   #define BOTtoken "2006772150:AAE6Fdjk3KbiySkzV6CLbd6ClJDzgTfJ5y0"
   ```
   
   </td></tr></table><br>
   
7. If it fails to connect to the Telegram Bot, then the problem may be in the firmware. Please check again.

<br><br>

## Get Started
1. Download and extract this repository.<br><br>
   
2. Make sure you have the necessary electronic components.<br><br>
   
3. Make sure your components are designed according to the diagram.<br><br>
   
4. Configure your device according to the settings above.<br><br>

5. Please enjoy [Done].

<br><br>

## Demonstration of Application
Via Telegram: <a href="https://t.me/personalgps_bot">@personalgps_bot</a>

<br><br>

## Highlights
<table>
<tr>
<th width="420">GPS Device</th>
<th width="420">Telegram Bot</th>
</tr>
<tr>
<td><img src="" alt="gps_device"></td>
<td><img src="" alt="telegram_bot"></td>
</tr>
</table>

<br><br>

## LICENSE
MIT License - Copyright © 2024 - Devan C. M. Wijaya, S.Kom

Permission is hereby granted without charge to any person obtaining a copy of this software and the software-related documentation files to deal in them without restriction, including without limitation the right to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons receiving the Software to be furnished therewith on the following terms:

The above copyright notice and this permission notice must accompany all copies or substantial portions of the Software.

IN ANY EVENT, THE AUTHOR OR COPYRIGHT HOLDER HEREIN RETAINS FULL OWNERSHIP RIGHTS. THE SOFTWARE IS PROVIDED AS IS, WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, THEREFORE IF ANY DAMAGE, LOSS, OR OTHERWISE ARISES FROM THE USE OR OTHER DEALINGS IN THE SOFTWARE, THE AUTHOR OR COPYRIGHT HOLDER SHALL NOT BE LIABLE, AS THE USE OF THE SOFTWARE IS NOT COMPELLED AT ALL, SO THE RISK IS YOUR OWN.
