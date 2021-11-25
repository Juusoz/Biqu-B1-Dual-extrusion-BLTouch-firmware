# Biqu B1 Dual extrusion BLTouch firmware

The default firmware for the Biqu B1 Dual extrusion upgrade kit did not have support for BLTouch, for some reason, so I rewrote it.
Hopefully this will save you some time instead of having to compile it yourself. I've also included an improved versions of the Cura profile, although Cura is still quite bad at supporting multi-extrusion printers.

Oh, and if you're still installing the parts, the instructions don't mention it, but you need to open up the bottom panel of your printer and put the motor cable in the rightmost slot in the motherboard and the motor driver next to the rest. **Make sure you put the red in red and black in black or else you'll fry your motherboard!**

![motherboard](https://user-images.githubusercontent.com/48849652/143468011-89eeb33e-20a5-4c28-b93d-4e5a31a3607b.jpg)

# Firmware

Copy the firmware.bin into an SD card and insert it into the SD card slot in the middle of the printer. The one in the front is for the screen.

If you want to modify the firmware, I've also listed the configuration files as well.

# Cura profile
1.  Add a new Custom FFF printer.

![Cura machine settings 0](https://user-images.githubusercontent.com/48849652/143470194-77956637-4b54-460d-8db9-5b7af5cb0d05.jpg)

2. Copy these values into your machine settings. The start and end G-Codes are listed above.

![Cura machine settings](https://user-images.githubusercontent.com/48849652/143470296-1d4a0af4-e1d4-4532-aa34-9cb660b937b0.jpg)
![Cura machine settings 2](https://user-images.githubusercontent.com/48849652/143470303-bda7a373-bc3c-4cc1-a749-26d6108e51a9.jpg)

3. Import the Cura profiles (Preferences -> Configure Cura -> Profiles)

![Cura Profile import](https://user-images.githubusercontent.com/48849652/143470844-804f33a5-c793-4707-a500-206edd3000c2.jpg)

It does some stringing between the prime tower and the print, which is caused by Cura not wiping the nozzle when leaving the prime tower. There is no feature to change that.

I will update this when Cura improves their dual extrusion. Feel free to modify the profile in the meanwhile, and if you figure out the stringing, please tell me.

4. Open the marketplace and install the "Printer Settings" -plugin, because Cura is dumb and doesn't recognize single nozzle multi-extrusion.

![printer settings](https://user-images.githubusercontent.com/48849652/143481611-24ec0a6e-c3a2-4aef-9f73-48b419885fbb.jpg)

5. In the search bar, type "Extruders share" and tick both Extruders Share Heater and Extruders Share Nozzle.

![extruders share](https://user-images.githubusercontent.com/48849652/143485912-5b816d4c-abc4-4f41-ae4e-2c134c3e822d.jpg)

This will prevent Cura from being stupid and trying to turn off the hotend when one of the extruders is no longer being used.
