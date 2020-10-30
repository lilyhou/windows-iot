---
title: Windows Defender Application Control (WDAC) and AppLocker
author: rsameser
ms.author: riameser
ms.date: 10/30/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about Windows Defender Application Control (WDAC) and AppLocker Features in Windows 10 IoT Enterprise.
keywords: Lockdown, AppLocker, Windows Defender
---

# Windows Defender Application Control (WDAC) and AppLocker
Windows 10 includes two technologies that can be used for application control depending on your organization's specific scenarios and requirements: [Windows Defender Application Control (WDAC) and AppLocker](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-control/wdac-and-applocker-overview).

WDAC was introduced with Windows 10 and allows organizations to control which drivers and applications are allowed to run on their Windows 10 clients. WDAC was designed as a security feature under the [servicing criteria](https://www.microsoft.com/msrc/windows-security-servicing-criteria?rtc=1) defined by the Microsoft Security Response Center (MSRC). To learn more about if WDAC can work for your organization, check out the following [documentation](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control-deployment-guide).

AppLocker advances the app control features and functionality of Software Restriction Policies. AppLocker contains new capabilities and extensions that allow you to create rules to allow or deny apps from running based on unique identities of files and to specify which users or groups can run those apps. Since AppLocker rules specify which apps are allowed to run on the device, you can leverage AppLocker to create a [Windows 10 kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-applocker) that runs multiple apps. AppLocker is ideal for organizations that currently use Group Policy to manage their PCs. To learn more about if AppLocker can work for your organization, check out the following [documentation](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-control/applocker/applocker-overview).

Note, when it comes to choosing between WDAC or AppLocker it is generally recommended that customers who are able to implement application control using WDAC rather than AppLocker, do so. WDAC is undergoing continual improvements and will be getting added support from Microsoft management platforms. Although AppLocker will continue to receive security fixes, it will not undergo new feature improvements.
AppLocker advances the app control features and functionality of Software Restriction Policies. AppLocker contains new capabilities and extensions that allow you to create rules to allow or deny apps from running based on unique identities of files and to specify which users or groups can run those apps. AppLocker is ideal for organizations that currently use Group Policy to manage their PCs. To learn more about if AppLocker can work for your organization, check out the following [documentation](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-control/applocker/applocker-overview).
