---
title: Windows Updates
author: rsameser
ms.author: riameser
ms.date: 12/04/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Update Notification Feature in Windows 10 IoT Enterprise.
keywords: Branding, Update Notification
---
# Windows Updates
In Windows 10 IoT Enterprise, we know that having your device ready for use at all time is very important. We have many features to help you maximize control over your devices' [update notifications](https://docs.microsoft.com/windows/deployment/update/waas-wu-settings#remove-access-to-use-all-windows-update-features) to ensure that you can plan and ahead and control when updates can occur. Below are some common recommended configuration settings that our IoT device partners tend to use. Consider whether each individual configuration setting applies to your device scenario.

## Control Windows Updates
One of the most common requests from device partners is centered around controlling automatic updates on Windows 10 IoT devices. The nature of IoT devices is such that unexpected disruptions, through something like an unplanned update, can create a bad device experience.

Questions that you should ask when considering how to control Windows updates:
* Is the device scenario such that any disruption of the workflow is unacceptable?
* How are updates validated prior to deployment?
* What is the update user experience on the device itself?

If you have a device where disruption of the user experience isn't acceptable, you should consider limiting updates to only certain hours, disabling automatic updates, or deploying updates either manually or through a controlled 3rd party solution.

## Limit reboots from updates
You can use the Active Hours Group Policy, MDM, or registry setting to limit updates to only certain hours.

1. Open the Group Policy Editor (gpedit.msc) and navigate to **Computer Configuration\Administrative Templates\Windows Components\Windows Update** and open the **Turn off auto-restart for updates during active hours** policy setting. **Enable** the policy so you can set the start and end times for active hours.
2. Set the **Start** and **End** time to the Active Hours window. For example, set Active Hours to start at 4:00AM and end 2:00AM. This allows the system to reboot from updates between the hours of 2:00 AM and 4:00 AM.

## Control UI notifications from the Windows Update client
A device can be configured in a way to hide the UI experience for Windows Update while letting the service itself run in the background and update the system. The Windows Update client still honors the policies set for configuring Automatic Updates, this policy controls the UI portion of that experience.

1. Open the Group Policy Editor (gpedit.msc) and navigate to **Computer Configuration\Administrative Templates\Windows Components\Windows Update\Display options for update notifications**
2. Set the policy to enabled.
3. Set Specify the update notifications display options to 1 or 2.

> [!TIP]
>
> Set the value to 1 to hide all notifications except restart warnings, or to 2 to hide all notifications, including restart warnings.

## Completely disable automatic Windows Updates
Security and stability are at the core of a successful IoT project, and Windows Update provides updates to ensure Windows 10 IoT Enterprise has the latest applicable security and stability updates. You might, however, have a device scenario where updating Windows has to be handled completely manually. For this type of scenario, we recommend disabling automatic updating through Windows Update. In previous versions of Windows device partners could stop and disable the Windows Update service, but this is no longer the supported method for disabling automatic updates. Windows 10 has a number of policies that allow you to configure Windows Updates in several ways.

To completely disable automatic updating of Windows 10 with Windows Update:
1. Open the Group Policy Editor (gpedit.msc) and navigate to **Computer Configuration\Administrative Templates\Windows Components\Windows update\Configure Automatic Updates**.
2. Explicitly set the policy to **Disabled**. When this setting is set to Disabled, any available updates from Windows Update must be downloaded and installed manually, which you can do in the Settings app under **Update & security > Windows Update**.

## Disable access to the Windows Update user experience
In some scenarios, configuring Automatic Updates isn't enough to preserve a desired device experience. For example, an end user may still have access to the Windows Update settings, which would allow manual updates via Windows Update. You can configure Group policy to prohibit access to Windows Update through settings.

To prohibit access to Windows update:
1. Open the Group Policy Editor (gpedit.msc) and navigate to **Computer Configuration\Administrative Templates\Windows Components\Windows update\Remove access to use all Windows update features**.
2. Set this policy to **Enabled** to prevent the "Check for updates" option for users. Note: Any background update scans, downloads, and installations will continue to work as configured. This policy simply prevents the user from accessing the manual check through settings. Use the steps in the previous section to also disable scans, downloads and installations.

> [!IMPORTANT]
>
> Be sure to have a well-designed servicing strategy for your device. Disabling Windows Update capabilities leaves the device in a vulnerable state if your device isn't getting updates in another way.

## Prevent drivers from being installed via Windows Update
Sometimes drivers installed from Windows Update can cause issues with a device experience. The steps below prohibit Windows Update from downloading and installing new drivers on the device.

1. Open the Group Policy Editor (gpedit.msc) and navigate to **Computer Configuration\Administrative Templates\Windows Components\Windows update\Do not include drivers with Windows Updates**.
2. Enable this policy, which tells Windows to not include drivers with Windows quality updates.

## Windows Update Summary
You can configure Windows Update in several ways, and not all policies are applicable to all devices. As a general rule, IoT devices require special attention to the servicing and management strategy to be used on the devices. If your servicing strategy is to disable all Windows Update features through policy, the steps below provide a combined list of policies to configure.

1. **Open** the Group Policy Editor (gpedit.msc) and navigate to **Computer Configuration** -> **Administrative Templates** -> **System** -> **Device Installation** and set the following policies:

    * **Specify the search server for device driver updates** to **Enabled**, with **Select update server** set to **Search Managed Server**
    * **Specify search order for device driver source locations** to **Enabled**, with **Select search order** set to **Do not search Windows Update**


2. In the Group Policy Editor, navigate to **Computer Configuration** -> **Administrative Templates** -> **Windows Components** -> **Windows Update** and set the following policies: 

    * **Configure Automatic Updates** to **Disabled**
    * **Do not include drivers with Windows Updates** to **Enabled**


3. In the Group Policy Editor, navigate to **Computer Configuration** -> **Administrative Templates** -> **System** -> **Internet Communication Management** -> **Internet Communication settings** and set **Turn off access to all Windows Update features** to **Enabled**


4. In the Group Policy Editor, navigate to **Computer Configuration** -> **Administrative Templates** -> **Windows Components** -> **Windows Update** -> **Display options for update notifications** and set the policy to **Enabled** with **Specify the update notifications display options** to **2**

## Additional Resources
* [Manage device restarts after updates](https://docs.microsoft.com/windows/deployment/update/waas-restart)
* [Manage additional Windows Update settings](https://docs.microsoft.com/windows/deployment/update/waas-wu-settings)
* [Deploy feature updates during maintenance windows](https://docs.microsoft.com/windows/deployment/update/feature-update-maintenance-window)
* [Deploy feature updates for user-initiated installations](https://docs.microsoft.com/windows/deployment/update/feature-update-user-install)
