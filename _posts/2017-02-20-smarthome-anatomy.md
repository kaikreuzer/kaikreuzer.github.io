---
layout: post
title: The Anatomy of Smart Homes
date: '2017-02-20T00:00:00.001+00:00'
author: Kai Kreuzer
tags:
- smarthome
modified_time: '2017-02-20T00:00:00.001+00:00'
header-img: "img/2017-02_bricks.jpg"
excerpt_separator: <!--more-->
---

Scott Jenson published a [very good article](https://medium.theuxblog.com/the-future-iot-building-better-legos-43047e17ad4c#.kihaq7usy) last week, where he nicely showed how far away we still are from the shiny Jetson-like marketing promises about smart homes. He asked us to take a step back so that we can think about the holistic shape of the "right" solution for smart homes. **Let's do so!**

<!--more-->

## Missing Technology?

Doing a shameless shortening of his thoughts, he concluded that many issues would be solved if all devices had

1. a smart setup that allows users a very simple way of commissioning
1. auto-arrangement through proximity-detection
1. a globally accepted way of announcing their capabilities
1. a mechanism to share their data instead of keeping it in a silo

These are the technologies that we as a community are still lacking and that need to be tackled.
Only if these are in place, it will enable devices to automatically form a distributed ensemble which we all aim for.

While I very much agree with all his points, I believe that solving the technological issues alone won't suffice, but that we need to take yet another step back to see the big picture.

## Taking Another Step Back

When talking about adding IoT devices to "the network", it is out of question for most people to wonder "which network" - since we are talking about the *Internet of Things*, the network can only be *The Internet* where everything is connected, right?

### Silos and Accounts

If we have a closer look at today's smart home devices (and also other IoT setups), the truth is that everyone uses IP, i.e. Internet *technology*. But are the devices available "on the Internet"? No, many of them effectively do not allow you to communicate in any direct way with them. Instead, they open an encrypted tunnel to a cloud service, which then acts as a portal to the device for the user - all data is kept secretly (not saying securely) in the cloud under full control of the manufacturer. Effectively, we have a big number of siloes that can be regarded as VPNs. It is important to note that these are deliberate silos - this choice is not (only) the fault of missing interoperability standards!

This setup is a major reason for Scotts points 1 (smart setup) and 4 (sharing data): The manufacturers do not want to give control to the users, but instead force them to create accounts at their cloud service, accept the manufacturers terms and conditions and let the manufacturer decide how and with whom to share the data.

This is the major issue that needs to be addressed: The mindset of people that are building IoT devices must move away from this omni-present IoT architecture. The outlook that users will have to create web accounts for every single household object (everything's going to be connected, right?) they buy in the future is ridiculous. This works as long as only nerds with a dozen devices play around with smart homes, but it definitely won't scale. Manufacturers must let their devices go - only if they are unleashed the devices will have a chance to communicate with each other and form distributed ensembles.
<video width="100%" autoplay loop muted>
    <source src="http://www.openhab.org/assets/smarthome.mp4" type="video/mp4">
</video>

### Internet vs. Intranet

Let's for the moment assume the devices were unleashed. Is the Internet then really the best place for them? Even if all potential authentication and authorization issues were solved, we all know that all those devices are hackable. Do we really want to see them publicly listed on [Shodan.io](https://www.shodan.io/)? Having isolated VPNs isn't such a bad idea after all and in the case of the smart home [the most natural fit is the local Intranet](2014/02/10/privacy-in-smart-home-why-we-need/). What you want to have on the public Internet are services (hosted on "real" servers that are hardened against attacks) and not household devices. A good compromise is in my opinion the concept of the [Physical Web](https://google.github.io/physical-web/), where the discovery and authorization could be done through low-range radio like BLE, while the heavy lifting is done through cloud servers - but this really hardly applies to the smart home itself. If services of a home should be shared (this decision should really be up the user), it could be made available on any standard-compliant cloud service (i.e. no vendor lock-in), once Lego brick 3 (Standard Descriptions) is in place. Unfortunately, I am not as optimistic as Scott to have a "shared, common approach soon" - maybe for technical operability, but most likely not for [semantical interoperability](/2016/03/21/semantic-interoperability-in-internet/).

### A Matter of Perspective

Taking the perspective of the user instead of the perspective of the manufacturer definitely brings us much closer to the desired solution. But putting *the user* in the center also causes some dilemma in the context of a smart home: After all, a home usually has multiple inhabitants, furthermore there are visitors, pets, burglars (hopefully not), etc. For the home to become smart and autonomous, the devices must become an integral part of the home and must not be a property of a single user. This is another clear indicator that we are still in an early phase: Most devices are bought off-the-shelf, installed DIY and registered to a certain user, who configures it to meet his needs. The devices are the personal objects of a person; they are not a part of the home. If this person moves the house, he will take his personal belongings with him. This works as long as you have only a dozen smart bulbs, a door lock and a web cam. It won't work - and especially it does not make any sense - for a photovoltaic system, a complex central heating, the in-wall motion sensors, the smart frontdoor,... you get the point. You are also not ripping out the wall switches and your windows when you sell a house. A smart home should be allowed to exist on its own, even if nobody lives there. What brings it into existence are its bricks and its infrastructure - including the local IP network as the communicatin backbone for its parts.

### Water, Electricity, Smartness

Smart home features and connectivity thus have to become a matter of course, just like electricity or water - it should not be treated as something that is retrofitted by the owner; instead, it must be an integral part of a home, which in turn becomes a smart, self-organizing entity. Having the devices build a local private network would ensure data privacy and the smallest possible attack target. **This** should be the long-term vision when designing smart home devices. In consequence, this means that devices must

1. not require a mandatory user registration
1. work (at least in a basic way) without a cloud connection
1. provide a local API for interaction with other devices (and not limiting access to a small set of business-oriented partnerships) and expect the same from the others

In short, things should focus again on being things in the first place and not cloud-connected devices - they must be unleashed to show their full potential.

This might sound trivial, but unfortunately these features are widely ignored in the industry - although they would secure the adoption of smart home technology in the long-term. How can the industry possibly be influenced to see that [a bit more communism](https://jenson.org/we-need-more-communism/) will eventually grow the cake for everyone?
