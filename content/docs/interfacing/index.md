---
title: 'Interfacing with the System'
date: 2019-02-11T19:27:37+10:00
draft: false
weight: 3
---

The Bendit I/O Server works as an intermediary connec- tion between web-enabled performance interfaces and any Bendit I/O-enabled hacked devices. Performers can choose to host the server locally on their machine or remotely for globally-connected performances. When a new Bendit I/O board connects, the server collects the unique socket ID and MAC address and stores it into an array. It then replaces this ID with a nickname (which can be displayed in the user’s performance interface) and device color (displayed with the on-board LED), allowing for visual identification during performance. If the user is playing with a large num- ber of circuit-bent devices, the server code provides the abil- ity to group board ID’s into smaller subgroups, giving them the ability to enact a particular bend only on the devices in a subgroup, while executing different control commands over the rest of the ensemble. This is helpful when performing with a mixed collection of hacked devices, providing the performer the ability to communicate with their devices as if they were separate sections of an orchestra.

The server supports bidirectional messaging through socket.io. Any internet-enabled device, software, or custom-made web app that can format messages accordingly can serve as a means of communicating with devices on the network. Examples include web-based interfaces (e.g. web pages, social network/data API’s, Node-Red), MaxMSP, PureData,
SuperCollider, and other microcontrollers or microproces- sors (e.g. BeagleBone Black, Raspberry Pi, Particle Argon, etc.). The server responds to OSC-style messaging schemes with a focus on keeping the syntax streamlined and easy to format. Each message must begin by addressing the assigned device number or subgroup name of the desired BendIt board (ex: device/1/). The rest of the message ad- dresses the specific switch, pot channel, or motor channel to be activated, followed by a specific action and value. Table 1 shows a sample of common messages and resulting actions for performing devices attached to Bendit I/O boards. 

A complete list will be pubished soon. Please check back for updates in late June!

