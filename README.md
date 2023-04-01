My investigation of building the TFT_LVGL_UI on Marlin (3/31/23)

OVERVIEW:
1) I found Mks-Robin-Nano-Marlin2.0-Firmware-master on gethub and modified to 
build and kinda-work.
2) I created Marlin-2.1.2.TT_BlueR-Plus_LVGL from the current Marlin 2.1.2 and
modified to build and kinda-work.

CONCLUSIONS:
1) Marlin does not support the MKS_ROBIN_TFT43 at it's real 480x272 resolution. 
So this is my last work on the LVGL graphics.
2) I am certainly no expert but was able to figure out this much for other brave souls.
3) I plan on using the Original Two Trees BLU-5 BLUER PLUS V2.0.2-V2 software if I want
LVGL, however my plan is to use my Marlin 2.1.2 TFT_COLOR_UI for my daily driver.

********************************************************************************
Marlin-2.0.9.1.TT_BlueR-Plus_LVGL.zip

Marlin 2.0.9.1 for BLU-5 Bluer Plus 5xTMC2209 and 5x1.8 degree stepper motors for use with the LVGL user
interface.

Build with Platformio or Auto Build Marlin extensions on Visual Studio Code: 
mks_robin_nano35 		- without the MKS WIFI enabled maple is NOT required

Do NOT BUILD with mks_robin_nano35_maple, because it will not work!

Notes:

o FILAMENT_RUNOUT_SENSOR, LCD_BED_LEVELING can not be enabled due to TFT_LVGL_UI.

o Touchscreen does not work because to utilize TFT_LVGL_UI the screen resolution must be 480x320 to
utilize TFT_LVGL_UI. The MKS_ROBIN_TFT43 is 480x272 resolution. So the whole screen won't fit and 
doesn't seem to be able to be calibrated by M995 over pronterface.

o Without the MKS WIFI enabled maple is NOT required (because it will not work!)

********************************************************************************
Marlin-2.1.2.TT_BlueR-Plus_LVGL.zip

Marlin 2.1.2 for BLU-5 Bluer Plus 5xTMC2209 and 5x1.8 degree stepper motors for use with the LVGL user
interface.

Build with Platformio or Auto Build Marlin extensions on Visual Studio Code: 
mks_robin_nano_v1v2				- without the MKS WIFI enabled

Do NOT BUILD with mks_robin_v1v2_maple, because it will not work!

Notes:

o FILAMENT_RUNOUT_SENSOR, LCD_BED_LEVELING can not be enabled due to TFT_LVGL_UI.

o Touchscreen does not work because to utilize TFT_LVGL_UI the screen resolution must be 480x320 to
utilize TFT_LVGL_UI. The MKS_ROBIN_TFT43 is 480x272 resolution. So the whole screen won't fit and 
doesn't seem to be able to be calibrated by M995 over pronterface.

o Without the MKS WIFI enabled maple is NOT required (because it will not work!)

Install/Run:

Marlin 2.0.9.1

1. copy Marlin-2.0.9.1.TT_BlueR-Plus_LVGL\.pio\build\mks_robin_nano35 assets folder and 
Robin_nano43.bin file to the SD Card.

Marlin 2.1.2

1. copy Marlin-2.1.2.TT_BlueR-Plus_LVGL\.pio\build\mks_robin_nano_v1v2 assets folder and 
Robin_nano43.bin file to the SD Card.
goto 2

2. With BLU-5 off insert the SD card.

3. Apply power, and view bin file and assets get loaded by the bootloader.
