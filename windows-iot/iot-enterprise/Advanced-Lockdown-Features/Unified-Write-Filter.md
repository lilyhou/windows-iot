---
title: Unified Write Filter
author: rsameser
ms.author: riameser
ms.date: 10/30/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Unified Write Filter Features of Windows 10 IoT Enterprise.
keywords: Lockdown, Unified Write Filter
---

# Unified Write Filter
The [Unified Write Filter (UWF)](https://docs.microsoft.com/windows-hardware/customize/enterprise/unified-write-filter#turn-on-and-configure-uwf) is a Windows 10 IoT Enterprise feature that helps to protect your drives by intercepting and redirecting any writes to the drive (app installations, settings changes, saved data) to a virtual overlay. The virtual overlay is a temporary location that is usually cleared during a reboot or when a guest user logs off. This is a great feature because it provides a clean experience for thin clients and workspaces that have frequent guests, like school, library or hotel computers. This way, guests can work, change settings, and install software, and after the device reboots, the next guest receives a clean experience. This also increases reliability for kiosks, IoT-embedded devices, or other devices where new apps are not expected to be frequently added. Learn how to [enable the unified write filter](https://docs.microsoft.com/windows-hardware/customize/enterprise/uwf-turnonuwf) to enhance your kiosk experience.  
