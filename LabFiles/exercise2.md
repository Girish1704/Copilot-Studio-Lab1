# Exercise 2: Create Agent Flows and Business Process Automation

### Estimated Duration: 20 Minutes

## Overview

In this exercise, you will advance your AI agent development skills by creating sophisticated Agent Flows that enable business process automation and seamless integration with Microsoft Teams. You'll learn to build end-to-end workflows that connect conversational AI with real-world business processes, specifically focusing on travel approval automation. This exercise demonstrates the power of combining conversational AI with Microsoft Power Platform capabilities to create comprehensive business solutions.

You'll design an Agent Flow that captures employee travel requests, automatically posts them to designated Teams channels for approval, and provides feedback to users. Additionally, you'll create custom Topics that leverage these flows, establishing the foundation for complex multi-step business processes. This practical experience showcases how AI agents can serve as intelligent interfaces to enterprise workflows and automation systems.

## Objectives

You will be able to complete the following tasks:

- Task 1: Create a Microsoft Teams team and channel for travel approvals
- Task 2: Design and build a Travel Approval Agent Flow with Teams integration
- Task 3: Configure flow inputs, outputs, and Microsoft Teams connectivity
- Task 4: Create custom Topics that leverage Agent Flows for business processes
- Task 5: Test end-to-end travel approval workflow and validate automation

## Prerequisites

- Completed **Exercise 1** with published Safe Travels agent
- Access to **Microsoft Teams** with team and channel creation permissions
- Understanding of basic workflow concepts and business process automation
- **Safe Travels agent** available in your Copilot Studio environment

## Task 1: Create Teams Infrastructure for Travel Approvals

In this task, you will establish the Microsoft Teams infrastructure required for automated travel approval workflows. This includes creating a dedicated team and channel where travel requests will be automatically posted for manager review and approval.

1. Open **Microsoft Teams** in a new browser tab or use the desktop application, ensuring you're signed in with your tenant credentials.

   ![Teams Dashboard](../media/teams-dashboard.png)

1. In the left navigation pane, locate and click **See all your teams** to access team management options.

   ![Teams Navigation](../media/teams-see-all-teams.png)

1. Click **Create team** to start building your travel approval infrastructure.

   ![Create Team Button](../media/create-team-button.png)

1. In the team creation interface, configure the following details:
   - **Team name:** `HR Team`
   - **First channel name:** `Travel Approval Channel`

   ![Team Configuration](../media/team-configuration.png)

   > **Business Context:** Creating dedicated teams and channels for automated workflows ensures proper organization, security, and governance of business processes.

1. Click **Create** to establish your HR Team with the Travel Approval Channel.

   ![Create Team Confirm](../media/create-team-confirm.png)

1. When prompted to add members to the HR Team, click **Skip** for this lab exercise.

   ![Skip Add Members](../media/skip-add-members.png)

1. Verify that your HR Team and Travel Approval Channel are successfully created and accessible.

   ![Team Created Success](../media/team-created-success.png)

   > **Infrastructure Ready:** Your Teams infrastructure is now prepared to receive automated travel approval requests from your Agent Flow.

## Task 2: Create Travel Approval Agent Flow

In this task, you will build a sophisticated Agent Flow that automates the travel approval process by capturing employee requests and posting them to your newly created Teams channel. This demonstrates advanced integration between Copilot Studio and Microsoft Power Platform.

1. Return to **Microsoft Copilot Studio** and navigate to your **Safe Travels** agent.

   ![Safe Travels Agent](../media/safe-travels-agent.png)

1. From the left navigation pane, select **Flows** to access the Agent Flow development environment.

   ![Flows Navigation](../media/flows-navigation.png)

1. Click **New agent flow** to create a new automation workflow.

   ![New Agent Flow](../media/new-agent-flow.png)

1. In the flow designer, click **Add a trigger** to define how the flow will be initiated.

   ![Add Trigger](../media/add-trigger.png)

1. Select **When an agent calls the flow** under the **AI capabilities** section.

   ![Agent Trigger](../media/agent-trigger.png)

   > **Trigger Type:** This trigger enables your conversational agent to invoke the flow based on user interactions and natural language processing.

1. Configure the flow inputs by clicking **+ Add an input**.

   ![Add Input](../media/add-input.png)

1. Select **Number** as the input type and name it `Employee ID`.

   ![Employee ID Input](../media/employee-id-input.png)

1. Click **+ Add an input** again to add a second parameter.

   ![Add Second Input](../media/add-second-input.png)

