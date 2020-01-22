# AKS Signage - Digital Signage for the Raspberry Pi

## Disk images

The recommended installation method is to grab the latest disk image from [here](https://github.com/damienpeerbolte/AKSSignage/releases).

## Installing on Raspbian

The command for installing AKS Signage on [Raspbian Lite](https://www.raspberrypi.org/downloads/raspbian/) is:

```
$ bash <(curl -sL http://aksdev.nl/akssignage/install-aks.sh)
```

**This installation will take 15 minutes to several hours**, depending on variables such as:

 * The Raspberry Pi hardware version
 * The SD card
 * The internet connection

During ideal conditions (Raspberry Pi 3 Model B+, class 10 SD card and fast internet connection), the installation normally takes 15-30 minutes. On a Raspberry Pi Zero or Raspberry Pi Model B with a class 4 SD card, the installation will take hours. As such, it is usually a lot faster to use the provided disk images.

AKS Signage works on all Raspberry Pi versions, including Raspberry Pi Zero and Raspberry Pi 3 Model B.
