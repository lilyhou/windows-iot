---
title: SoCs and Custom Boards for Windows 10 IoT Enterprise
author: rsameser
ms.author: riameser
ms.date: 1/8/2021
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about SoCs and Custom Boards requirements for Windows 10 IoT Enterprise.
keywords: IoT Enterprise, Hardware, SoCs, Custom Boards, development devices, boards, SOC, SOM, system on chips, Windows IoT
---
# SoCs and custom boards

## Microsoft-enabled SoCs

Microsoft works alongside Intel, Qualcomm, and AMD to verify support for Windows 10 IoT Enterprise on several vendors' system on a chip (SoCs). These SoCs are used in hundreds of different devices that you can use to prototype and commercialize your idea. The SoC you choose to adopt will depend on considerations such as performance requirements, power profile, cost, physical connectivity options, long term support, and operating conditions.

You'll also need to decide whether you want to use an off-the-shelf board or device, build a custom device using a system on a module (SoM) plus a custom carrier board, or build a complete custom board. Cost and the degree of customization are the key factors in this decision, with both generally increasing as you customize further.

## Boards

If an off-the-shelf device is in a form factor that includes the connectivity options that work for your scenarios, that will often be the most cost- and time-effective choice.  

For most people, developing a complete custom board would make sense when the product is expected to be sold in volumes greater than tens, or even hundreds, of thousands of units. For smaller volumes, using a SoM and designing a custom carrier board, instead of designing a completely new board, can significantly reduce your cost and time-to-market, as well as streamlining software development and integration.

Each of the platforms has unique quirks that need attention during implementation. There are many companies building on Windows 10 IoT Enterprise, here is a list of some that have proven experience working with Windows 10 IoT Enterprise:

* [Intel](https://www.intel.com/content/www/us/en/products/boards-kits.html)
* [Qualcomm](https://www.arrow.com/en/manufacturers/qualcomm/microcontrollers-and-processors/evaluation-development-boards-and-kits/embedded-system-development-boards-and-kits)
* [AMD](https://www.amd.com/en/products/embedded)
* [VIA Technologies](https://www.viatech.com/en/products/boards/embedded-boards/)

*If you are a SoM provider or an ODM and would like to be added to the list below, please send email to [winiotsomhelp@microsoft.com](mailto:winiotsomhelp@microsoft.com) or directly edit this page and submit a pull request.*
