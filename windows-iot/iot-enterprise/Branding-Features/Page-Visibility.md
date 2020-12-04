---
title: Settings Page Visibility
author: rsameser
ms.author: riameser
ms.date: 12/04/2020
ms.topic: article
ms.prod: windows-iot
ms.technology: iot
description: Learn about the Page Visibility Features of Windows 10 IoT Enterprise.
keywords: Branding, Settings Page Visibility
---

# Settings Page Policy: Page Visibility
In Windows 10 IoT there are many [settings policies](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings) that can be set. One settings policy that is quite useful is configuring [page visibility](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-pagevisibilitylist). This feature allows you to prevent specific pages in the System Settings app from being visible or accessible, or to do so for all pages except those specified.

## Configure the Page Visibility Policy
The [Policy configuration service provider (CSP)](https://docs.microsoft.com/windows/client-management/mdm/policy-configuration-service-provider) enables the enterprise to configure policies on Windows 10. Use this configuration service provider to configure any company policies.

Added in Windows 10, version 1703, this mode will be specified by the policy string beginning with either the string "showonly:" or "hide:".  Pages are identified by a shortened version of their already published URIs, which is the URI minus the "ms-settings:" prefix. For example, if the URI for a settings page is "ms-settings:bluetooth", the page identifier used in the policy will be just "bluetooth". Multiple page identifiers are separated by semicolons.

### Example 1: Access only to the about and bluetooth pages

The following example illustrates a policy that would allow access only to the about and bluetooth pages, which have URI "ms-settings:about" and "ms-settings:bluetooth" respectively:

showonly:about;bluetooth

If the policy is not specified, the behavior will be that no pages are affected. If the policy string is formatted incorrectly, it will be ignored entirely (i.e. treated as not set) to prevent the machine from becoming unserviceable if data corruption occurs. Note that if a page is already hidden for another reason, then it will remain hidden even if it is in a "showonly:" list.

The format of the PageVisibilityList value is as follows:

* The value is a unicode string up to 10,000 characters long, which will be used without case sensitivity.
* There are two variants: one that shows only the given pages and one which hides the given pages.
* The first variant starts with the string "showonly:" and the second with the string "hide:".
* Following the variant identifier is a semicolon-delimited list of page identifiers, which must not have any extra whitespace.
* Each page identifier is the ms-settings:xyz URI for the page, minus the ms-settings: prefix, so the identifier for the page with URI "ms-settings:network-wifi" would be just "network-wifi".

The default value for this setting is an empty string, which is interpreted as show everything.

Example 1, specifies that only the wifi and bluetooth pages should be shown (they have URIs ms-settings:network-wifi and ms-settings:bluetooth). All other pages (and the categories they're in) will be hidden:

showonly:network-wifi;bluetooth

### Example 2: Wifi page should not be shown

The following example illustrates a policy that spcifies that the wifi page should now be show:

hide:network-wifi

ADMX Info:
* GP English name: Settings Page Visibility
* GP name: SettingsPageVisibility
* GP path: Control Panel
* GP ADMX file name: ControlPanel.admx

To validate on Desktop, do the following:
1. Open System Settings and verify that the About page is visible and accessible.
2. Configure the policy with the following string: "hide:about".
3. Open System Settings again and verify that the About page is no longer accessible.

## Additional Resources
* [Page Visibility List](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings#settings-pagevisibilitylist)
* [Policy CSP - Settings](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-settings)
* [Policy CSP](https://docs.microsoft.com/windows/client-management/mdm/policy-configuration-service-provider)
