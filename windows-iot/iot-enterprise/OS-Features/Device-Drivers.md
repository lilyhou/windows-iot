---
title: Device Drivers
author: rsameser
ms.author: riameser
ms.date: 10/28/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about what Technical Components of Windows 10 IoT Enterprise.
keywords: IoT Enterprise, Device Drivers
---

# Device Drivers
Device Drivers are essential for any IoT device. This section outlines how to write device drivers, how to driver signing works in Windows 10 IoT Enterprise (this is different than traditional client signing), and how to add device drivers to images.  

## How to Write Device Drivers
Windows contains [built-in drivers](https://docs.microsoft.com/windows-hardware/drivers/gettingstarted/do-you-need-to-write-a-driver-) for many device types. If there is a built-in driver for your device type, you won't need to write your own driver. Your device can use the built-in driver. However if you need to write a device driver for your device, please leverage the [Windows Driver Kit (WDK)](https://docs.microsoft.com/windows-hardware/drivers/ddi/).  

## Device Signing
In Windows 10 IoT Enterprise, the device signing process is different than the [traditional client signing](https://docs.microsoft.com/windows-hardware/drivers/install/driver-signing ) process.  
[Insert the steps, and explain the difference for IoT Enterprise requirements here]

## How to Add Device Drivers to Images
With Windows 10 IoT Enterprise, you can add device drivers to a Windows image before, during, or after you deploy the image. When planning how to add drivers to your Windows deployment, it's important to understand how driver folders are added to the image, how driver ranking affects deployment, and the digital signature requirements for drivers. To understand more about how to add drivers, check out the following article, [Device Drivers](https://docs.microsoft.com/windows-hardware/manufacture/desktop/device-drivers-and-deployment-overview).
