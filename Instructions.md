#Initial Steps

# Installing leJOS

- Windows 10, link: https://sourceforge.net/p/lejos/wiki/Windows%20Installation/

>Drivers problems, just install Lego Mindstorm software, with drivers included.
>Link: http://www.java-online.ch/lego/index.php?inhalt_links=home/nav_home.inc.php&inhalt_mitte=ev3install/usb_windows.inc.php&navUSB=ev3install/usb_windows.inc.php

- Download & install leJOS software;
- Import additional Sources (Samples);

# Installing Eclipse plugin
Link: https://sourceforge.net/p/lejos/wiki/Installing%20the%20Eclipse%20plugin/

# Installing IntelliJ plugin
Link: https://plugins.jetbrains.com/plugin/9954-lejos-plugin-for-lego-ev3-mindstorms

# Configuring network on lego EV3

- Wifi (only if you have a usb wifi board on Lego EV3), link: https://sourceforge.net/p/lejos/wiki/Configuring%20Wifi/

- USB sharing Wifi on Windows 10:
After install leJOS drivers (make sure that as  USB-Ethernet/RNDIS Gadget)
Next share the Internet with wifi network and EV3 network
Then on leJOS EV3, on PAN network, USB Client. To force the DHCP of Laptop wifi network get in action.

# Configure leJOS plugin

To update java program, we need to change the ip address to the right one.
We can use the leJOS software from eclipse called EV3 Control GUI tool to know what is the current IP, or by finding the ip addres from DHCP list.

After select the IP, compile and update your code.

# Upload JAVA program from terminal SSH
Link: https://sourceforge.net/p/lejos/wiki/Connecting%20to%20the%20EV3%20with%20ssh/

on terminal:
> ssh root@<IP ADDRESS>

in case of connection problem (diffie-hellman-group1-sha1), use
> ssh -oKexAlgorithms=+diffie-hellman-group1-sha1 root@<IP ADDRESS>

No password defined, just press enter. (note: Do not define password, it will be impossible to auto build with eclipse plugin)

Now copy your jar file from scp ~/lejos/samples/


Follow Official leJOS EV3 tutorial link: https://sourceforge.net/p/lejos/wiki/Getting%20started%20with%20leJOS%20EV3/
