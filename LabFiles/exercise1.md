# Exercise 1: Create Safe Travels Agent and Deploy to Microsoft Teams

### Estimated Duration: 30 Minutes

## Overview

In this foundational exercise, you'll create your first AI agent using Microsoft Copilot Studio's Safe Travels template. This is a practical, hands-on introduction to conversational AI that will give you a working travel assistant agent deployed to Microsoft Teams by the end of 30 minutes.

The Safe Travels agent will help employees with travel-related questions, policy information, and guidance. You'll see how easy it is to create powerful AI agents using templates, test them thoroughly, and deploy them to your organization's collaboration platform. This exercise focuses on getting you comfortable with the core agent development workflow that applies to any business scenario.

## Objectives

You will be able to complete the following tasks:

- Task 1: Create the Safe Travels agent from template (8 mins)
- Task 2: Add company Travel Policy knowledge source (5 mins)
- Task 3: Test enhanced agent functionality (7 mins)  
- Task 4: Publish and deploy agent to Microsoft Teams (10 mins)

## Prerequisites

- Access to **Microsoft Copilot Studio** with agent creation permissions
- **Microsoft Teams** access for testing deployed agents
- **Admin tenant credentials** for publishing to enterprise channels
- Basic understanding of conversational AI and Microsoft 365 collaboration tools

## Task 1: Create Safe Travels Agent from Template

In this task, you will navigate Microsoft Copilot Studio and create your first AI agent using the pre-built Safe Travels template. This template provides a solid foundation with built-in travel assistance capabilities that you can customize for your organization's specific needs.

1. Ensure you're signed in to **Microsoft Copilot Studio** at `https://copilotstudio.microsoft.com`.

   ![Copilot Studio Home](../media/copilot-studio-home.png)

1. In the top navigation, verify you're working in the correct environment. If you see an environment selector, choose **Dev One** environment for this lab.

   ![Environment Selection](../media/environment-selection.png)

   > **Important Note:** If you don't see the environment selector or need to access a specific environment ID, you can navigate directly using the environment-specific URL format: `https://copilotstudio.microsoft.com/environments/{EnvironmentID}`

1. From the left navigation pane, select **+ Create** to start building a new agent.

   ![Create New Agent](../media/create-new-agent.png)

1. In the agent creation interface, locate the **Start with an agent template** section and select the **Safe Travels** template.

   ![Safe Travels Template](../media/safe-travels-template.png)

   > **Template Benefits:** The Safe Travels template includes pre-configured conversational flows, travel-related knowledge sources, and common travel assistance scenarios, significantly reducing development time.

1. Review the template description and capabilities. The Safe Travels template is designed to:
   - Provide employees with comprehensive travel assistance
   - Offer conversational interface for easy information access
   - Include built-in US travel destination knowledge
   - Support customization with company-specific policies

   ![Template Overview](../media/template-overview.png)

1. Configure your Safe Travels agent with these specific details:
   - **Agent name:** `Safe Travels Agent`
   - **Description:** `A travel assistant agent that helps employees with travel planning, policies, and guidance`

   ![Agent Configuration](../media/agent-configuration.png)

1. Examine the **Knowledge** section where you'll see **US Travel Website** is already included as a knowledge source. Keep this default source - we'll add our company travel policy in the next task.

   ![Knowledge Sources](../media/knowledge-sources.png)

   > **Knowledge Integration:** The template includes general travel information, but we'll enhance it with company-specific policies next.

1. Review all settings and click **Create** to generate your Safe Travels agent.

   ![Create Agent Button](../media/create-agent-button.png)

1. Wait for the agent creation process to complete. The system will automatically open the **Overview** page of your newly created agent.

   ![Agent Overview](../media/agent-overview.png)

   > **Success Indicator:** You should see the agent's overview page with various configuration options, knowledge sources, and the ability to test the agent immediately.

## Task 2: Add Company Travel Policy Knowledge (5 minutes)

In this task, you'll enhance your Safe Travels agent with company-specific travel policy information, making it more useful for real business scenarios.

1. On the agent's **Overview** page, scroll down to the **Knowledge** section and click **+ Add knowledge**.

   ![Add Knowledge](../media/add-knowledge.png)

1. Click **select to browse** to upload the company travel policy document.

   ![Browse Knowledge](../media/browse-knowledge.png)

1. Navigate to the lab files directory and select **Travel Policy.docx**. Click **Open**.

   ![Upload Travel Policy](../media/upload-travel-policy.png)

   > **File Location:** The Travel Policy.docx file contains company-specific travel guidelines, approval processes, and policy information that will enhance your agent's responses.

1. Click **Add to agent** to integrate the travel policy with your agent.

   ![Add Policy to Agent](../media/add-policy-agent.png)

1. Wait for the file processing to complete. The status should change from **In progress** to **Ready** before proceeding.

   ![Knowledge Processing](../media/knowledge-processing.png)

   > **Processing Time:** Knowledge processing typically takes 1-2 minutes. The agent will now be able to answer company-specific travel policy questions.

