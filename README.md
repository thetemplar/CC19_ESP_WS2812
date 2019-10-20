# Coding Challenge 2019 - Trinket!

Beschreibungen und Handouts der CC19 der EFS!

## Was ist drauf?
- ESP8266-12E
- AMS1117-3.3
- Micro-USB-Buchse (nur zur Stromversorgung)
- 9x WS2812
- Widerstände zum Betrieb des ESP8266
- optional: Kondensatoren
- optional: UART Header

## Was ist geflasht?
Eine per Arduino-IDE geschriebene Software, welche ein kleines LED-Lichtspiel anzeigt und parallel dazu die ersten 10 Minuten nach dem Booten ein WLAN-AP auf macht, um sich per OTA flashen zu lassen.

## Wie flashe ich selber?
1) Arduino-IDE laden
2) ESP8266 Bib laden (https://github.com/esp8266/Arduino)
3) OTA Funktion durchlesen (https://arduino-esp8266.readthedocs.io/en/latest/ota_updates/readme.html#arduino-ide)  
> Blockquote ggf ist es nicht notwendig extra Python zu installieren
4) Sich in das WLAN des ESP8266 verbinden (heißt CC19_ESP8266_<hex-chip-id\>)
5) Bei Board "NodeMCU 1.0 .." auswählen, bei Port die Netzwerkschnittstelle (siehe Settings.png in diesem Repo)
6) Flashen
**ACHTUNG!** Neue Software muss auch OTA unterstützen, am besten die FW dieses Repos als Basis nutzen!

## I fcked up... 
ESP8266 "gebrickt" oder OTA geht nicht? Alternativ per UART (also nach einem FTDI-Adapter wie CP210x oder FT232RL) die Platine über die Header anschließen. Damit der Bootloader in den Flashmodus geht, muss **VOR** Powerup der GPIO-0 auf Masse gezogen werden. Dies geht am besten in dem das linke Pad des oberen rechten Widerstands auf Masse gezogen wird! Für alles weitere gibt es viele viele Tutorials im Internet.  Zum Beispiel [hier](https://alselectro.wordpress.com/2016/11/07/esp8266-upload-code-from-arduino-ide-no-arduino-board-required/) oder
[hier](https://www.instructables.com/id/ESP-12F-ESP8266-Module-Minimal-Breadboard-for-Flas/).

## Details zu den Robots
...folgt :)
