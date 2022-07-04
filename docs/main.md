You should really only follow this if you were redirected here due to unable to use the browser for some reason.

?> UDPIH requires a Raspberry Pi Zero/Pico, or a Switch capable of running payloads (Unpatched or a Modchipped Unit).

- Set up UDPIH on your [Raspberry Pi Zero](https://github.com/GaryOderNichts/udpih#raspberry-pi-zero-linux), [Pico](https://github.com/GaryOderNichts/udpih#pico), or [Nintendo Switch](https://github.com/GaryOderNichts/udpih_nxpayload#instructions). (Click on the link that suits your needs best.)

### Needed files
- [Tiramisu](https://tiramisu.foryour.cafe/) (Just click `Download Package`).
- The <a href="docs/files/recovery_menu" download>LoadRPX UDPIH Payload</a>.

### SD Setup
1. Copy the **contents** of the downloaded Tiramisu `.zip` file to the root of your SD Card.
1. Copy the `recovery_menu` file to the root of your SD Card.
1. Copy the `root.rpx` file from `sd:/wiiu/environments/tiramisu` to root of the SD Card, and rename to `launch.rpx`.
1. Insert the SD Card into the Wii U 

### UDPIH
1. Shut off your Wii U, if it was on.
1. Unplug the Wii U from power, and then replug it.
1. Power on your Wii U.
1. As soon as you see the `Wii U` logo, plug in your UDPIH device.
1. Load any application. You should now see the environment loader.
1. Navigate to and select `installer`.
1. Press A `Check`.
1. Press A on `Install / Update`.
1. You’ll be asked if you are sure you want to install the PayloadLoader. Use the D-Pad to select `Install` and press A.
1. Press A to shut down the console.

### Nand Backup
1. Power on the console.
1. Launch the Health and Safety application while holding B.
1. Select `nanddumper`
1. Make the settings look like this and then press A. MLC is optional as it is the biggest part of the NAND Backup (8gb or 32gb depending on your model).
	- SLC: Yes
	- SLCCMPT: Yes
	- MLC: Optional
	- OTP: Yes
	- SEEPROM: Yes 
1. Wait for it to finish. It may take a few hours if you opted to dump MLC. 
1. To make sure you don’t lose the files, copy the `slc.bin`, `slccmpt.bin`, `seeprom.bin`, `otp.bin` and if you chose to go with a full backup, every `mlc.bin.part` file to your computer.
1. Delete the files to free up space on the SD Card.

### Autobooting Tirmisu
?> This section is optional. If you do not want to autoboot into the PayloadLoader, then skip to [Finalizing Setup](https://wiiu.hacks.guide/#/tiramisu/finalizing-setup)
1. Start the console to boot into the Wii U Menu, launch the Health and Safety Information app and hold the X button to open the Environment Loader menu.
1. Navigate the list using the D-Pad and navigate to the `installer` environment, press A to launch it.
1. Press A to select `Check`. 
1. Select `Boot Options`.
1. You will be asked if you want to switch the boot title. Press A to select `Switch to PayloadLoader`.
1. When the process finished, press A to shutdown the console.
1. The PayloadLoader will now be launched automatically on every boot.

### Finalizing Setup
?> The main guide has a page on this. You can find it [here](https://wiiu.hacks.guide/#/tiramisu/finalizing-setup)
