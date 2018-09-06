---
title: "Head tablet Setup"
permalink: /head_setup/
excerpt: "How to quickly install and setup the head tablet for use in the Indigenous Language Robots project."


toc: true
toc_icon: "clipboard-list"
toc_label: "Steps"
toc_sticky: true
---

The router is responsible for setting up the local network used by all components of the robot to talk to each other.

## Unpacking the router

The router we are using in this project is a TP Link mini router TL-WR810N. When unpacking it, the box should contain:

- the router 
- one micro-usb cable (used for powering the router)
- one ethernet cable (we will use it later to connect the [raspberry pi](/ILR/rpi_setup/) to the router)

![router image](/ILR/assets/router/router.jpg){: .align-left width="50%"}  Prior to setting up the router, look at the back of it and note the SSID and password (they will be needed to connect to the router)

## Connecting to the router
{: .text-nowrap}

Power the router and, from your computer, connect to it via Wifi (The network id and password will be the one at the back of the router)

Once your computer is connected to the router local network, open a web browser and type *192.168.0.1* to access the router settings page. The browser should display the page below:

![admin interface](/ILR/assets/router/1.png){: .align-center width="100%"}  

Enter the default login (*admin*) and password (*admin*) to access the router settings page.

**Note**: On TP Link wifi, the interface can also be accessed by typing *tplinkwifi.net/* in the browser. It is also possible to change the admin login and password from this interface (but not necessary for the robot to work).
{: .notice--info}

## Router settings

Once in the router settings interface, apply the settings below one by one:

**Warning**: These changes will prompt the router to restart. You will have to connect to it again before you can proceed.
{: .notice--warning}

1. Set the **Operation Mode** as *Access Point*

![setting access point](/ILR/assets/router/2.png){: .align-center width="100%"}  

2. In **Wireless->Basic Settings**,  change the network name (give it the name of your robot, for instance).

![setting access point](/ILR/assets/router/3.png){: .align-center width="100%"}

**Note**: Changing the name of the network is optional but recommended, as it heps identify the robot better. In addition, you can also change the network password in **Wireless->Wireless Security**
{: .notice--info} 

## Address reservation for the Raspberry Pi

The Raspberry Pi has been set up in a [previous step](/ILR/rpi_setup/). To operate normally, the Pi needs to be use a static IP address on the network. This steps goes through adress reservation for the Pi.

1. Make sure the Raspberry Pi is off, and connect it to the router using the ethernet cable.

2. Turn on the Raspberry Pi.

3. On your computer, connect to the router admin interface and go to **DHCP->DHCP Client List**. You should see the raspberry pi in the list of the clients.

![DHCP clients](/ILR/assets/router/5.png){: .align-center width="100%"}

**Note**: The raspberry pi can take a minute or so to connect to the network. Hit *Refresh* if you can't see it.
{: .notice--info}

4. Copy the MAC address of the Raspberry Pi.

5. In **DHCP->Address Reservation**, hit **Add New**. Create a new address reservation by pasting the MAC address of the Raspberry Pi, setting its IP address to *192.168.0.2*, and setting its status as *Enabled*

![DHCP address reservation](/ILR/assets/router/7.png){: .align-center width="100%"}

**Warning**: The address reservation will take effect only after restarting the router. Next time you restart the router, if you go to **DHCP->DHCP Client List**, the Raspberry Pi should be listed with an IP of *192.168.0.2* and a "permanent" lease time.
{: .notice--warning}


Once these steps are complete, you can proceed to setting up the [Head tablet](/ILR/head_setup).
