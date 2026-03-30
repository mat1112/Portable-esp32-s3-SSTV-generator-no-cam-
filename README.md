# Portable-esp32-s3-SSTV-generator-no-cam
Portable esp32-s3 SSTV generator (no cam). For use with a handheld VHF/UHF radio like the Baufeng UV5. No audio filtering electronics required. No DAC required.

Adapted from:
https://github.com/vaugerbird/sstv-backpack
and
http://blog.dzl.dk/wp-content/uploads/2022/09/ESP32CAM_SSTV6_blog.zip

I've used the Arduino IDE for this code, with board ESP32-S3-USB-OTG.

The image to be sent is loaded at compile time with the code i.e. badge.c

To substitute your own 320 x 240 pixel image, use a conversion tool like: https://lcd-image-converter.riuson.com/en/about/
To generate your own image, select the Color R8G8B8 conversion and set the Block size to 8 bits.

More images could be sent by using an SD card, to store these image data files.

