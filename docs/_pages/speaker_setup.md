---
title: "Speaker setup"
permalink: /speaker_setup/
excerpt: "How to quickly setup the speaker for use in the Indigenous Language Robots project."
date: 2018-09-13T05:04:41+00:00

toc: true
toc_icon: "clipboard-list"
toc_label: "Steps"
toc_sticky: true
---


The speaker ensures that the sound can be loud enough for use in public spaces (e.g. classroom). The speaker we use for the project is a *Sony SRS-XB10*, and should be paired with the [Tummy tablet](/ILR/tummy_setup) by following the steps described below.

## Unpacking the speaker

The tablet used for the head is a *Sony SRS-XB10* speaker. When unpacking it, the box should also contain a micro-usb cable that we will use to power it.

## Pairing the speaker with the tablet : speaker side
 
- Turn on the speaker by pressing the <i class="fas fa-power-off"></i> button

- Press and hold the <i class="fas fa-power-off"></i> button to prepare the speaker for pairing. The speaker should make a "beep" sound, and the LED indicator should start blinking
 
![speaker pairing](/ILR/assets/speaker/speaker.png){: .align-center width="75%"}

## Pairing the speaker with the tablet : tablet side

**Warning**: At this stage, your tablet should be connected to a network with internet access
{: .notice--danger}

- Make sure you connect your tablet to the internet (you can "drag" the settings menu from the top of the tablet screen to connect to another network).

- Open a web browser, and go to `https://play.google.com/app/testing/com.UQ.ILR`. You should see the following :

![ILR download](/ILR/assets/tummy/8.png){: .align-center width="75%"}

- Hit *Become a tester*. This will take you to a new page confirming that you joined the testing.

![ILR download](/ILR/assets/tummy/9.png){: .align-center width="75%"}

- Hit *Download it on Google Play*. This will take you to the google play store and give you the option to download the app.

**Note**: When you first open the Google Play store on a new tablet, the tablet may ask you to re-enter the email details. Make sure you use the robot email address.
{: .notice--info}

- Hit *Accept*. The Google Play store will ask you to grant access to "Wifi connection information" to the app. Hit *Allow* and the app should download.

- Once the app is downloaded, turn on the robot [router](/ILR/router_setup) and connect the tablet to its network (in the example below, the robot network is called *Stripey*)

- When you start the app for the first time, it will ask you to grant the app access to the microphone. Make sure you accept, as the microphone is used to record language productions.

**Note: At this stage, when you start the app, the screen will turn black and nothing will appear. This is normal, as there are currently no language resources on the tablet and the app needs them to work.**
{: .notice--info}

- **Restart your tablet now.**

## Setting up the Config file 

The `Config.txt` file contains the connection settings that enable the app to connect to the local robot network automatically. 

On your computer, create a text file called `Config.txt` (or modify the `Config.txt` file provided in the startup resources). The content of the file should be following:

```
{
"SSID":	"network_name_here",
"password": "network_password_here"
}
```

**Note**: In the file, replace the network name and corresponding password to match those you defined when setting up the [router](/ILR/router_setup)
{: .notice--info}

![Config file](/ILR/assets/tummy/configsetup.gif){: .align-center width="100%"}

## Uploading resources on the tablet

As part of the resources necessary to set up the robot, you should have a `start_up_resources` folder. The folder contains the Config.txt file (you should replace it with  the one you have created in the previous step) and some language resources (French is provided)

The startup resources folder should have the following structure:

```
start_up_resources
│   
│   Config.txt    
│
└───ExternalAssets
    │
    └───Instructions
    │   │   greetings.wav
    │   │   instructions_recall.wav
    │   │   ...
    │
    └───French
        │
        └───pictures
        │   │   pic0.jpg
        │   │   ...
        │
        └───sounds
        │   │   word0.wav
        │   │   ...
        │
        └───story
        │   └───masks
        │   └───pictures
        │   └───sounds
        │
        └───translations
        │   
        └───words
```

**Note**: When you create your own language resources (for instance using [Hermes](https://github.com/CoEDL/hermes)), they should be placed in a folder named after the language in the ExternalAssets folder
{: .notice--info}

- Restart the tummy tablet and connect it to your computer using the micro-usb cable

- Copy the content of the `start_up_resources` folder (including the `Config.txt` file and the `ExternalAssets` folder)

- Using the file explorer on your computer, navigate in the tablet memory to *Android->data->com.UQ.ILR->files*

**Warning**: If you can't find the *com.UQ.ILR* folder, it means that you probably haven't restarted the tablet correctly (or haven't installed the app)
{: .notice--danger}

- Drop the content of the `start_up_resources` folder at this location.

**Note**: It is useful to note that this location on the tablet (*Android->data->com.UQ.ILR->files*) is also where the raw user logs can be found, when the robot is being used (individual folders will be created, corresponding to each profile on the robot) 
{: .notice--info}

![Config file](/ILR/assets/tummy/dropresources.gif){: .align-center width="100%"}

- The app is ready to be used on the tablet !


Once these steps are complete, if you have not done it, proceed to [pair the Tummy tablet with the speaker](/ILR/speaker_setup).


