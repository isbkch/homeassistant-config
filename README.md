# Home Assistant Configuration

Here's my [Home Assistant](https://home-assistant.io/) configuration. I have installed HA on a [Lenovo ThinkCentre M93P Tiny](https://amzn.to/3bCllLi/) with an Intel Dual-Core i5-4570T Processor up to 3.60 GHz, 8GB RAM and 240GB SSD. I am currently running [HA OS](https://github.com/home-assistant/operating-system) directly on the NUC and use a [ConBee II USB](https://amzn.to/3EF6LPn) as Zigbee Gateway

I regularly update my configuration files. If you like anything here, Be sure to :star2: my repo!

## Some of the devices and services that I use with HA

### Amazon Echo Devices

We use Amazon devices to start/stop automations: "Alexa, prepare the gym", to target specific devices: "Alexa, open the master bedroom blinds" and as speakers to listen to music: "Alexa, play Taylor Swift on Spotify". The DOTs are littered around the house, and we use them to communicate rather than shouting at each other.

| [Amazon Echo Show](https://amzn.to/3k7K0fl) | [Amazon Echo (3nd Gen)](https://amzn.to/3EQyNHP) | [Echo Dot (3nd Gen)](https://amzn.to/301FVSs) | [Echo Dot (4th Gen)](https://amzn.to/3BQYfv3) | [Echo Flex](https://amzn.to/303Ghsk) |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| [<img height="150" src="https://m.media-amazon.com/images/I/510lFo8UR0S._AC_SL1000_.jpg">](https://amzn.to/3k7K0fl) | [<img height="150" src="https://m.media-amazon.com/images/I/615DcmT2o5L._AC_SL1000_.jpg">](https://amzn.to/3EQyNHP) | [<img height="100" src="https://m.media-amazon.com/images/I/6182S7MYC2L._AC_SL1000_.jpg">](https://amzn.to/301FVSs) | [<img width="170" src="https://m.media-amazon.com/images/I/71fm-oidY3L._AC_SL1000_.jpg">](https://amzn.to/3BQYfv3) | [<img height="150" src="https://m.media-amazon.com/images/I/41fTockMHSL._AC_SL1000_.jpg">](https://amzn.to/303Ghsk)

### Indoor Cameras

[Yi 1080](https://amzn.to/3w9Ppax) Wireless IP Security Indoor Camera.

[<img height="250" src="https://m.media-amazon.com/images/I/518Ngm46uuL._AC_SL1500_.jpg">](https://amzn.to/3w9Ppax)

I like using this camera because of how easy it is to flash with a [custom firmware](https://github.com/roleoroleo/yi-hack-Allwinner) making sure all images stays local within my HA instance and nothing goes to the cloud. I have it set up to automatically take pictures when movement is detected and send me notifications on my iPhone and Apple watch. Here's a [link to watch](https://www.youtube.com/watch?v=GCHYBxnZK-E) a step by step video on how I set it up.

<img width="250" src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/security_camera.png?raw=true">

### Outdoor Cameras

[Blink Outdoor](https://amzn.to/3CIKj6M) Wireless, Weather-resistant & Battery Powered.

[<img height="250" src="https://m.media-amazon.com/images/I/61TRYGIDWkL._SL1000_.jpg">](https://amzn.to/3CIKj6M)

I like using this camera kit because it's wireless, weather-resistant, HD, with two-year battery life and has motion detection.
because it's powered via battery, I couldn't afford it streaming live all the time- Although I might end up getting [this solar panel](https://amzn.to/30YdaqA) model for it. For now, I have it set up to refresh automatically when I click the image picture in my dashboard using [this script](https://github.com/isbkch/homeassistant-config/blob/main/scripts.yaml#L74).

My script puts the picture under the folder `/config/www/camera_cabanon/` so make sure the folder is created beforehand. I also like to use the `media browser` to browse the pictures, so make sure you have declared the folder like [I did here](https://github.com/isbkch/homeassistant-config/blob/main/integrations/home_assistant.yaml#L6).

<img width="600" src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/camera_blink_2.png?raw=true">

### Motion Detectors

I use 2 brands of ZigBee Motion Sensor to detect movement and trigger automations

* These [SONOFF SNZB-03](https://amzn.to/31hJCEi). They are small and discreet but I found them to be fragile and unreliable.
* These [Hacbop ZigBee PIR](https://amzn.to/3q2V8xV) that are a little bit more expensive than the [SONOFF SNZB-03](https://amzn.to/31hJCEi) but they are more reliable and have a longer battery life.

I also use the [SONOFF SNZB-04](https://amzn.to/31tMnTd) Door & Window Sensor to detect when a door or window is opened in order to send notifications and/or trigger automation

| [SONOFF SNZB-03](https://amzn.to/31hJCEi) | [Hacbop ZigBee PIR](https://amzn.to/3q2V8xV) | [SONOFF SNZB-04](https://amzn.to/31tMnTd) |
| ----------- | ----------- | ----------- |
| [<img height="250" src="https://m.media-amazon.com/images/I/51grJ93MlxL._AC_SL1000_.jpg">](https://amzn.to/31hJCEi) | [<img height="250" src="https://m.media-amazon.com/images/I/51NhalPh1zL._AC_SL1500_.jpg">](https://amzn.to/3q2V8xV) | [<img height="250" src="https://i5.walmartimages.com/asr/8d9d4cd5-876e-4b3a-bb6a-16c6a8ef514e.87ae5c04b2e27210f64cd5c53755fe50.jpeg?odnHeight=450&odnWidth=450&odnBg=ffffff">](https://amzn.to/31tMnTd)


### IKEA TRÅDFRI

I shopped a lot for smart, motorized blinds before deciding to get these [IKEA FYRTUR](https://www.ikea.com/ca/en/p/fyrtur-blackout-roller-blind-wireless-battery-operated-gray-00408216/). They are relatively cheap but have good build quality. They do require, however, the use of the [TRADFRI Hub](https://www.ikea.com/ca/en/p/tradfri-gateway-white-00337813/) and IKEA mobile app, luckily, the [HA integration](https://www.home-assistant.io/integrations/tradfri/) (Zigbee-based) works pretty well and it's easy to setup.

| [TRÅDFRI Gateway](https://www.ikea.com/ca/en/p/tradfri-gateway-white-00337813/) | [FYRTUR Blinds](https://www.ikea.com/ca/en/p/fyrtur-blackout-roller-blind-wireless-battery-operated-gray-00408216/) |
| ----------- | ----------- |
| [<img height="250" src="https://www.ikea.com/ca/en/images/products/tradfri-gateway-white__0974247_pe812322_s5.jpg?f=xl">](https://www.ikea.com/ca/en/p/tradfri-gateway-white-00337813/) | [<img height="250" src="https://www.ikea.com/ca/en/images/products/fyrtur-blackout-roller-blind-wireless-battery-operated-gray__0595177_pe675958_s5.jpg?f=xl">](https://www.ikea.com/ca/en/p/fyrtur-blackout-roller-blind-wireless-battery-operated-gray-00408216/) |

### Plugs & Energy Consumption

I like my plugs to monitor energy consumption as well. This is the main reason I go with [Emporia](https://amzn.to/307EHWn). They are very cheap (4 plugs for $69 CAD), and easy to connect with HA through the [Emporia Vue integration](https://github.com/magico13/ha-emporia-vue). Upon the first connection, the integration creates multiple sensors showing energy consumption per minute, day and month. And that's all I need to track usage and build my energy dashboards.

<img width="500" src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/plug_1.png?raw=true" /> <img height="260" src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/plug_2.png?raw=true" />


### DIY (Arduino + ESP32 + ESP8266)

* WIP

## Automation: Turn on/off lights when someone walks in/out of a room

I have put various instances of the [SONOFF SNZB-03](https://amzn.to/31hJCEi) in strategic places around my house to detect movement and turn on/off lights. This one for example is placed at the top of the stairs to detect when someone is walking down towards the kitchen. This movement detection then triggers [this automation](https://github.com/isbkch/homeassistant-config/blob/main/automations.yaml#L910) that switches on the lights in the kitchen, then switches them off again when no movement is detected after 2 minutes.

<img width="450" src="https://github.com/isbkch/homeassistant-config/blob/main/repo_documents/motion_5.jpeg?raw=true">

## Automation: Cats want to come in

When one of my cats wants to come in, they usually come to the door and start peeking inside trying to get our attention.
I have put this [Hacbop PIR Motion detector](https://amzn.to/3q2V8xV) right at the edge of the door. When it detects a motion, it triggers [this automation](https://github.com/isbkch/homeassistant-config/blob/main/automations.yaml#L544) that asks my home camera at the back to take a picture and send it to my iPhone.

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
