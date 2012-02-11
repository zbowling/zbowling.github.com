---
layout: post
title: XIB/NIBs on iOS
description: Too much trouble to use interface builder
---

I came to this conclusion a while back. There are some fundamental issues with XIB/NIBs on iOS that make them far less useful than on Mac OSX. iOS 5 introduced UIStoryboard, which is a nice addition but most of the problem still exist.

To understand the issue, we need to look back at the history of iOS, Mac OS, and Interface Builder (IB). 

iPhone OS 1.0 - The early days
------------------------------

When the iPhone came out in 2007, we didn't have third party development apps on the iPhone. Apple wrote the apps. They built the toolkits they used on iOS to service their own needs. Everyone added code to UIKit directly to add the basic UI primitives we use in apps today. From what I gather, there wasn't a huge architectural lead behind UIKit to make sure that it was designed entirely with third party developers using it. It was a reusable toolkit, just like Cocoa, but I believe it was originally designed to be used internally only, at least at first, just like (ProKit)[http://www.cocoadev.com/index.pl?ProKit]. 

iPhone OS 2.0 - The SDK.
------------------------

The demand to run third party apps on the iPhone was more than Apple was expecting. With jailbreaking and potential compition on the horizon, it became a primary focus on the iPhone team to support third party developers. In less than a year, we had iPhone OS 2.0 with a fully fledged SDK for third parties to use. 

Apple had to shape up their existing framework, add in sandboxing, and build out a deployment system quickly (the AppStore) to pull if off. A lot of times, Apple has had the tendency of leaving private frameworks private for a least few releases until the interfaces solidify. They didn't really get to do this as much with UIKit. 

Apple went in with a knife and cut out a part of it that we could use. A mixed bag of low level UI components and high level UI components. It was an odd mix. On one side, you would have pickers for date selection that were fantastic and pretty, but then on the other, you given really basic UIButtons that are fairly ugly out of the box and not like any of the glossy buttons found on the platform. They gave you UITableView with grouping, but not the cells that make the pretty table based forms you find in many apps for settings and configuration. 

