# Home Assistant Configuration

Here's my [Home Assistant](https://home-assistant.io/) configuration. I have installed HA on a [Lenovo ThinkCentre M93P Tiny](https://amzn.to/3bCllLi/) with an Intel Dual-Core i5-4570T Processor up to 3.60 GHz, 8GB RAM and 240GB SSD. I am currently running HA OS directly on the NUC and use a [ConBee II USB](https://amzn.to/3EF6LPn) as Zigbee Gateway

I regularly update my configuration files. If you like anything here, Be sure to :star2: my repo!

## Some of the devices and services that I use with HA

### Lights and Switches

* WIP

### Cameras

[Yi 1080](https://amzn.to/3w9Ppax) Wireless IP Security Camera.

I like using this camera because of how easy it is to flash with a custom firmware, so all images stays local within my HA instance and nothing goes to the cloud.

I have it set up to automatically take pictures when movement is detected and send me notifications on my iPhone and Apple watch. Here's a [link to watch](https://www.youtube.com/watch?v=GCHYBxnZK-E) a step by step video on how I set it up.

<img width="250" src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/security_camera.png?raw=true">

### Motion Detectors

I use 2 brands of ZigBee Motion Sensor to detect movement and trigger automations

* These [SONOFF SNZB-03](https://amzn.to/31hJCEi). They are small and discreet but I found them to be fragile and unreliable.
* These [Hacbop ZigBee PIR](https://amzn.to/3q2V8xV) that are a little bit more expensive than the [SONOFF SNZB-03](https://amzn.to/31hJCEi) but they are more reliable and have a longer battery life.

I also use the [SONOFF SNZB-04](https://amzn.to/31tMnTd) Door & Window Sensor to detect when a door or window is opened in order to send notifications and/or trigger automation

### Plugs

* WIP

### Buttons

* WIP

### Voice Interaction

* WIP

### Notifications

* WIP

### Weather and Climate related

* WIP

### DIY (Arduino + ESP32 + ESP8266)

* WIP

## Automation: Cats want to come in

When one of my cats wants to come in, they usually come to the door and start peeking inside trying to get our attention.
I have put this [Hacbop PIR Motion detector](https://amzn.to/3q2V8xV) right at the edge of the door. When it detects a motion, it triggers an automation that asks my home camera at the back to take a picture and send it to my iPhone.

Here is where the PIR motion detector is placed

<img width="450" src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/motion_1.png?raw=true"> <img width="350" src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/motion_2.png?raw=true">

And here is what the camera screenshot looks like

<img width="450" src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/motion_3.jpeg?raw=true"> <img height="350" src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/motion_4.png?raw=true">

## My Home Assistant dashboard

I have one tab for every floor in my house and I put all smart devices of the same floor in the same tab.
I also use one tab for all scenes, one for energy details and one for system monitoring.
Here are some screenshots (please note that these may not be the most updated images, but you should get an idea).

<img src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/ha_ss_1.png?raw=true" alt="Home Assistant dashboard" />

<img src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/ha_ss_2.png?raw=true" alt="Home Assistant dashboard" />

<img src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/ha_ss_5.png?raw=true" alt="Home Assistant dashboard" />

<img src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/ha_ss_4.png?raw=true" alt="Home Assistant dashboard" />

<img src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/ha_ss_6.png?raw=true" alt="Home Assistant dashboard" />

<img src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/ha_ss_3.png?raw=true" alt="Home Assistant dashboard" />
