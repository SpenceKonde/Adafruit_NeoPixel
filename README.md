# MODIFIED NeoPixel Library - removed use of digitalWrite/pinMode

Often, pinMode() is used only in setup() where it can be replaced by few lines of direct port manipulation. This can be useful when space is very tight, and you want to get rid of the overhead for the pinMode() function (which is larger than you'd expect, partly because it brings in the lookup tables for the DDR and PUE registers). However, the standard version of this library includes pinMode() calls. This frankly makes little sense in the first place - there's nothing fancy about the pin modes for driving neopixels, you just need it to be set output, which most sketches I see do already (redundantly). By removing the pinMode() calls, and placing the burden on the user to set the pin mode, this library provides the option of eliminating pinMode from the sketch, saving 250-300 bytes of flash. 


# Adafruit NeoPixel Library

Arduino library for controlling single-wire-based LED pixels and strip such as the [Adafruit 60 LED/meter Digital LED strip][strip], the [Adafruit FLORA RGB Smart Pixel][flora], the [Adafruit Breadboard-friendly RGB Smart Pixel][pixel], the [Adafruit NeoPixel Stick][stick], and the [Adafruit NeoPixel Shield][shield].

After downloading, rename folder to 'Adafruit_NeoPixel' and install in Arduino Libraries folder. Restart Arduino IDE, then open File->Sketchbook->Library->Adafruit_NeoPixel->strandtest sketch.

[flora]:  http://adafruit.com/products/1060
[strip]:  http://adafruit.com/products/1138
[pixel]:  http://adafruit.com/products/1312
[stick]:  http://adafruit.com/products/1426
[shield]: http://adafruit.com/products/1430
