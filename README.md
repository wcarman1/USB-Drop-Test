# USB-Drop-Test
This is for testing purposes only!

I Dropped USBs around My office to gather info on who would plug them into their PCs. Way cheaper then a Rubber Ducky and works on a normal USB.

All you need is an apache webserver and a USB drive. I used apache2 on a kali linux VM

On your Kali system, start apache2

```systemctl start apache2```

Then tail the access file

```tail -f /var/log/apache2/access.log```

In the leak.url file, edit the "ip of webserver" section with the ip or hostname of the apache server you are monitoring and save it. on the USB right click on the .url file and go to properties, General, check the "Hidden" box.

Load up your USB drive (not sure if it matters but mine was formated to ntfs) with the .url file. 

How it works:
When inserted and opened in explorer it reaches out to the server you input into the .url file to request the icon while giving you the requester's username and hostname so you can follow up with them and provide remedial training. If they click on the link it brings them to CISA's tips on USB devices. https://us-cert.cisa.gov/ics/tips/CSAR-10-114-02


# Tip

I usually attache a lanyard and some old keys to make it look like a personal item. I also add additional dummy files like excel does and stock photos to the USB drive.

I also like to include documents from CISA like https://us-cert.cisa.gov/sites/default/files/publications/RisksOfPortableDevices.pdf on the drive.

If you drop multiple usb(s) you can add a number to the request string. example ```...\usb-1.ico``` to track where you dropped it to which PC it ended up getting plugged into.
