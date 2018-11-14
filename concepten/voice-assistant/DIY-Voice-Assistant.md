# Build your own open-source voice assistant

## Hardware 
* Raspberry Pi 3/3B+ (see compatibility chart above)
* Micro SD card, 8GB or larger _highly_ recommended
* Power adapter with micro USB for your country.
* An analog Speaker that can be plugged into the 3.5mm audio jack on the RPi 3 or a Bluetooth speaker
* USB Microphone or a traditional microphone with a 3.5mm microphone jack.

'For my setup I use an 7.1 Channel USB External Sound Card Audio Adapter to improve the playback sound quality of the voice.'

![7.1 Channel USB External Sound Card Audio Adapter](https://i.imgur.com/gemSYbl.jpg "7.1 Channel USB External Sound Card Audio Adapter")


Optional

* USB keyboard (required for setting up)
* Monitor or TV connected via HDMI cable (required for setting up)
* Ethernet cable (if not connecting via WiFi)

#### Hardware recommendations

Below is information on specific hardware that has been tested with Jarvis. If you have further recommendations, please raise an Issue or a Pull Request (PR) on this page.

##### Working Microphones

* **Blue Snoball/Snoball Ice** - Works very well
* **CM108 Based Mics** - The CM108 chip drives many low-priced microphones in various form-factors (if you run `lsusb` you'll see them as _C-Media Electronics, Inc. CM108 Audio Controller_.  All work, but some are better than others for Picroft purposes.
   * eBerry Plug and Play Home Studio - decent experience, fair range
   * Kinobo Makio - functional, but only works at close range
* **[Jabra Speak410 USB Speakerphone](http://amzn.to/2kriCvh)** - Microphone and Speaker in the same device. Microphone range is good and speaker sound is loud and crisp.
* **[mVox USB Speakerphone](http://amzn.to/2jYCxR3)** - Microphone and Speaker in the same device. Microphone range is poor and speaker sound is bad compared to the Jabra Speak410.
* **[PS3 Eye Camera](http://amzn.to/2jFC6MP)** - Affordable and microphone range is good.


##### Working Speakers

* **Logitech Z50** - Mono speaker, wired, simple, can be found for cheap.

### Getting Started

#### Downloading the disk image

First, download the [disk image](https://).

#### Burn the disk image to the Micro SD card

Next, the disk image needs to be burnt to the Micro SD card.
The [Raspberry Pi official documentation provides an excellent tutorial](https://www.raspberrypi.org/documentation/installation/installing-images/) on this, using Etcher software. We recommend that you burn the Picroft image to the Micro SD card using Etcher.

![Etcher SD card image burning tool](https://i.imgur.com/gcBSiBd.png "Etcher SD card image burning tool")

If you prefer to use the Linux command line tool `dd` to burn the disk image instead, follow these instructions: 

1. Download the [disk image](https://)
2. Insert the Micro SD card you wish to burn the image to. It must have a storage capacity of 8GB or higher. 
3. Identify the path where the MicroSD card is mounted by running the command `sudo fdisk -l`. You will be able to tell the path based on the storage size of the device.
4. Keep a note of this - it will be something like `/dev/sdb1`
5. Unmount the disk so that no other operation can write to the device while it is being imaged using the command `sudo umount /dev/sdb1`. Make sure to substitute for the location of your device. 
5. Run the command `sudo dd if=path-to-your-image.img of=/dev/sdb1 bs=20M`. Make sure to substitute the location of your device, and the path to the `.img` file you downloaded.
6. This will take several minutes to run. The command prompt will return if successful, otherwise an error message will be displayed on your terminal.

#### Booting up Jarvis

Once you've burned the disk image to the Micro SD card, insert the Micro SD card into the Micro SD card slot on the Raspberry Pi. Plug in your microphone, speakers, and if you're using a monitor and/or keyboard, plug these in too.

Next, plug in the power and switch the power on.

Our next step is to connect Jarvis to the internet. 

####  Getting Jarvis connected to the internet using a network cable

Plug the Jarvis into your router using an ethernet cable plugged into the RJ45 port on the Raspberry Pi.

When Jarvis boots, it will look for a network connection and will prompt you to set up a WiFi connection if a wired connection is not found.

#### Getting Jarvis connected to the internet using Wifi

Using your computer or a mobile device, connect to the Wifi SSID `Jarvis` using the password `We have a Hulk`. O
* Ensure you know the IP address of Jarvis on your network. A handy way to do this is to install the IP Address **Skill**, and then Speak:

> Yo Jarvis, what's your IP address?

`"This is my wlan IP address ..."`

* Open up your favorite terminal program, like PuTTy on Windows, or a new terminal on Linux
* `ssh Jarvis@IPADDRESS`
* The default password is `We have a Hulk`, so enter this when prompted.
* If you have successfully logged in via SSH you will see a command prompt like the one below:

```
$ ssh Jarvis@192.168.0.2
Jarvis@192.168.0.2's password:

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Sun Nov 4 10:40:21 2018
Jarvis@VA:~ $
```

