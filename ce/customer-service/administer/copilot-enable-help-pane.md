---
title: Enable features in Copilot pane
description: Learn how to enable features that appear in the Copilot help pane to increase agent productivity in Customer Service workspace.
author: gandhamm
ms.author: mgandham
ms.reviewer: neeranelli
ms.topic: how-to 
ms.collection: 
ms.date: 02/19/2024
ms.custom: bap-template 
---

# Enable features in Copilot pane

The Copilot help pane allows agents to use Copilot features such as respond to questions, compose an email, and draft a chat response in Customer Service workspace.

> [!NOTE]
> Respond to questions and compose an email features are generally available in the North America region only. These features are in preview in the rest of the supported regions.

## Prerequisites

- See [Prerequisites](configure-copilot-features.md#prerequisites) for the list of prerequisites to enable and use the features in the Copilot pane.
- You must have the [Knowledge management](set-up-knowledge-management-embedded-knowledge-search.md#setup-overview) configured in your environment for write an email and ask a question features. 
- Your knowledge article parameters are as follows:
   - Updated with the latest version
   - The state is set to Published

> [!NOTE]
> Copilot uses the content attribute only in knowledge article table to generate responses for ask a question, write an email, and draft a chat features. You can't customize this behavior.

- If you aren't in the North America region and you want to use the web search powered by Bing feature, you must enable data movement across regions and Bing search in Power Platform admin center. See [Enable data movement across regions](/power-platform/admin/geographical-availability-copilot).

   :::image type="content" source="../media/ppac-gen-ai-features.png" alt-text="Power Platform Admin center bing chat.":::

## Enable Copilot assist features

Perform the following steps to enable the Copilot features in Customer Service admin center:

1. Use one of the following navigation options:
      - **Agent Experience** > **Productivity** > **Copilot help pane**
      - **Operations** > **Insights** > **Copilot help pane**
1. Select **Manage** in **Copilot help pane**. The **Copilot help pane** page appears. You can select the Copilot features you'd like to enable for agents on this page.

     :::image type="content" source="../media/copilot-admin-email-mini.png" alt-text="Screenshot of ask a question in Copilot pane." lightbox="../media/copilot-admin-email.png":::


## Enable ask a question

Select **Make Copilot available to agents** in the **Copilot help pane** page of Customer Service admin center. The **Ask a question** tab on the **Copilot help pane** appears when agents sign in to Customer Service workspace. Agents can ask questions conversationally, and Copilot answers the questions based on the internal knowledge base sources.

## Enable draft a response (Preview)

[!INCLUDE [preview-banner](../../../shared-content/shared/preview-includes/preview-note.md)]

Select **For customer chat** in the **Copilot help pane** page of Customer Service admin center. The one-click response generation button appears on both the conversation panel for a conversation and on the **Ask a question** tab on the Copilot help pane in Customer Service workspace. Copilot retrieves the context and drafts the response based on the knowledge resources configured for your organization.

## Enable write an email 

Select **For email** in the **Copilot help pane** page of Customer Service admin center. The **Write an email** tab appears on **Copilot help pane** in Customer Service. Copilot helps agents create email responses based on the context of the case.

## Add trusted webpages as sources

You can select **Add web address** in **Web resources** to add trusted domains. You can add up to five trusted web domains for Copilot to search and generate responses from. Copilot searches for information up to two levels down from the configured domain. You must enable the Bing Search in Power Platform admin center to add trusted web sources. See [Enable data across geographic locations](/microsoft-copilot-studio/manage-data-movement-outside-us#enable-data-across-geographic-locations).

Copilot uses articles that are two nodes down the configured domain.

> [!NOTE]
> - The knowledge base content is refreshed every day.
> - Web domains are used by Copilot to only draft emails and chat replies.

## Set up filters

Filters enable Copilot to generate responses based on a specific set of topics. You can set up filters for ask a question and draft a response features by sending an email a request to d365_csaipreview@microsoft.com. See: [Apply filters](../use/use-copilot-features.md#apply-filters).

### Features supported with different knowledge sources

The following table summarizes the Copilot features supported for a configured knowledge source.

| Feature|Knowledge base | External web resources |
|-------|----------|---------|--------|
|Ask a question |✔|X|
|Write an email | ✔|✔|
|Draft a response |✔|✔|

### See also

[Use Copilot to solve customer issues](../use/use-copilot-features.md)
