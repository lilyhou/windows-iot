---
title: Getting Started with Windows 10 IoT Enterprise
author: rsameser
ms.author: riameser
ms.date: 1/17/2021
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about what Windows 10 IoT Enterprise is and what you can do with it.
keywords: IoT Enterprise, binary, fixed purpose devices, LTSC, Silicon
---

# Getting Started with Windows 10 IoT Enterprise
This documentation set will cover the technical breakdown of what's included when you choose to use Windows 10 IoT Enterprise. This article will give you an overview of the product and guide you through how to get started with Windows 10 IoT Enterprise.

## What is Windows 10 IoT Enterprise?
Windows 10 IoT Enterprise is a full version of Windows 10 that delivers enterprise manageability and security to IoT solutions. Windows 10 IoT Enterprise shares all the benefits of the world-wide Windows ecosystem. It is a binary equivalent to Windows 10 Enterprise, so you can use the same familiar development and management tools as client PCs and laptops. However, when it comes to licensing and distribution, the desktop version and IoT versions differ.

With the 1903 release, we have created a new edition for Windows 10 IoT Enterprise. In the future, it can unlock IoT scenarios with a tailored feature set. As of the 1903 & 1909 releases, the sole difference between the Desktop and IoT versions is that reserved storage for updates and temporary files isn’t set aside during installation; this allows for the use of smaller storage devices with an identical feature set. Also, with the new keys, the edition will now show up as Windows 10 IoT Enterprise​.

Please note that Windows 10 IoT Enterprise offers both [Long-term Servicing Channel (LTSC)](https://docs.microsoft.com/windows/deployment/update/waas-overview#servicing-channels) and [Semi-Annual Channel (SAC)](https://docs.microsoft.com/windows/deployment/update/waas-overview#servicing-channels) options. OEMs can choose the version they require for their devices.

## Fixed purpose devices

> [!TIP]
> See your licensing agreement for complete guidance on all Windows 10 IoT Enterprise usage scenarios. If you are an end-user customer, your OEM should have provided you with the terms in an agreement. If you are an OEM, you can direct questions to your distributor regarding your specific licensing agreement.  

If you do not have this licensing agreement, ask the OEM you work with for the commercial agreement.

Windows is well known as the operating system for laptops and desktops that have been used by consumers and businesses worldwide for decades.  Windows also powers many ATM machines, point-of-sale terminals, industrial automation systems, thin clients, medical devices, digital signage, kiosks, and other fixed purpose devices.  Windows 10 IoT Enterprise allows you to build these fixed purpose devices with specific allowances and restrictions in the license agreement.  

A fixed purpose device differs from a general-purpose device in the following ways:  
* The device is locked down to a single application or fixed set of applications through the Assigned Access or Shell Launcher features.  
* The device experience is often immediate when the customer powers-on. This is achieved by configuring the device image to skip the normal Windows out-of-box experiences.
* Keyboards, USB ports, and device policies can be locked down to constrain the device to be used only in its fixed purpose.  
* The IoT Device OEM licenses the device to the user with the software attached to the device as a complete product and passes through specific Windows terms in their own IoT OEM agreements.
* The OEM provides the customer support for their complete product, including the functions performed by the operating system.