1. Select **Text** as the input type and name it `Purpose`.

   ![Purpose Input](../media/purpose-input.png)

   > **Input Parameters:** These inputs will capture essential information from users during travel approval conversations.

## Task 3: Configure Microsoft Teams Integration

In this task, you will configure your Agent Flow to automatically post travel requests to your Teams channel, enabling seamless integration between conversational AI and collaborative workflows.

1. Below the trigger node, click **Add an action** to begin building your workflow logic.

   ![Add Action](../media/add-action.png)

1. In the action search interface, type `Teams` and click **See more** under the Teams connector group.

   ![Search Teams](../media/search-teams.png)

1. Select **Post message in a chat or channel** from the available Teams actions.

   ![Post Message Action](../media/post-message-action.png)

1. Click **Sign in** to authenticate your Teams connection and provide necessary permissions.

   ![Teams Sign In](../media/teams-sign-in.png)

1. Complete the authentication process using your tenant credentials when prompted.

   ![Teams Authentication](../media/teams-authentication.png)

1. Configure the Teams message posting parameters:
   - **Post as:** Select `User`
   - **Post in:** Select `Channel`
   - **Team:** Select `HR Team`
   - **Channel:** Select `Travel Approval Channel`

   ![Teams Configuration](../media/teams-configuration.png)

1. In the **Message** field, create a formatted travel request message using the following template:

   ```
   Travel Request from 
   Employee ID - <Employee ID>
   Purpose - <Purpose>
   ```

   ![Message Template](../media/message-template.png)

   > **Dynamic Content:** Replace `<Employee ID>` and `<Purpose>` with the corresponding dynamic content variables from your flow inputs.

1. Click on the **Employee ID** dynamic content to insert it into your message template.

   ![Insert Employee ID](../media/insert-employee-id.png)

1. Similarly, insert the **Purpose** dynamic content variable to complete your message template.

   ![Insert Purpose](../media/insert-purpose.png)

1. Review your completed message configuration to ensure proper dynamic content integration.

   ![Complete Message Config](../media/complete-message-config.png)

## Task 4: Configure Flow Response and Publishing

In this task, you will complete your Agent Flow by configuring the response that users will receive and publishing the flow for use by your conversational agent.

1. Add another action after the Teams message posting by clicking **Add an action**.

   ![Add Response Action](../media/add-response-action.png)

1. Under the **Skills** section, select **Respond to the agent**.

   ![Respond to Agent](../media/respond-to-agent.png)

1. Click **Add an output** to configure what the agent will communicate back to the user.

   ![Add Output](../media/add-output.png)

1. Configure the output parameter:
   - **Type:** Select `Text`
   - **Name:** `Output`
   - **Value:** `Request submitted`

   ![Output Configuration](../media/output-configuration.png)

   > **User Feedback:** This output provides confirmation to users that their travel request has been successfully submitted for approval.

1. Click **Save draft** to preserve your flow configuration.

   ![Save Draft](../media/save-draft.png)

1. After saving, click **Publish** to make your flow available for agent integration.

   ![Publish Flow](../media/publish-flow.png)

1. Confirm the flow has been successfully published by checking the status indicator.

   ![Flow Published](../media/flow-published.png)

1. Navigate to the **Overview** tab of your Agent Flow.

   ![Flow Overview](../media/flow-overview.png)

1. Click **Edit** to customize the flow name and description.

   ![Edit Flow Details](../media/edit-flow-details.png)

1. Update the flow name to `Request Travel Approval Flow` and click **Save**.

   ![Update Flow Name](../media/update-flow-name.png)

   > **Flow Management:** Descriptive naming helps maintain organization and clarity in complex automation scenarios.

## Task 5: Integrate Agent Flow with Safe Travels Agent

In this task, you will connect your newly created Agent Flow to your Safe Travels agent, enabling users to trigger travel approval workflows through natural conversation.

1. From the left navigation, select **Agents** to return to your agent management interface.

   ![Agents Navigation](../media/agents-navigation.png)

1. Select your **Safe Travels** agent to access its configuration.

   ![Select Safe Travels](../media/select-safe-travels.png)

1. On the agent's Overview page, scroll down and click **Add tool** to integrate your flow.

   ![Add Tool](../media/add-tool.png)

1. In the tool selection interface, navigate to the **Flow** tab and select your **Request Travel Approval Flow**.

   ![Select Flow Tool](../media/select-flow-tool.png)

