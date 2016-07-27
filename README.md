# opencvsh_for_ubuntu_mate

Step 0: For your convenience, I made a README and script file on

https://github.com/nanuyo/opencvsh_for_ubuntu_mate

pls download and unzip and open the README.md

Step 1. Download ubuntu mate image from

http://odroid.in/ubuntu_16.04lts/

Step 2. un xz on your host with this command

unxz ubuntu-16.04-mate-odroid-xu3-20160708.img.xz

Step 3. Insert micro-SD Card to your host PC
            Be sure that your SD is more than 8GByte
            (The size of Ubuntu mate image is around 4GByte and Opencv requires around 2.5GByte)

Step 4. Copy img to SDCARD 

Replace sdX to your SDCARD device name in your host.
==> !! BE CAREFUL -> IF YOU PUT THE NAME OF YOUR LOCAL HDD INSTEAD OF SDCARD, YOU LOST ALL YOUR DATA IN HDD.

sudo dd if=ubuntu-16.04-mate-odroid-xu3-20160708.img of=/dev/sdX bs=1M conv=fsync
	sync

Step 6. Install Gparted on your host and run
(you need to resize rootfs partition as it is just 4GByte in the image)

sudo apt-get install gparted
sudo gparted

Step 7. select /dev/sdX on Gparted
and on the rootfs. click right button on mouse and select resize.
and set max size of sdcard.

 
Step 8. Turn off the Odroid and Put your SDCARD into Odroid

Step 9. Move the switch to uSD from emmc and Turn on the board

Step 10. login your target(User:odroid, PW: odroid)

Step 11. on your target : run any web-browser and connect to

https://github.com/nanuyo/opencvsh_for_ubuntu_mate

Step 9: and download opencv_install_to_ubuntu_mate_16.04.sh
(Or, copy this script file from your host)

Step 10. run script
source opencv_install_to_ubuntu_mate_16.04.sh

Step 11. Test facedetect sample

cd opcv-2.13.xx/samples/c
./facedetect lena.jpg




