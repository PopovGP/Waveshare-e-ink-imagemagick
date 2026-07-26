# How to make images for Waveshare 7.3inch E6 Full Color E-Paper using Image magick

Waveshare e-ink display can show only 6 colors: Black, White, Green, Blue, Red, Yellow, 
so you cannot use any image for it, but using Image magick you can convert any image to use with this display.

Display homepage:

[https://www.waveshare.com/rpi-zero-photopainter-acce.htm](https://www.waveshare.com/rpi-zero-photopainter-acce.htm)


Display wiki:

[https://www.waveshare.com/wiki/RPi_Zero_PhotoPainter](https://www.waveshare.com/wiki/RPi_Zero_PhotoPainter)


# 1. Install Image magick

[https://imagemagick.org/](https://imagemagick.org/)

on MacOS

``
brew install imagemagick
``

# 2. Now you can convert one image or all at once

## 2.1. Convert one image

To convert `pic.jpeg` to `pic.bmp` use this command:

``
magick pic.jpeg -resize 800x480 -background white -gravity center -extent 800x480 -dither FloydSteinberg -remap colortable-2.gif pic.bmp
``

`magick` - main command

`pic.jpeg` - image to convert

`-resize 800x480` - resize image to 800 pixels width and 480 pixels height 

`-background white` - if image is smaller then fill background with white

`-gravity center -extent 800x480` - this centers the original image inside a new white 800 × 600 pixel canvas

`-dither FloydSteinberg` - make Floyd-Steinberg dithering

`-remap colortable-2.gif` - use colors from this file. It is compulsory.

Download colortable-2.gif here: [colortable-2](colortable-2.gif)



