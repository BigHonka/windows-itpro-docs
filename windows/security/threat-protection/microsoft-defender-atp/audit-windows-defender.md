---
title: Test how Microsoft Defender ATP features work in audit mode
description: Audit mode lets you use the event log to see how Microsoft Defender ATP would protect your devices if it was enabled.
keywords: exploit guard, audit, auditing, mode, enabled, disabled, test, demo, evaluate, lab
search.product: eADQiWindows 10XVcnh
ms.prod: w10
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
ms.localizationpriority: medium
audience: ITPro
author: levinec
ms.author: ellevin
ms.reviewer: 
manager: dansimp
---

# Test how Microsoft Defender ATP features work in audit mode

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


**Applies to:**

* [Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP)](https://go.microsoft.com/fwlink/p/?linkid=2069559)

You can enable attack surface reduction rules, exploit protection, network protection, and controlled folder access in audit mode. Audit mode lets you see a record of what *would* have happened if you had enabled the feature.

You may want to enable audit mode when testing how the features will work in your organization. Ensure it doesn't affect your line-of-business apps, and get an idea of how many suspicious file modification attempts generally occur over a certain period of time.

The features won't block or prevent apps, scripts, or files from being modified. However, the Windows Event Log will record events as if the features were fully enabled. With audit mode, you can review the event log to see what impact the feature would have had if it was enabled.

To find the audited entries, go to **Applications and Services** > **Microsoft** > **Windows** > **Windows Defender** > **Operational**.

You can use Microsoft Defender Advanced Threat Protection to get greater details for each event, especially for investigating attack surface reduction rules. Using the Microsoft Defender ATP console lets you [investigate issues as part of the alert timeline and investigation scenarios](../microsoft-defender-atp/investigate-alerts.md).

This article provides links that describe how to enable the audit functionality for each feature and how to view events in the Windows Event Viewer.

You can use Group Policy, PowerShell, and configuration service providers (CSPs) to enable audit mode.

>[!TIP]
>You can also visit the Windows Defender Testground website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to confirm the features are working and see how they work.

 Audit options | How to enable audit mode | How to view events
-|-|-
Audit applies to all events | [Enable controlled folder access](enable-controlled-folders.md) | [Controlled folder access events](evaluate-controlled-folder-access.md#review-controlled-folder-access-events-in-windows-event-viewer)
Audit applies to individual rules | [Enable attack surface reduction rules](enable-attack-surface-reduction.md) | [Attack surface reduction rule events](evaluate-attack-surface-reduction.md#review-attack-surface-reduction-events-in-windows-event-viewer)
Audit applies to all events | [Enable network protection](enable-network-protection.md) | [Network protection events](evaluate-network-protection.md#review-network-protection-events-in-windows-event-viewer)
|Audit applies to individual mitigations | [Enable exploit protection](enable-exploit-protection.md) | [Exploit protection events](exploit-protection.md#review-exploit-protection-events-in-windows-event-viewer)

## Related topics

* [Protect devices from exploits](exploit-protection.md)
* [Reduce attack surfaces with attack surface reduction rules](attack-surface-reduction.md)
* [Protect your network](network-protection.md)
* [Protect important folders](controlled-folders.md)
