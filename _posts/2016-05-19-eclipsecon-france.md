---
layout: post
title: Smart Home Technology at EclipseCon France
date: '2016-05-18T00:00:00.001+02:00'
author: Kai Kreuzer
tags:
- eclipse
- eclipsecon
- openhab
modified_time: '2016-05-18T00:00:00.001+02:00'
header-img: "img/2016-05_ecf.jpg"
excerpt_separator: <!--more-->
---

[EclipseCon France](https://www.eclipsecon.org/france2016) is less than three weeks away from now and I am very much looking forward to it! It is the first time for me to attend an EclipseCon in France and also to visit the city of Toulouse - my main encounter with the French Smart Home community has been an [Eclipse Day in Grenoble](http://www.kaikreuzer.de/2015/04/01/recap-of-eclipse-iot-days-grenoble/) last year, which was much fun.

<!--more-->

In [my session "Home Automation Reloaded" at EclipseCon France](https://www.eclipsecon.org/france2016/session/home-automation-reloaded), I will cover different topics around smart homes: 

- Diving into the Smart Home market means dealing with the huge interoperability issues that everyone comes across sooner or later. It is important to see [why Open Source is a suitable way to address this](https://ianskerrett.wordpress.com/2016/04/22/can-open-source-solve-the-too-many-iot-standards-problem/).
- An introduction to the concepts and the architecture of the [Eclipse SmartHome project](https://www.eclipse.org/smarthome/) follows. A special focus will of course be on the very latest developments like the user interfaces for system administration, the new rule engine as well as all the work that is going on around voice enabling smart home solutions through features like text-to-speech (TTS), speech-to-text (STT) and even natural language processing (NLP).
- As it is usually best to learn from example (and people love live demos!), I will also bring real hardware with me and use [openHAB 2](https://github.com/openhab/openhab-distro#introduction) for demonstration purposes.

{:.center}
![Paper UI]({{ base }}/img/2016-05_screenshot1.jpg)
<small>openHAB automatically discovering devices</small>

As openHAB 2 is still in beta phase, I am currently working hard on getting a beta3 out. There have been tremendous efforts on the code since the beta2 release and thus I believe it will be a major milestone towards a first stable release. 

Besides the many new features that come officially with the distribution,  I have now also introduced experimental features that can be activated. The new rule engine is such a feature: It is fully controllable through the REST API, and it is therefore possible to create graphical rule editors, which construct and edit rules as JSON structures - for advanced use cases, it is even possible to send Javascript as part of the rules. Many further possibilities will follow, like full support for JSR223 (alternative script engines) or the integration of CalDAV servers for rule triggering and the integration of the existing openHAB 1 Xtext DSL rules (which use Xbase).

{:.center}
![Rule UI]({{ base }}/img/2016-05_screenshot2.jpg)
<small>The new experimental rule editor</small>

The openHAB 2 beta 3 will also be the one shipped with the [Pine64 IoT package](http://www.pine64.com/) - this will allow the quickest start with Eclipse SmartHome ever - simply insert the SD card, power it up and all is ready to start playing! If you are interested in learning more about the Pine64 board: Come and see me at EclipseCon France, I will have one with me!

{:.center}
![Pine64]({{ base }}/img/2016-05_pine64.jpg)
<small>The Pine64 is the cheapest way (just $15) to get started with Eclipse SmartHome</small>

You see that a lot of fascinating things are going on - and this is just about one project in the Eclipse IoT space, while there is a lot more to discover at EclipseCon France. So don't miss to register for the conference asap and meet me and the rest of the Eclipse community in Toulouse!
