# CTIF

An image format for OpenComputers and ComputerCraft. See releases for JAR converter binaries.

* [OpenComputers Thread/Examples](https://oc.cil.li/index.php?/topic/864-chenthread-image-format-high-quality-images-on-opencomputers/)
* [ComputerCraft Thread/Examples](http://www.computercraft.info/forums2/index.php?/topic/26186-chenthread-image-format-quality-images-on-18-computercraft)

# Usage

To run CTIFConverter, you need Java 8.

    java -jar CTIFConverter.jar -h

will be your best friend. Here's an example command:

    java -jar CTIFConverter.jar -m oc-tier3 -P preview.png -o image.ctif image.png

will convert image.png to image.ctif and kindly save preview.png as a preview file. (The "-P preview.png" can be omitted)

    java -jar CTIFConverter.jar -m cc -W 102 -H 57 -o image.ctif image.png

will convert your image into a ComputerCraft picture of at most 102x57. If you want to ignore the aspect ratio and force it to be 
exactly 102x57, use "-N".

## Note when running on Windows

Download **imagemagick** for java, then add the path to an env variable called `IM4JAVA_TOOLPATH`

# Viewers

If you just want to view CTIF files, see the viewers directory.

* ctif-cc.lua - ComputerCraft image viewer. "ctif-cc {file} [monitor side]" to use. If it errors about the image size being too 
large, keep in mind it operates on *characters*, while the converter operates on *pixels* - to convert from one to the other, 
multiply the width by 2 and the height by 3.

* ctif-oc.lua - OpenComputers image viewer. Not optimized - expect it to load images slower than what you saw at BTM. Requires Lua 5.3.

An optimized OpenComputers viewer will be released as part of the promised-at-BTM15 release of OpenPoint soon.

## OpenComputers note

To run this, you need to set the `CPU`'s architecture to **Lua 5.3**, to do this, just *sneak-click the cpu while holding it*.
