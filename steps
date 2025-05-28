Flashing the kernel version 5.4.70 image in imx8qxp

1. Download the Prebuilt Kernel Image
	Visit the official NXP website:
	https://www.nxp.com/design/design-center/software/embedded-software/i-mx-software/embedded-linux-for-i-mx-applications-processors:IMXLINUX


Download the prebuilt kernel image for i.MX8QXP with Linux kernel version 5.4.70
2. Download the Universal Update Utility (UUU)
	Copy the below link to download the Universal Update Utility (uuu) 
	https://github.com/NXPmicro/mfgtools/releases
	Navigate to the folder with the uuu binary and use the following command to make it executable:
		$ sudo chmod a+x uuu
	Move the uuu binary to /usr/local/bin with the following command:
		$ sudo mv uuu /usr/local/bin
		
3. Prepare the i.MX8QXP Board
	Set Switch 2 (SW2)(1) to the ON position. All other switches should be OFF.
	This sets the board into serial download mode, enabling flashing via USB.
	
4. Flash the Image to SD Card
	Unzip the prebuilt kernel image package.
	Navigate to the directory containing the imx-boot and .wic files.

5. Run the following command to flash the image to an SD card:
	$ sudo uuu -b sd_all imx-boot-imx8qxpc0mek-sd.bin-flash_spl imx-image-full-imx8qxpc0mek.wic (file may vary)

	To flash the image to eMMC instead of the SD card, use:
		$ sudo uuu -b emmc_all imx-boot-imx8qxpc0mek-sd.bin-flash_spl imx-image-full-imx8qxpc0mek.wic

6. Configure Boot Mode
	If booting from the SD card, set both SW2(1) and SW2(2) to ON. Ensure all other switches are OFF.

	If booting from eMMC, set only SW2 to ON. Ensure all other switches are OFF.

7. To build the kernel image, run the following command

	$ chmod +x build.sh
	$ ./build.sh
	

7. All changes were made in imx8qxp-mek-isl79987.dts file, so replace the fdt_file with imx8qxp-mek-isl79987.dtb
