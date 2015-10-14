Makeblock-USB-Driver
====================
 Makeblock Orion or mBot On Yosemite:
 * install the Makeblock_Orion_Driver_for_MacOSX or mBot_Driver_for_MacOSX driver
 * Run the command in Terminal:
 sudo nvram boot-args="kext-dev-mode=1"
 * Reboot

Makeblock Orion or mBot on OSX El Capitan. Just like Yosemite, El Capitan requires kext driver signing. How this can be disabled in OSX 10.11 is changed however.
To get the drivers to work in El Capitan you need to use the new tool csrutil as follows:
 * Reboot and press CMD+R immediately after hearing the startup sound to boot to Recovery Mode
 * Open Terminal
 * Execute the following command: csrutil enable --without kext
 * Reboot
After rebooting you should see your serial ports again in the Arduino IDE or mBlock so you can program your Me Orion (or any other Arduino compatible device using CH340/CH341) again.
