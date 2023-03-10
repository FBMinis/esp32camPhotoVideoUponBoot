# esp32camPhotoVideoUponBoot
PIR turns ESP32-Cam ON; photo and video are captured and sent through Telegram.

(modified version of: https://github.com/jameszah/ESP32-CAM-Video-Telegram)

PIR outputs 3.3V signal when movement is detected, n-mosfet is siwtched ON (AO3400), camera is powered through p-mosfet (AO3401)

![keep camera ON while PIR output is HIGH](https://user-images.githubusercontent.com/36670323/224354396-e35774d3-f410-4284-ab9c-ad323cc820e4.png)

PIR module is an HC-SR501 modded as shown in order to run at 3.3V
The 1uF capacitor keeps the PIR inactive for 25 seconds before being able to detect movement again.
https://diyi0t.com/hc-sr501-pir-motion-sensor-arduino-esp8266-esp32/

![IMG_20230309_125437](https://user-images.githubusercontent.com/36670323/224354265-22d472e6-fda7-41e4-906e-c6b0dc795bfd.jpg)

The project is powered through an HT7833 LDO
Idle current is 70uA; it pulls close to 200mA while sending photo+video+message

![IMG_20230309_125545](https://user-images.githubusercontent.com/36670323/224354306-955de1a2-1c58-401a-8738-f83f3659f757.jpg)
![IMG_20230309_125632](https://user-images.githubusercontent.com/36670323/224354364-2e3ceb3e-4c70-472a-bce8-4c549ace5faf.jpg)