1. Click **Add to agent** to complete the integration.

   ![Add Flow to Agent](../media/add-flow-to-agent.png)

1. Verify that your flow appears in the **Tools** section of your agent's Overview page.

   ![Flow Added Confirmation](../media/flow-added-confirmation.png)

   > **Tool Integration:** Your agent can now access and execute the travel approval workflow as part of conversational interactions.

## Task 6: Create Custom Topic for Travel Approval

In this task, you will create a custom Topic that enables natural language triggering of your travel approval workflow, providing a seamless user experience for travel request submission.

1. From the top navigation, select **Topics** to access topic management.

   ![Topics Navigation](../media/topics-navigation.png)

1. Click **+ Add a topic** and select **Add from description with Copilot**.

   ![Add Topic with Copilot](../media/add-topic-copilot.png)

1. Configure your topic with the following details:
   - **Name:** `Travel Approval`
   - **Create a topic to:** `This topic should get the Employee ID (Number) and Purpose of travel (Text) details from the user and invoke the Tool "Request Travel Approval Flow"`

   ![Topic Configuration](../media/topic-configuration.png)

1. Click **Create** to generate your travel approval topic.

   ![Create Topic](../media/create-topic.png)

1. Review the generated topic structure and verify it includes nodes for collecting Employee ID and Purpose information.

   ![Topic Structure](../media/topic-structure.png)

1. If the flow invocation node is not automatically created, add it manually by clicking **Add a node** after the purpose collection.

   ![Add Flow Node](../media/add-flow-node.png)

1. Select **Add a tool** and choose **Request Travel Approval Flow**.

   ![Select Flow Tool in Topic](../media/select-flow-tool-topic.png)

1. Map the collected variables to the flow inputs:
   - **Employee ID** → `EmployeeID` variable
   - **Purpose** → `Purpose` variable

   ![Map Variables](../media/map-variables.png)

1. Add a final message node that displays the flow output to confirm successful submission.

   ![Add Confirmation Message](../media/add-confirmation-message.png)

1. Click **Save** to preserve your topic configuration.

   ![Save Topic](../media/save-topic.png)

## Task 7: Test End-to-End Travel Approval Workflow

In this task, you will validate your complete travel approval workflow by testing the integration between your conversational agent, Agent Flow, and Teams channel.

1. Click **Publish** to make your updated agent with the new topic available for testing.

   ![Publish Agent](../media/publish-agent.png)

1. Confirm the publishing action in the dialog box.

   ![Confirm Publish](../media/confirm-publish.png)

1. Open the **Test** panel and initiate a travel approval conversation:

   ```
   Travel Approval
   ```

   ![Test Travel Approval](../media/test-travel-approval.png)

1. Provide the requested information when prompted:
   - **Employee ID:** `1234`
   - **Purpose of travel:** `Client meeting for finalizing proposal of XYZ project`

   ![Provide Travel Details](../media/provide-travel-details.png)

1. When prompted for permissions, click **Allow** to enable the flow execution.

   ![Allow Permissions](../media/allow-permissions.png)

1. Verify you receive the confirmation message "Request submitted" from the agent.

   ![Request Submitted](../media/request-submitted.png)

1. Navigate to your **Microsoft Teams** HR Team and check the Travel Approval Channel for the automated message.

   ![Teams Channel Verification](../media/teams-channel-verification.png)

   > **Success Validation:** You should see your travel request details posted automatically to the Teams channel, demonstrating successful end-to-end workflow automation.

## Summary  

In this exercise, you successfully created sophisticated business process automation using Agent Flows and Microsoft Teams integration. You learned how to design workflows that bridge conversational AI with real-world business processes, enabling employees to submit travel requests through natural conversation while automatically routing them to appropriate approval channels.

Key accomplishments include:
- ✅ Created Teams infrastructure for travel approval workflows
- ✅ Built comprehensive Agent Flow with dynamic inputs and Teams integration
- ✅ Configured automated message posting to designated Teams channels
- ✅ Created custom Topics that trigger complex business processes
- ✅ Validated end-to-end workflow automation and user experience

Your travel approval automation system now demonstrates how AI agents can serve as intelligent interfaces to enterprise business processes, reducing manual overhead while maintaining proper approval workflows. The skills you've developed in this exercise provide the foundation for implementing multi-agent orchestration scenarios in the next exercise.

### You have successfully completed this exercise. Click **Next >>** to continue to Exercise 3.