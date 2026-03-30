# Portable-esp32-s3-SSTV-generator-no-cam
Portable esp32-s3 SSTV generator (no cam). For use with a handheld VHF/UHF radio like the Baufeng UV5. No audio filtering electronics required. No DAC required.

Adapted from:
https://github.com/vaugerbird/sstv-backpack
and
http://blog.dzl.dk/wp-content/uploads/2022/09/ESP32CAM_SSTV6_blog.zip

I've used the Arduino IDE for this code, with board ESP32-S3-USB-OTG.

The SSTV image to be sent is loaded at compile time with the code i.e. badge.c

To substitute your own 320 x 240 pixel image, use a conversion tool like: https://lcd-image-converter.riuson.com/en/about/
To generate your own image, select the Color R8G8B8 conversion and set the Block size to 8 bits.

More images could be sent by using an SD card, to store these image data files.

The overlay text functionality is not being used in this example.

If you would like to learn more about the DDS frequency synthesis used in this code, AI may help (ChatGPT).
Use the following prompt: "Explain simply how a dds uses accumulation and phasing and sine lookups to create a frequency."

I have found that the RFI from the radio caused interference with the esp32-s3 and power supply. Using shielded wires from the esp32-s3 to the radio has helped significantly. (See attached images.)

GPIO 4 is used for the Speaker output, directly connected to the radio microphone input. For the UV5, this is the ring of the 3.5mm jack plug. (Bigger plug.)
GPIO 5 is the PTT control signal. This goes to the ground of above plug.
GPIO 6 is a spare wire, which may be used with a buzzer, if required.
GPIO 7 is to wake the esp32-s3 from deep sleep and resend the SSTV image. Connect momentarily to ground 0v.

73, Mat ZS6EG


