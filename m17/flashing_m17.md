# Flashing OpenRTX to the CS7000-M17

Flashing the CS7000-M17 is a fairly easy process. Be patient and take your time
through the whole process. Read all instructions before attempting to flash
your radio. This document is provided as a guide and is not a replacement for
support by the manufacturer, Connect Systems Inc. 

Through the process, references to hardware buttons will be made. For clarity,
the hardware buttons referenced in this document are pictured below.

![Hardware Buttons](_media/hw_buttons.png)

* SK1 - Side Key 1 - Top button on the left side of the radio. Above the large PTT button.
* SK2 - Side Key 2 - Third button from the top on the left side of the radio. Below the large PTT button.
* SK3 - Side Key 3 - Fourth button from the top on the left side of the radio. Below SK3, second below the large PTT button.
* TK - Top Key - Orange button on the top of the radio. Between the channel select knob and antenna port.
* F1 - Front 1 - Labeled F1 on the front of the radio. Top left hand button.
* F2 - Front 2 - Labeled F2 on the front of the radio. Top right hand button.

You will also need the following:

* CS7000-M17 radio and fully charged battery (obviously.)
* CS7000-M17 Programming Cable
* Flashing software appropriate for your operating system (described in their sections)
* OpenRTX firmware from CSI
* Patience
* Drink of your choice

CSI provides a software page with the OpenRTX firmware, `Openrtx_CS7000.dfu`.
Flashing software for Windows, `DfuSeDemo V3.0.6` is also provided there.

[Connect Systems Software Page for CS7000-M17](https://www.connectsystems.com/products/top/radios/CS7000_M17_SOFTWARE.htm)

Instructions for flashing your radio with [Windows](#windows), [Mac](#mac), and [Linux](#linux) are below.

## Windows

### Flashing software: 

DfuSeDemo (version 3.0.6), available from Connect Systems' Software page

### Steps

1. Download and install DfuSeDemo.
2. Download the OpenRTX firmware from CSI's Software page.
3. Open the DfuSeDemo application.

You should see this window on your screen:

![DfuSeDemo_1](_media/dfuse_1.png)

4. Attach the Programming Cable to the radio by placing its hook into the
hole next to the antenna port, and pressing the connector against the right
side of the radio. Use the thumbscrew to secure the connector in place.

5. Plug the USB connector from the programming cable into the computer.

6. While pressing and holding SK1, turn the volume control knob clockwise to
power the radio on. The screen will illuminate, and remain blank. The radio is
now in DFU (flashing) mode.

7. Check the DfuSeDemo application to ensure that the radio is recognized.

You should see this window on your screen:

![DfuSeDemo_2](_media/dfuse_2.png)

| :exclamation: If you do not see "STM Device in DFU Mode" under Available DFU Devices - `STOP` and wait for Windows to automatically install the driver. |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|

| :exclamation: If Windows does not automatically install a driver, check Device Manager to see if "STM BOOTLOADER" is present. If you see "STM BOOTLOADER" in Device Manager, and no devices are listed in DfuSeDemo - `STOP` and follow the troubleshooting steps at the bottom of this page. |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

8. In DfuSeDemo, in the Actions section, double-click the `Target Id 01` (Option Bytes) line item.

You should see this dialog box open:

![DfuSeDemo_3](_media/dfuse_3.png)

9. Click on `Yes` to remove read protection.
  * This is a required step before you can flash the OpenRTX firmware to the radio
  
  | :exclamation: Disabling the read protection on the radio may take a minute or so. `BE PATIENT` |
  |------------------------------------------------------------------------------------------------|

When the process is complete, you should see this dialog box open:

![DfuseDemo_4](_media/dfuse_4.png)

10. Click on `OK`.

11. Turn the volume knob fully counter-clockwise to power the radio off.

12. While pressing and holding SK1, turn the volume control knob clockwise to
power the radio on. The screen will illuminate, and remain blank. The radio is
now in DFU (flashing) mode.

13. Back in the main DfuSeDemo window, select (single-click) the `Target Id 00` (Internal Flash) line item.

The window should look like this:

![DfuSeDemo_5](_media/dfuse_5.png)

14. In the Upgrade or Verify Action section, click the `Choose...` button.

15. Use the dialog box to find and select the `openrtx_cs7000.dfu` file downloaded previously.

You might find it in your Downloads folder like below:

![DfuSeDemo_6](_media/dfuse_6.png)

16. DfuSeDemo should show a green bar at the bottom, indication the firmware file loaded correctly.

Like this:

![DfuSeDemo_7](_media/dfuse_7.png)

17. Click on the `Upgrade` button.

18. You will receive another dialog box warning you that the radio is in DFU
mode and DfuseDemo cannot determine if the file is correct for the device. This
is normal, click on `Yes` to proceed.

Click on `Yes`

![DfuSeDemo_8](_media/dfuse_8.png)

19. The flashing process will proceed, with a progress bar at the bottom of the
window. When the process is complete, the progress bar will show `Target 00:
Upgrade successful !`

Like this:

![DfuSeDemo_9](_media/dfuse_9.png)

20. Turn the volume knob fully counter-clockwise to power the radio off.

21. Remove the programming cable from the radio by loosening the thumbscrew
and lifting the connector away and up from the body of the radio.

22. Turn the volume control knob clockwise to power the radio on. The screen
will illuminate, and show the OPNRTX logo on screen briefly. Once the radio
has booted, you will be presented with the OpenRTX idle screen, showing the
mode (FM), frequency, and battery status. Further information about this
screen will be discussed in the [Operating OpenRTX](/m17/operating.md) section.

#### Congratulations!

You now have flashed the OpenRTX firmware on your radio! Continue on to the
[Operating OpenRTX](/m17/operating.md) section of this Wiki to learn how to use
the OpenRTX firmware, and how to start using the M17 digital radio mode!

## Mac

:exclamation: TBD

## Linux

:exclamation: TBD