---
title: Configure automated messages
description: Perform the steps mentioned in the article to configure automated messages in Omnichannel for Customer Service.
ms.date: 02/29/2024
author: lalexms
ms.author: laalexan
ms.reviewer: nenellim
ms.topic: how-to
ms.custom: bap-template
---

# Configure automated messages

[!INCLUDE[cc-use-with-omnichannel](../../includes/cc-use-with-omnichannel.md)]

You can configure Omnichannel for Customer Service to send automated messages through a channel, such as chat, voice, SMS, or social channels. The **Automated messages** tab in each channel instance enables you to create channel-specific and locale-specific text. You can customize, deactivate, and activate customer and agent-facing messages at the channel level.
As an administrator, you can also overwrite or deactivate the preconfigured, out-of-the-box automated messages for any channel instance. The preconfigured automated message triggers are listed in [this section](#preconfigured-automated-message-triggers).

## Display a list of all automated messages

You can view a list of all agent and customer-facing automated messages in your Omnichannel for Customer Service environment.

1. Go to one of the apps, and perform the following steps.
   
   ### [Customer Service admin center](#tab/customerserviceadmincenter)
     
     1. In the site map, select **Customer Settings** in **Customer support**. The **Customer settings** page appears.
     1. In the **Automated messages** section, select **Manage**.

     The **Automated messages** page is displayed.

   ### [Omnichannel admin center (deprecated)](#tab/omnichanneladmincenter)

    [!INCLUDE[oac-deprecation](../../includes/oac-deprecation.md)] 
    
     1. In the site map, select **Customer Settings** in **Advanced settings**. The **Customer settings** page appears.
     2. In the **Automated messages** section, select **Manage**.

      The **Automated messages** page is displayed.

    > [!div class=mx-imgBorder]
    > ![Display all automated messages.](../media/automated-messages-list.png "Display all automated messages")
2. Select one or more of the records to edit the language code and text. If you want to deactivate the messages, select the **Deactivate** button.

## Customize automated messages at the channel level

You can customize messages across instances within a channel. For example, you can apply a change to all Facebook accounts or all SMS numbers.

1. Select a message on the **Automated messages** page, and then select **Edit**.

2. On the **General** tab, edit the **Localized text** field, and then select **Save**.

    The message field supports the following slugs.
    
    | **Slug** | **Description** |
    |----------|-----------------|
    |{AgentName} | The full name of the agent who is assigned to the conversation. |
    |{QueueName} | The name of the queue. |

    > [!div class=mx-imgBorder]
    > ![Configure automated messages at channel level.](../media/automated-messages-general.png "Configure automated messages at channel level")

## Customize automated messages at the channel instance level

You can customize automated messages at the channel instance level. For example, you can apply a change to a specific Facebook account or a specific SMS number. If you don't create customized automated messages at the channel instance level, each instance inherits the channel-level settings.

> [!IMPORTANT]
> If you create customized automated messages at the channel instance level, then the channel-level settings are overwritten.

### Add custom automated messages

Do the following for the channel in which you want to create custom automated messages in the Customer Service admin center or Omnichannel admin center (deprecated) app:

1. Go to the workstream, and edit the channel instance.
2. On the **Behaviors** page, select **Add message** in the **Custom automated messages** area.
3. On the **Add automated message** pane, select a trigger from the **Select a message trigger** dropdown list.
4. In the **Automated message** box, type the message that should be displayed.
5. Select **Confirm**.
6. Repeat steps 3 through 5 to create multiple messages.
7. Save the settings.

## Preconfigured automated message triggers

| **Message trigger** | **Definition** | **When to trigger** |
|-----------------|------------|-----------------|
| Greeting Message for Async Channels and Voice | The automated message played for the customer as soon as the call is connected <br>**Note**<br> If the bot is enabled, ensure that the automated greeting message is different from the bot message. | You can set it up to be played as the first message that the customer should hear when they call the digital contact center. |
| Agent assigned to a conversation | Message displayed to the customer when the agent is assigned to the conversation | When the agent is assigned to the conversation.
| Agent couldn’t be assigned to conversation   | Message displayed to the customer when agent assignment fails | When work distribution fails or when routing is unable to add the agent to the chat due to system (CBB/IC3) failure. For example, no agents are linked to the queue, or the default queue isn't found. <br>**Note**<br> This trigger isn't applicable to a scenario when a matching agent can't be identified based on the assignment configuration. |
| Agent disconnected from conversation | Message displayed to the customer when the agent gets disconnected | When the agent gets disconnected due to browser tab closure, browser closure, offline agent presence, or network issue.  |
| Agent ended conversation | Message displayed to the customer when the agent ends the conversation | When the agent selects the End button |
| Agent joined conversation | Message displayed to the customer when the agent joins a conversation | When the agent accepts the notification. |
| Agent joined customer conversation | Message displayed to the customer when the agent joins a customer conversation | When the agent joins a customer conversation.  |
| Agent left customer conversation | Message displayed to the customer when the agent leaves a customer conversation. | When the agent leaves a customer conversation. |
| Average wait time for customers: Hours <br> (applies to live chat and voice channels only) | Message displayed to the customer with the average wait time displayed in hours  |  When customer is waiting in queue. |
| Average wait time for customers: Hours and minutes <br> (applies to live chat and voice channels only) | Message displayed when the customer is waiting in queue with average wait time being displayed in both minutes and hours | When customer is waiting in queue |
| Average wait time for customers: Minutes <br> (applies to live chat and voice channels only)  | Message displayed to the customer with the average wait time displayed in minutes  | When customer is waiting in queue. |
| Consult accepted  | Message displayed to the customer when another agent is consulted successfully  | When another agent accepts the consult request.  |
| Consult session ended  | Message displayed to the customer when consulted agent ends the session | When the consulted agent closes the session. |
| Customer is next in line  |   Message displayed when the customer is next in line in the queue  |  When customer is next in line in the queue. |
| Customer's position in queue |  Message displayed when the customer is waiting in queue at the second position or beyond | When customer is waiting in queue at the second position or beyond. |
| Customer disconnected from conversation | Message displayed to the agent when the customer gets disconnected | When customer explicitly closes the browser tab or gets disconnected because of network issue.  |
| Holiday message to customer | Message displayed to the customer on holidays | When the customer initiates a conversation on holidays set up for the Live Chat, channel, or queue.  |
| Out of operating hour message to customer | Message displayed to the customer outside of the business hours  | When customer initiates a conversation outside of business hours set up for the Live Chat, channel, or queue. |
| Session ended   | Message displayed to the customer when the agent ends the conversation and closes the session| When the agent ends the conversation and closes the session. |
| Transfer to agent accepted  | Message displayed to the customer when the conversation is transferred successfully | When another agent accepts the transfer request.|
|Offer customer callback |The callback message played for the customer when the wait times are longer than expected| When the customer calls and wait time is long.|
| Customer callback response | When the customer presses 1 on the call menu, a confirmation message is played to indicate the customer choice.| Customer presses 1 on the call menu. The response to offer customer callback message is played.|

## Best practices for using automated messages 

Use the following best practices when you configure automated messages for the voice channel:

- Make sure that you configure concise messages when you use automated and custom messages because lengthy messages might mean that agents take longer to connect with customers.

- Consider configuring **Greeting Message for Async Channels and Voice** instead of **Agent assigned to a conversation**.

- If you've configured both **Agent assigned to a conversation** and **Greeting Message for Async Channels and Voice**, consider configuring **Greeting Message for Async Channels and Voice** to avoid the accumulation of messages in the queue.

- Disable messages that announce the average wait times, unless your business requires that customers know this information. 
 
## Next steps

[Add a chat widget](add-chat-widget.md)  

### See also
[Channels](../use/channels.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
