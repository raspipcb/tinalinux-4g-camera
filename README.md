# tinalinux-4g-camera
Tina-Linux based 4G USB camera

## Setting Up the Tinalinux Build Environment

1. Download the Ubuntu VMware image from this [Google Drive link](https://drive.google.com/drive/folders/1lrqDsxtGl8WvU7o547lT9IkHwGyAHXFU?spm=a2g0o.detail.1000023.1.74524KRw4KRwT2) located in the VOS folder.
2. Extract the image and open it in VMware.
3. Build the SDK following the manufacturer’s [wikipage](http://wiki.lctech.cc/index.php?title=LC-PI-T113).

### Steps to Build Tina-Linux

Navigate to `~/LC/Tina-Linux` and execute the following commands:
```shell
source build/envsetup.sh
lunch
```
Select your board accordingly. With the build environment enabled, configure Tina-Linux using the following commands:

#### Linux Kernel Configuration
```shell
m kernel_menuconfig
```

#### OpenWRT Configuration
```shell
m menuconfig
```

### Building Tina-Linux

After completing the configuration, build Tina-Linux by running:
```shell
build
```
During the compilation process, confirm all prompts when prompted.

### Generating the Final Image

Once the compilation is complete, execute the following commands to generate the final image:
```shell
mboot
pack
```
After running these commands, the location of the generated image will be displayed.