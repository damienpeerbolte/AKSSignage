# AKSSignage - Digital Signage for the Raspberry Pi

## Installing on Raspbian

The command for installing AKSSignage on [Raspbian Lite(STRETCH NOT BUSTER!!)](https://www.raspberrypi.org/downloads/raspbian/) is:

```
$ bash <(curl -sL http://aksdev.nl/akssignage/install-aks.sh)
```

**This installation will take 15 minutes to several hours**, depending on variables such as:

 * The Raspberry Pi hardware version
 * The SD card
 * The internet connection

During ideal conditions (Raspberry Pi 3 Model B+, class 10 SD card and fast internet connection), the installation normally takes 15-30 minutes. On a Raspberry Pi Zero or Raspberry Pi Model B with a class 4 SD card, the installation will take hours. As such, it is usually a lot faster to use the provided disk images.

## Dockerized Development Environment

To simplify development of the server module of Screenly OSE, we've created a Docker container. This is intended to run on your local machine with the Screenly OSE repository mounted as a volume.

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
