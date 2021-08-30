# USB-Drop-Test
This is for testing purposes only!

I Dropped USBs around My office to gather info on who would plug them into their PCs. Way cheaper then a Rubber Ducky and works on a normal USB.

All you need is an apache webserver and a USB drive. I used apache2 on a kali linux VM

On your Kali system, start apache2

systemctl start apache2

Then tail the access file

tail -f /var/log/apache2/access.log

In the leak.url file, edit the <ip of webserver> section with the ip or hostname of the apache server you are monitoring and save it.

load up your USB drive (not sure if it matters but mine was formated to ntfs) with the .url file. All this does is, when inserted and opened in explorer it reaches out to the server you input into the file to request the icon file while giving you their username and hostname so you can follow up with them and provide remedial training.
