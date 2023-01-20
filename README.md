# DWM1001_MQTT_central_server
MQTT central server and frontend project to scale to multiple gateways

## This project is based in Qorvo/Decawave MDEK1001 developper kit, which include the WDM1001 board for UWB (Ultra Wide Band)

### Disclaimer: 
The frontend has been taken without official permission from the public source code found inside the DRTLS_raspbian_R2.0.img file.

Official Qorvo/Decawave site to read documentation, download software and buy WDM1001 boards:
https://www.qorvo.com/products/p/DWM1001C#documents

## Server Requirements

- NodeJs.
- MQTT server, the most used is Mosquitto, this configuration use MQTT over Websocket.
- Available Ports for HTTP, MQTT and WS, in this configuration used ports 80, 1883 and 15675 respectively.

## How to run

1) Clone this project in your server
2) Run **npm install** command
3) Run **npm start** command

### All Infraestructure requirements

- Local Area Network.
- 2 o more Raspberry Pi 3.
- Central server (PC or another Raspberry).
- 10 or more WDM1001 boards (12 is minimum recomended for basic scalable environment).

### Gateway configuration changes (inside Raspberry Pi 3 software). 

You must change MQTT server configuration in the section **# daemon settings** in the file **/etc/dwm1001/dwm1001.config**:

You need to change **proxy_server_host** to IP server and **proxy_server_port** to MQTT server port.

[![Example configuration file](https://raw.githubusercontent.com/pablotoledom/DWM1001_MQTT_central_server/main/assets/dwm1001_config.png)](https://raw.githubusercontent.com/pablotoledom/DWM1001_MQTT_central_server/main/assets/dwm1001_config.png)