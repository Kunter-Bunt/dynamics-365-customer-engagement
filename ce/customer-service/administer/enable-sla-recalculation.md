---
title: Recalculate SLAs in terminal status in Dynamics 365 Customer Service
description: Learn how to configure the recalculation of SLAs that reach the terminal status in Dynamics 365 Customer Service.
ms.date: 10/12/2023
ms.topic: how-to
author: Soumyasd27
ms.author: sdas
ms.reviewer: shujoshi
search.audienceType: 
  - admin
  - customizer
  - enduser
ms.custom: 
  - bap-template
  - dyn365-customerservice
ms.collection: get-started
---

# Recalculate SLAs in terminal status

SLAs in terminal status are recalculated in the following scenarios:

- If the SLA KPI instance is in an expired state and the applicable when or success condition changes, the SLAs are recalculated if the recalculate flag is on.
- SLA KPI instances that are in succeeded or canceled terminal states remain in the same state irrespective of changes to the applicable from or when conditions if the recalculate SLA option is set to no. Changes occur only if the recalculate SLA option is set to yes.
- When a SLA KPI instance is in an expired state and changes are made to its applicable SLA item, the SLAs are recalculated. A new slakpiinstance is created, and its status depends on the failure time. Failure time is calculated from the applicable from field. If the SLA KPI Instance has passed the specified failure time, it creates a new slakpiinstance in an expired state.
- By default, SLAs in the succeeded and noncompliant terminal statuses aren't reevaluated when the success condition changes or can't be paused or resumed. However, you can recalculate such SLAs when the applicable when and success criteria of the target entity changes by enabling the recalculate SLA setting in the **Service Configuration Settings** view.

## Enable recalculation of SLAs on reaching terminal status

You can enable the recalculation of SLAs that reach the terminal status in the Customer Service admin center or Customer Service Hub app.

1. Go to one of the apps and perform the following steps.

   ### [Customer Service admin center](#tab/customerserviceadmincenter)

    1. In the site map, select **Service Terms** in **Operations**.
    1. In the **Other SLA Settings** section, select **Manage**.
        The **Service Configuration Settings** view is displayed.

   ### [Customer Service Hub - Service Management (deprecated)](#tab/customerservicehub)

    [!INCLUDE[csh-deprecation](../../includes/csh-deprecation.md)]

    1. In the site map, Go to **Service Management**.
    1. From the list of entity records, select **Service Configuration Settings** in **Service Terms**.

        The **Service Configuration Settings** view is displayed.

2. In **Recalculate SLA on terminal status**, switch the toggle to **Yes**, and select **Save**.

    :::image type="content" source="../media/sla-recalculate.png" alt-text="Enable recalculate SLA on reaching terminal status.":::



### See also

[Define service-level agreements](define-service-level-agreements.md)  
[Apply SLAs](apply-slas.md#apply-slas) 
[Enable records for SLA](enable-entities-service-level-agreements.md)  