## Task 3: Test Enhanced Agent Functionality

In this task, you'll test your enhanced Safe Travels agent to see how it handles both general travel questions and company-specific policy inquiries.

1. Locate the **Test** panel on the right side of the screen. If it's not visible, click the **Test** icon in the top-right corner.

   ![Test Panel](../media/test-panel.png)

1. First, test the agent's passport information capabilities:

   ```
   How to apply for passport?
   ```

   ![Passport Query](../media/passport-query.png)

   > **Expected Response:** The agent should provide comprehensive passport application information from its built-in travel knowledge.

1. Now test the company travel policy integration:

   ```
   What is our company travel policy?
   ```

   ![Travel Policy Query](../media/travel-policy-query.png)

   > **Enhanced Knowledge:** The agent should now provide company-specific travel policy information from the Travel Policy.docx file you uploaded.

1. Test a travel approval scenario:

   ```
   Need travel approval
   ```

   ![Travel Approval Query](../media/travel-approval-query.png)

   > **Policy Integration:** The agent should provide specific guidance based on your company's travel approval process from the policy document.

## Task 4: Publish Agent to Microsoft Teams

In this task, you will deploy your Safe Travels agent to Microsoft Teams, making it accessible to your organization's employees through their familiar collaboration environment. This integration demonstrates enterprise-scale agent deployment capabilities.

1. Before publishing, ensure Microsoft Teams is available in your environment. Open **Microsoft Teams** in a new browser tab or desktop application and sign in with your tenant credentials.

   ![Teams Login](../media/teams-login.png)

1. Return to Copilot Studio and click **Publish** in the top-right corner of the agent page.

   ![Publish Button](../media/publish-button.png)

1. In the publish confirmation dialog, review the publishing details and click **Publish** to confirm.

   ![Publish Confirmation](../media/publish-confirmation.png)

   > **Publishing Process:** The agent will be packaged and made available for channel deployment. This process may take a few moments to complete.

1. After successful publishing, navigate to **Channels** from the top navigation bar.

   ![Channels Navigation](../media/channels-navigation.png)

1. From the available channels list, select **Teams and Microsoft 365 Copilot**.

   ![Teams Channel Selection](../media/teams-channel-selection.png)

   > **Channel Benefits:** This channel enables deployment to both Microsoft Teams and Microsoft 365 Copilot, providing multiple access points for end users.

1. Click **Add channel** to configure the Teams integration.

   ![Add Channel](../media/add-channel.png)

1. Once the channel is configured, click **See agent in Teams** to test the deployment.

   ![See Agent in Teams](../media/see-agent-teams.png)

1. This will open Microsoft Teams with your agent available for installation. Click **Add** to add the agent to your Teams environment.

   ![Teams Add Agent](../media/teams-add-agent.png)

1. After adding the agent, click **Open** to start interacting with it in Teams.

   ![Teams Open Agent](../media/teams-open-agent.png)

## Task 5: Validate Enterprise Deployment

In this task, you will validate that your Safe Travels agent is successfully deployed and accessible to users through Microsoft Teams, ensuring the enterprise integration is working correctly.

1. In the Microsoft Teams interface, you should now see your Safe Travels agent in a chat window. Test its functionality by entering a travel-related query:

   ```
   I need help with travel planning
   ```

   ![Teams Agent Test](../media/teams-agent-test.png)

1. Verify the agent responds appropriately within the Teams environment, maintaining the same functionality as in the Copilot Studio test environment.

   ![Teams Agent Response](../media/teams-agent-response.png)

   > **Integration Success:** The agent should provide consistent responses regardless of the access channel (Copilot Studio or Teams).

1. Test the agent's knowledge integration by asking about specific travel information:

   ```
   What are the current travel restrictions?
   ```

   ![Travel Restrictions Query](../media/travel-restrictions-query.png)

1. Return to Copilot Studio and close the Teams channel configuration window by clicking the **X** or **Close** button.

   ![Close Channel Window](../media/close-channel-window.png)

1. Navigate back to your agent's **Overview** page to review the deployment status and available channels.

   ![Agent Deployment Status](../media/deployment-status.png)

   > **Deployment Verification:** You should see confirmation that your agent is successfully published and available through the Teams and Microsoft 365 Copilot channel.



## Summary

Excellent work! In just 30 minutes, you've successfully:

- ✅ Created a working Safe Travels agent from Microsoft's template
- ✅ Tested its travel assistance capabilities with real queries
- ✅ Published the agent to Microsoft Teams for your organization

Your Safe Travels agent is now live and ready to help employees with travel questions, passport information, and destination guidance. You've experienced the power of low-code AI development - creating enterprise-ready conversational agents without any programming.

**What's Next:** In Exercise 2, you'll add business process automation and see how multiple agents can work together to handle complex employee requests.

### You have successfully completed Exercise 1. Click **Next >>** to continue to Exercise 2.