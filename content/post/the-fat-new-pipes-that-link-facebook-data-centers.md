+++
date = "2017-05-07"
draft = false
title = "The Fat New Pipes that Link Facebook Data Centers"
+++

Earlier this week Facebook announced that over some recent period of time traffic between its data centers has been carried by a separate network backbone than the backbone that connects its data centers to the public internet – a major architectural change for the social network which for 10 years had been moving both types of traffic on a single backbone.

The amount of traffic traveling between Facebook data centers today is many times bigger than the amount of traffic that travels between its infrastructure and the internet, where its 2 billion monthly active users access the social network. And while Facebook’s traffic to the internet has grown slowly in recent years, the amount of bandwidth required for replicating rich content like photos and videos across multiple data centers has skyrocketed, forcing the company’s engineers to rethink the way its global network is designed.

Along with implementing a whole new global backbone, dubbed Express Backbone, or EBB, Facebook’s infrastructure team also designed a new control stack for managing traffic flows on it, taking lots of cues from the way network fabric inside its data centers is designed.

Facebook is not unique in having separate backbones for internal and external traffic. Google has B2, an internet-facing backbone, and B4, an inter-data center backbone. But Google is just one example, albeit a massive-scale one.

“All of the hyper-scalers and many financial services companies have private fiber networks that traverse long distances between [data centers] but are not (directly) connected to the public internet,” Kyle Forster, founder of the software-defined networking startup Big Switch Networks, said via email. Internal traffic often runs on a company’s own fiber, which for a hyper-scale platform can be cheaper than using service providers, he added.

Web-oriented companies often use this type of network design to isolate “dirty” network activity from “clean network” activity, explained JR Rivers, co-founder and CTO of Cumulus Networks, which sells a Linux-based operating system for data center networks. In the mid-2000s, Rivers worked at Google, where he was involved in designing the company’s home-grown data center network.

Having separate backbones for internal and external traffic helps companies “provide quality of service, denial-of-service and intrusion protection, and network address isolation,” Rivers wrote in an email. “Some even use optimized network protocols on their ‘inside’ networks, which is enabled by this physical isolation.”

The innovative part of Facebook’s announcement is the control stack its engineers built to manage EBB. According to a company blog post, it includes:

Centralized (and highly redundant) ensemble of BGP-based route injectors to move traffic on/off the network
sFlow collector, based on collecting sFlow samples from the network devices, used to feed in active demands into the traffic engineering controller
Traffic engineering controller, which computes and programs optimum routes based on the current demand set
Open/R agents running on network devices to provide IGP and messaging functionality
LSP agents, also running on network devices to interface with the device forwarding tables on behalf of the central controller
See a detailed technical description of the control stack here.

Building such a system requires advanced technical skills and significant investment in innovation, Ihab Tarazi, CTO of Equinix, commented via email. “This architecture includes the development of automated network routing, management, and operations tools that are very sophisticated. It also leverages open source hardware design. More importantly, this is a whole new culture and agile DevOps model that is unique to Facebook.”

While particularly well-suited for hyper-scale platforms, they’re not the only type of companies using the approach. Cumulus works with numerous customers of different scale who have similar architectures, according to Rivers. “Some with smaller scale will use virtual networks to provide this isolation, and others will have separate physical networks,” he said.

In the enterprise space, however, the architecture is becoming less common, said Big Switch’s Forster: “While numerous large enterprises used to have these private backbones, it went out of fashion over the last ten years, as prices from major telcos have come down, and the numbers are dwindling.”

Source: <a href=http://www.datacenterknowledge.com/archives/2017/05/04/the-fat-new-pipes-that-link-facebook-data-centers/>Datacenter Knowledge</a>
