My corne keyboard build and UK layout images.

*Left*
![some image](images/img1.jpg)


*Right*
![some image](images/img2.jpg)


*Connected*
![some image](images/img3.jpg)


*Finished*
![some image](images/img4.jpg)

### Layer 1
![s](images/Layer1.PNG)

### Layer 2
![s](images/Layer2.PNG)

### Layer 3
![s](images/Layer3.PNG)

### Layer 4
![s](images/Layer4.PNG)

---------------------------------------
07.06.2024
Today I accidentally pulled the usb-c cable which was attached to the left(master) side and that broke the usb-c port. Nothing happened when I reinserted the usb-c cable into the left side. The only thing to do was to either order a new Elite-C micro-controler or make the right side the master and the left side the slave.

This is what I did.

I am on a Windows 10 machine and I followed the qmk guide: https://docs.qmk.fm/newbs_getting_started


1. Downloaded qmk msys.

2. Ran qmk setup

3. Generated my own set of config.h and keymap.c files by following the guide on the qmk websi

4. Previously I used https://config.qmk.fm/#/oddball/v2_1/LAYOUT in order to generate a .JSON and a .hex file. So now I used https://jhelvy.shinyapps.io/qmkjsonconverter/ to convert my pre-existing JSON to a .c file (old_json_file.c)

5. Replace the new keymap.c file contents with the contents from old_json_file.c

6. As suggested in config.h I commented out

// #define MASTER_LEFT
and uncommented 
#define MASTER_RIGHT

7. I ran qmk compile which generated a new .hex file for me

8. Opened qmk toolbox. Opened the hex file inside it. Inserted the usb c cable into the right keyboard. Hit the reset button and viola.

Just to confirm I did not need to flash the left side, flashing only the right side got both halves working. (edited)
