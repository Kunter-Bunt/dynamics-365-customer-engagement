---
title: Enable enhanced experience for email attachments
description: Enable enhanced email attachment control for agents to have a consistent experience across all forms. 
author: gandhamm
ms.author: mgandham
ms.reviewer: neeranelli
ms.topic: how-to 
ms.collection:
ms.date: 12/08/2023
ms.custom:
  - bap-template
  - ai-gen-docs-bap
  - ai-gen-title
  - ai-seo-date:12/01/2023
  - ai-gen-desc
---

# Enable enhanced experience for email attachments

You can enable the enhanced email attachment control for forms to provide a consistent email attachment experience to agents. Do the following steps:

1. In [Power Apps](https://make.powerapps.com/), select the environment that contains your solution.
1. Select **Tables**> **Email**> **Forms** and then select the required form.
1.  Add **Attachments control** to **Components** in the **Attachment** subgrid properties. For more information: [Add components to a form](/power-apps/maker/model-driven-apps/add-move-configure-or-delete-components-on-form#add-components-for-a-column-on-the-form).
1. Save and publish the form.

## Enable drag and drop for attachments in the rich text editor

You can enable the drag and drop feature for files to be added as attachments for the rich text editor. Do the following steps:

1. In [Power Apps](https://make.powerapps.com/), select the environment that contains your solution.
1. Select **Tables**> **Email**> **Forms** and then select the required form.
1. Edit **Email body** > **Components** > **Rich Text Editor Control**.
1. Edit **Custom Configuration URL** and add the following configuration:
     
     ```
        "base64FileUploader":true,
        "attachmentEntity": {
        "tableName": "activitymimeattachments",
        "contentColumn": "body",
        "fileNameColumn": "filename",
        "mimeTypeColumn": "mimetype",
        "objectTypeCodeColumn": "objecttypecode",
        "relatedEntityName": "emails",
        "relatedFieldName": "objectid_email"
        }    

     ```
1. Save and publish the form.

## Next steps

[Use the enhanced email attachment experience across email forms](../use/enhanced-email-attachment-control.md)
