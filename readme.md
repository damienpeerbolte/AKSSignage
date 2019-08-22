[![Build Status](https://travis-ci.org/Screenly/screenly-ose.svg?branch=master)](https://travis-ci.org/Screenly/screenly-ose)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/5905ebcf4aab4220ad9fdf3fb679c49d)](https://www.codacy.com/app/vpetersson/screenly-ose?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Screenly/screenly-ose&amp;utm_campaign=Badge_Grade)

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

## Quick links:

 * [FAQ](https://support.screenly.io/hc/en-us/sections/202652366-Frequently-Asked-Questions-FAQ-)
 * [Screenly OSE Forum](https://forums.screenly.io/c/screenly-ose)
 * [Screenly OSE Home](https://www.screenly.io/ose/)
 * [Live Demo](http://ose.demo.screenlyapp.com/)
 * [QA Checklist](https://www.forgett.com/checklist/1789089623)
 * [API Docs](http://ose.demo.screenlyapp.com/api/docs/)

Screenly OSE works on all Raspberry Pi versions, including Raspberry Pi Zero and Raspberry Pi 3 Model B.

## Dockerized Development Environment

To simplify development of the server module of AKS Signage, we've created a Docker container. This is intended to run on your local machine with the AKS Signage repository mounted as a volume.

Assuming you're in the source code repository, simply run:

```
$ docker run --rm -it \
    --name=screenly-dev \
    -e 'LISTEN=0.0.0.0' \
    -p 8080:8080 \
    -v $(pwd):/home/pi/screenly \
    screenly/ose-dev-server
```

## Running the Unit Tests

    nosetests --with-doctest
