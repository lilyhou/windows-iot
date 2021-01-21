---
title: OEMS & Licensing
author: rsameser
ms.author: riameser
ms.date: 1/21/2021
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Read about licensing for Windows 10 IoT Enterprise.
keywords: IoT Enterprise, OEM, Licensing, LTSC, SAC
---
# Licensing
In order to start your journey with Windows 10 IoT Enterprise, you'll need to get a license. You can retrieve a license by contacting a [Windows IoT Distributor](https://aka.ms/IoTDistributorList) or leverage the [Windows 10 IoT Enterprise 90 day Evaluation](https://www.microsoft.com/evalcenter/evaluate-windows-10-enterprise).

> [!TIP]
> There are currently **two** release channels for Windows 10:
> * The Semi-Annual Channel receives feature updates twice per year.
> * The Long Term Servicing Channel, which is designed to be used only for specialized devices (which typically don't run Office) such as those that control medical equipment or ATM machines, receives new feature releases every two to three years.

## Semi-Annual Channel (SAC)
In the Semi-Annual servicing channel, feature updates are available as soon as Microsoft releases them. This servicing model is ideal for pilot deployments and testing of Windows 10 feature updates and for users such as developers who need to work with the latest features immediately. Once the latest release has gone through pilot deployment and testing, you will be able to choose the timing at which it goes into broad deployment.

Please review [Semi-Annual Servicing Channel](https://docs.microsoft.com/en-us/windows/deployment/update/waas-overview#semi-annual-channel) for more information.

## Long-term Servicing Channel (LTSC)
Specialized systems such as devices that control medical equipment, point-of-sale systems, and ATMs—often require a longer servicing option because of their purpose. These devices typically perform a single important task and don’t need feature updates as frequently as other devices in the organization. It’s more important that these devices be kept as stable and secure as possible than up to date with user interface changes. For these fixed-purpose devices, we recommend the long-term servicing channel.

Please review [Long-term Servicing Channel](https://docs.microsoft.com/en-us/windows/deployment/update/waas-overview#long-term-servicing-channel) for more information.

### Fixed purpose devices
Windows is well known as the operating system for laptops and desktops that have been used by consumers and businesses worldwide for decades.  Windows also powers many ATM machines, point-of-sale terminals, industrial automation systems, thin clients, medical devices, digital signage, kiosks, and other fixed purpose devices.  Windows 10 IoT Enterprise allows you to build these fixed purpose devices with specific allowances and restrictions in the license agreement.  

A fixed purpose device differs from a general-purpose device in the following ways:  
* The device is locked down to a single application or fixed set of applications through the Assigned Access or Shell Launcher features.  
* The device experience is often immediate when the customer powers-on. This is achieved by configuring the device image to skip the normal Windows out-of-box experiences.
* Keyboards, USB ports, and device policies can be locked down to constrain the device to be used only in its fixed purpose.  
* The IoT Device OEM licenses the device to the user with the software attached to the device as a complete product and passes through specific Windows terms in their own IoT OEM agreements.
* The OEM provides the customer support for their complete product, including the functions performed by the operating system.

> [!NOTE]
> See your licensing agreement for complete guidance on all Windows 10 IoT Enterprise usage scenarios. If you are an end-user customer, your OEM should have provided you with the terms in an agreement. If you are an OEM, you can direct questions to your distributor regarding your specific licensing agreement.  

## Distributors
Microsoft offers more than 500 Windows IoT and Embedded SKUs. Authorized distributors of Windows IoT products can help you pick the right SKU for your hardware and your budget by leveraging their development experiences, and knowledge, to help you build secure and connected Windows IoT solutions. If you would like to work with one of our distributors, please [select a distributor](https://aka.ms/IoTDistributorList) in your region and contact the distributor directly for more details.

## Additional Resources
* [Windows 10 IoT Enterprise Manufacturing Guide](https://docs.microsoft.com/windows-hardware/manufacture/desktop/iot-ent-overview)
* [Windows 10 Servicing](https://docs.microsoft.com/windows/deployment/update/waas-overview#servicing)
* [Servicing Channels](https://docs.microsoft.com/windows/deployment/update/waas-overview#servicing-channels)
