#User Manual

This sketch was built to work with the project "DIY Si4730 All Band Radio (LW, MW, SW, FM)" receiver by Mirko Pavleski.
The original project can be found on [create.arduino.cc](https://create.arduino.cc/projecthub/mircemk/diy-si4730-all-band-radio-lw-mw-sw-fm-1894d9).
Please, follow the circuit available on that link.

If you are using a SI4735-D60 or SI4732-A10 based circuit, you can also use this sketch to add the SSB
functionality to the original Pavleski's project. If you are using the original SI4730-D60 based circuit, the
SSB will not work. However, the STEP, MODE, AGC, Attenuation, bandwidth, Soft Mute, Audio Volume and
Shortwave will still work.

There are two boards commonly found on eBay and AlliExpress based on SI4730.

1) “PL102BA-S V:2.1 10628” based on SI4730-D60 with shortwave support and FM / RDS.
   See [pu2clr.github.io/SI4735/extras/BOARD_PL102BA/](https://pu2clr.github.io/SI4735/extras/BOARD_PL102BA/) for more details.

2) “NE928-10A V:01” based on SI4730-B20 without shortwave and FM / RDS.
   See [pu2clr.github.io/SI4735/extras/BOARD_NE928_10A_V_01](https://pu2clr.github.io/SI4735/extras/BOARD_NE928_10A_V_01/) for more details.


Commands

1. BAND SELECTION

    Select the band by pressing the encoder push button once, and then rotate the encoder clockwise or
    counterclockwise to change which band is shown. When the desired band is shown on display, you can press
    the button once again or wait for about 2 seconds. The control will then go back to the VFO.

2. STEP, MODE, AGC/Attenuation, bandwidth, Soft Mute and VOLUME

     2.1. Press the encoder push button twice (within 1/2 second).  
     2.2. After that, the display will show you the Menu text. Rotate the encoder clockwise or
            counterclockwise to select the option (STEP, MODE, AGC/Attenuation, bandwidth, VOLUME, etc).  
     2.3. After that, select the option you want to setup by pressing the encoder push button once again.  
     2.4. After that, rotate the encoder clockwise or counterclockwise to select the parameter.  
     2.5. Finally, you can press the button once again or wait for about 2 seconds.  
            The control will go back to the VFO.

3. VFO/BFO Switch

     3.1. Press the encoder push button twice (within 1/2 second).  
     3.2. Rotate the encoder clockwise or counterclockwise and go to the BFO option. This option is shown only
             on SSB mode.  
     3.3. Press the encoder push button once again.  
     3.4. Rotate the encoder clockwise or counterclockwise to increment or decrement the BFO (select the offset).  
     3.5. If you press the button again or stop rotating the encoder for about 2 seconds, the control will
             then go back to the VFO.


4. SEEK

    4.1. Select the menu by pressing the encoder push button twice. The seek direction is based on the last
         encoder movement. If clockwise, the seek will go up. If counterclockwise, the seek will go down.


###ATTENTION:
            Try to press and release the push button quickly. If you hold the button for too long, you might
            alternate the command status (enable and disable) randomly.
            After about 2 seconds, the current command or action is disabled automatically and the interface
            goes back to VFO control.

###TIPS:
            Try to refine the time to disable a current command or action by changing the constant ELAPSED_COMMAND
            (#define ELAPSED_COMMAND 2000). The value 2000 means 2 seconds. Increase or decrease the value to get
            a better interface for you.
            Try to refine the constant ELAPSED_CLICK (#define ELAPSED_CLICK 1500). This constant controls the time
            for double click on encoder push button. Smaller values demand more agility in the double click.
