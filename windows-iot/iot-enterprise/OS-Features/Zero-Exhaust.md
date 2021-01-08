---
title: Zero Exhaust
author: rsameser
ms.author: riameser
ms.date: 1/8/2021
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the zero exhaust features of Windows 10 IoT Enterprise.
keywords: IoT Enterprise, zero exhaust
---

# Zero Exhaust
Zero exhaust is defined as no network traffic (diagnostic data or otherwise, such as downloading background images, Windows Updates, etc.) from Windows and inbox applications to public IP addresses unless directly intended by the user. This allows the enterprise admin to configure devices where no network communication is initiated by the system without explicit approval.

The article [Manage connections from Windows 10 operating system components to Microsot services](https://docs.microsoft.com/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services) list the components that make network connections to Microsoft services by default and shows you how to configure these settings to control the data that is sent to Microsoft. To prevent Windows from sending any data to Microsoft, configure diagnostic data at the Security level, turn off Windows Defender diagnostic data and MSRT reporting, and turn off all of these connections.

* [Manage Settings for Windows 10 IoT Enterprise](https://docs.microsoft.com/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#settings-for-windows-10-enterprise-edition)

## Additional Resources
* [TPMPolicy CSP](https://docs.microsoft.com/windows/client-management/mdm/tpmpolicy-csp#:~:text=Zero%20exhaust%20is%20defined%20as%20no%20network%20traffic,IP%20addresses%20unless%20directly%20intended%20by%20the%20user.)
