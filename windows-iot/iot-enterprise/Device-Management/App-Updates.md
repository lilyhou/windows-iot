---
title: Application Updates
author: rsameser
ms.author: riameser
ms.date: 12/11/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about how apps can be updated in Windows 10 IoT Enterprise.
keywords: Branding, Microsoft Store Access
---

# Application Updates
OEMs and enterprise customers can deliver app updates to Windows 10 IoT Enterprise devices in the following ways:
* **Using Microsoft Store**: The app is published and updated from the Microsoft Store
* **Using Device Update Center**: The app is published to Windows Update and updated like any other OEM package (driver package)
* **Using Azure IoT Device Management**: The app is published to Azure Storage and updated through the Azure DM channel New for Windows 10, version 1709
* **Using OMA-DM**: The app is updated using an OMA-DM compliant device management channel such as Intune or Endpoint Manager.

The first version of the app is always pre-packaged in the device during image time. The [ApplicationManagement/AllowAllTrustedApps](https://docs.microsoft.com/windows/client-management/mdm/policy-configuration-service-provider#applicationmanagement-allowalltrustedapps) setting should be set for enabling installation of trusted apps.

## Using the Microsoft Store
The Microsoft Store provides unique and secure means to update the IoT Enterprise apps, independent of the OS/OEM Component updates. This option is interesting for OEMs who have:

* **High update frequency**: App update frequency higher than the driver updates and App updates are independent of drivers.
* **Third-party ISV developers**: Third-party ISV developed app, managed with a different release schedule.

In this option, the apps that is pre-packaged needs to be Microsoft Store compliant apps (store signed).

### Managing Store app updates
The following settings on the device side control the updates from Windows Store.

* [ApplicationManagement/AllowStore](https://docs.microsoft.com/windows/client-management/mdm/policy-configuration-service-provider#applicationmanagement-allowstore): Enable/disable store.
* [ApplicationManagement/AllowAppStoreAutoUpdate](https://docs.microsoft.com/windows/client-management/mdm/policy-configuration-service-provider#applicationmanagement-allowappstoreautoupdate): Enable auto update of all store apps.

#### Self updates
The Apps can be designed to control the updates by itself (either automatically or with user interaction with the appx). Windows makes available APIs that give a developer the ability to query available updates, download available updates and install available updates.

See [Download and install package updates for your app](https://docs.microsoft.com/windows/uwp/packaging/self-install-package-updates) for more information on building this capability. In this case, the AllowAppStoreAutoUpdate should be disabled.

## Using Device Update Center
[Device Update Center](https://docs.microsoft.com/windows-hardware/service/iot/using-device-update-center) is a channel to update OEM custom packages that includes apps, drivers and various other files. In this path, the application is packaged in a provisioning package and delivered to the device. On the device boot, this provisioning package is processed and the contained app is installed/updated. See instructions for Adding an app to your image.

This option is interesting for OEMs who have:

* **Dependency with drivers**: App updates are dependent on drivers and are updated at the same frequency of drivers.
* **Dependency with other apps**: More than one apps present on the device and should be updated together at all times.

In this option, the apps that is pre-packaged need not be Microsoft Store compliant apps (store signed). You may still want to Store sign the apps that enables you an option to update the apps using the Microsoft Store in the future.

## Using Azure IoT Device Management
[Azure IoT Device Management (AzureDM)](https://docs.microsoft.com/windows/iot-core/manage-your-device/azureiotdm) is a highly scalable management solution available on Windows 10 IoT Enterprise. See [Application Management](https://github.com/ms-iot/iot-core-azure-dm-client/blob/master/docs/application-management.md) for the details of installing and updating applications via AzureDM.

## Using OMA-DM
The OMA-DM interface is supported in Windows 10 IoT Enterprise and any OMA-DM compliant management solution can be used to install and update applications. Read the documentation for [EnterpriseModernAppManagement CSP](https://docs.microsoft.com/windows/client-management/mdm/enterprisemodernappmanagement-csp) for usage instructions.

## Comparisons of various options
| Item | Using Microsoft Store | Using Device Update Center | Using AzureDM | Using OMA-DM |
|------|-----------------------|----------------------------|---------------|--------------|
| Appx Signing | Store Signed | Store signed or OEM Signed | Store signed or OEM Signed | Store signed or OEM Signed |
| Distribution/Visibility | Store private (not available in store catalog) | Private | Private | Private |
| Infrastructure | Microsoft Store | Windows Update | Azure IoT / Storage | OEM Infrastructure