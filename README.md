wireshark-plugin-mqtt
=====================

MQTT dissector plugin for wireshark


This project is a dissector plugin for wireshark based on the wireshark Generic Dissector.

It authorized Wireshark to identify and display clearly MQTT messages decoding fixed and variable header.

The full specification of protocole MQTT V3.1 is supported and managed.

## Installation

###wireshark Generic Dissector

For starting you need to download and install Wireshark Generic Dissector for your environnement.
Wireshark Generic Dissector is a generic plugin for Wireshark helping you to quickly develop plugins dissector.

It presents itself as a simple C library that you need to copy in one of the Wireshark plugins directories.

For more details on the project you can go here : http://wsgd.free.fr/index.html

Download and install the generic plugin corresponding to your environment in the download section : http://wsgd.free.fr/download.html

###Identify Wireshark plugins folder

Start Wireshark and verify your plugins folders as follows
Help -> About Wireshark -> Folders

You'll find informations about your personal plugins folder and the shared plugins folder :
* Personal Plugins : Your personnal plugins folder
* Global Plugins : Shared plugins for all users of Wireshark

Depending of your needs and your authorizations, choose one of them.

###Install the plugin

Copy the following files in the previously chosen directory :
* generic.so (or generic.dll on Windows)
* mqtt.fdesc
* mqtt.wsgd

The library will be automatically loaded at startup and will load in its turn the description of MQTT protocol.

###Verify the installation

The verification of the installation is very simple. you just need to start Wireshark and type mqtt in the Filter field.
Normally, there is an automatic completion helping you to find the MQTT protocol.
If MQTT appears in a green background then the installation is correct and you can start to decode MQTT messages.

If not, verify that the generic dissector plugin is well installed and loaded like this :
Help -> About Wireshark -> Plugins
Verify that dissector plugin generic.so (or generic.dll) is present.




