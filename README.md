# Growatt_ShineWiFi custom firmware for HomeAssistant with MQTT trough ESPHome inside HomeAssistant.
Firmware replacement for Growatt ShineWiFi-S (serial), ShineWiFi-X (USB) or custom build sticks (ESP8266/ESP32).
FW.bin is only for factory reset!

Everything has been 100% tested with my SHINE-S, for the SHINE-X i could not test. 
I'm not responsible for any damages.




### RESTORE TO FACTORY
* I added the FW.bin you can flash it with ESPHome in homeassistant or an other tool to revert back to factory
Be sure when u did flash it with this bin file just reset the SHINE-S
* This will go back to Factory, so not visable in HomeAssistant!
<br>
<br>


### First things first

Initial loading of Firmware to the stick is rather easy:

Remove the stick's PCB from the housing. 
You need some power supply for the module while programming, e.g. if you use an USB-serial module that can supply the 3.3V while programming.


### How to put the SHINE-S in bootmode?:

* You'll need to power the module while programming. If you're using a USB-serial module that can supply 3.3V while programming, connect it as follows:
* Connect the RX pin from your flasher to the TX pin of your SHINE-S.
* Connect the TX pin from your flasher to the RX pin of your SHINE-S.
* Connect the GND pin from your flasher to the GND pin of your SHINE-S.
* Extend the GND cable with a piece of metal pin as the GND cable also needs to be in GPIO1.
* Connect the VIM pin of your flasher to the 3v pin of your SHINE-S.

### Installing ESPhome in homeassistant

Open Home Assistant and go to the Supervisor tab.
* Click on Add-on Store and search for ESPHome.
* Click on the ESPHome add-on and then click on Install.
* After the installation is complete, go back to the Supervisor tab and click on the ESPHome add-on.
* Click on Configuration and then on the Edit button (pencil icon).
* Add your ESPHome configuration settings, such as the name of your device and the IP address of your Home Assistant instance.
* Click on Save and then click on Start to start the ESPHome add-on.
* Once you have completed these steps, you should have ESPHome installed on your Home Assistant instance. You can then use the ESPHome dashboard to create and manage your ESPHome devices.

## To compile the firmware be sure to use google chrome!:

* Open the ESPHome dashboard by clicking on the ESPHome add-on in the Supervisor tab.
* Click on the "create device" button to create a new device configuration.
![image](https://user-images.githubusercontent.com/13116501/235431875-60adc436-4b74-468b-ab3f-4cefecf749ff.png)
* Select the device you want to configure and give it a name.

![image](https://user-images.githubusercontent.com/13116501/235431928-21725fbd-f262-4d2f-b72e-46892067f5c8.png)


![image](https://user-images.githubusercontent.com/13116501/235432006-489eadb4-8368-42a7-8278-a267b133e3e3.png)


* Click on edit Add the configuration settings for your device, such as the type of sensor you want to use and any other customizations you want to make.
Thanks for the code Wilbert Verhoeff, i did alter it and added MQTT

Check the yaml [here](https://github.com/malosaa/Growatt_Shine-S_HASS_Mod/blob/main/growatt.yaml) this is the code to upload.

* Once you have added all the necessary configuration settings, click on "Save" to save your configuration.

* When ready click on install 

![image](https://user-images.githubusercontent.com/13116501/235432251-2ba7e71d-5fb7-4d63-80e0-a272a466c17f.png)

* next step  click on from computer, and no wireless, wireless works if u did flash it the first times, so you don't have to be connected on your pc.

![image](https://user-images.githubusercontent.com/13116501/235432342-6b065fdd-8fac-4022-8a09-5f6a1e835f3a.png)

* Now you get this window, but wait till you get the download project, this will let yo download the bin file
After that press on open ESPHOME and follow the instructions, it lets u upload the binfile what you just downloaded and flash it.

![image](https://user-images.githubusercontent.com/13116501/235432505-aa9005d3-0c7c-4a48-8217-77d5898bb16f.png)

* If done correct, you see its online 

![image](https://user-images.githubusercontent.com/13116501/235432729-c736e215-6464-4ef9-9011-f87e2a1bffe5.png)

* When u click visit it shows u this dashboard.

![image](https://user-images.githubusercontent.com/13116501/235432695-5d7099d9-de53-4ee8-8000-8f12c6865e90.png)

* In homeassistant it will be detected instantly, and if u add it it shows up like this:

![image](https://user-images.githubusercontent.com/13116501/235435206-4a7f44a6-8512-4ee6-907b-6e3f2e865d3d.png)


![image](https://user-images.githubusercontent.com/13116501/235435239-5a3e8f37-87c4-4d5c-a91d-2fb27f00c00d.png)

* and in the MQTT addon it shows up like this:

![image](https://user-images.githubusercontent.com/13116501/235435320-4e450096-4bb4-4530-a3a5-e826167994b1.png)







# UPDATE 01-05-2023

* Added a slider in the GUI to select the update interval.
* Added a reboot button in the GUI so when u press that it reboots the device after setting up the update interval.



![image](https://user-images.githubusercontent.com/13116501/235464597-756dcac9-064d-4c70-945d-ff40f80bc2ad.png)




You can always edit the code when pressing edit and when done install and you select wireless, and it will go OTA:)
Have fun








