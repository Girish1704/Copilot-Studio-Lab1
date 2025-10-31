# Exercise 1: Create Safe Travels Agent and Deploy to Microsoft 365

### Estimated Duration: 20 Minutes

## Overview

In this foundational exercise, you will create your first intelligent conversational agent using Microsoft Copilot Studio's Safe Travels template. You'll learn the complete lifecycle of agent development, from initial creation and customization to enterprise deployment across Microsoft Teams and Microsoft 365 Copilot. The Safe Travels agent serves as a Business-to-Employee (B2E) solution that provides comprehensive travel assistance, helping employees access travel information, company policies, and essential travel-related guidance.

You'll discover how to leverage pre-built agent templates to accelerate development, customize knowledge sources with company-specific information, and integrate seamlessly with your organization's existing Microsoft 365 ecosystem. This exercise establishes the foundation for more advanced agent development scenarios and demonstrates the power of low-code AI development using Microsoft's enterprise-grade tools.

## Objectives

You will be able to complete the following tasks:

- Task 1: Create and customize the Safe Travels agent from template
- Task 2: Integrate company-specific knowledge sources and policies  
- Task 3: Test agent functionality and conversational capabilities
- Task 4: Publish agent to Microsoft Teams and Microsoft 365 Copilot
- Task 5: Validate enterprise deployment and user accessibility

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

1. Examine the **Knowledge** section where you'll see **US Travel Website** is already included as a knowledge source. This demonstrates how agents can leverage external information sources to provide accurate, up-to-date responses.

   ![Knowledge Sources](../media/knowledge-sources.png)

   > **Knowledge Integration:** You can replace or supplement the default knowledge sources with your own company travel policies, destination guides, or internal resources.

1. For this exercise, keep all default settings and click **Create** to generate your Safe Travels agent.

   ![Create Agent Button](../media/create-agent-button.png)

1. Wait for the agent creation process to complete. The system will automatically open the **Overview** page of your newly created agent.

   ![Agent Overview](../media/agent-overview.png)

   > **Success Indicator:** You should see the agent's overview page with various configuration options, knowledge sources, and the ability to test the agent immediately.

## Task 2: Test Agent Functionality and Capabilities

In this task, you will validate your Safe Travels agent's functionality by testing its conversational capabilities and knowledge integration. This testing phase ensures the agent responds appropriately to travel-related queries before deploying to end users.

1. Locate the **Test** panel on the right side of the screen. If it's not visible, click the **Test** icon in the top-right corner to open it.

   ![Test Panel](../media/test-panel.png)

1. In the test chat interface, enter your first query to test the agent's passport information capabilities:

   ```
   How to apply for passport?
   ```

   ![Passport Query](../media/passport-query.png)

1. Press **Send** or hit **Enter** to submit your query and observe the agent's response.

   ![Passport Response](../media/passport-response.png)

   > **Response Analysis:** The agent should provide comprehensive information about passport application procedures, demonstrating its ability to access and synthesize information from its knowledge sources.

1. Test additional travel-related scenarios to validate the agent's knowledge breadth:

   ```
   What documents do I need for international travel?
   ```

   ![Documents Query](../media/documents-query.png)

1. Try a more specific destination query:

   ```
   Tell me about travel requirements for New York
   ```

   ![Destination Query](../media/destination-query.png)

   > **Knowledge Source Validation:** These tests confirm the agent is successfully accessing the US Travel Website knowledge source and providing relevant, contextual responses.

1. Test the agent's conversational abilities with a follow-up question:

   ```
   What about vaccinations?
   ```

   ![Follow-up Query](../media/followup-query.png)

   > **Conversational Context:** The agent should maintain conversation context and provide relevant vaccination information related to travel.

## Task 3: Publish Agent to Microsoft Teams

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

## Task 4: Validate Enterprise Deployment

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

## Task 5: Enhance Agent with Company Knowledge

In this task, you will enhance your Safe Travels agent by adding company-specific knowledge sources, demonstrating how to customize agents with organizational policies and information.

1. From the agent's **Overview** page, scroll down to the **Knowledge** section and click **+ Add knowledge**.

   ![Add Knowledge](../media/add-knowledge.png)

1. In the knowledge source selection interface, click **select to browse** to upload a company document.

   ![Browse Knowledge](../media/browse-knowledge.png)

   > **Note:** For this lab exercise, you would typically upload a company travel policy document. The system supports various file formats including Word documents, PDFs, and text files.

1. If you have access to company travel policy documents, select and upload them. Otherwise, you can continue with the existing knowledge sources for this exercise.

   ![Upload Document](../media/upload-document.png)

1. After uploading any additional knowledge sources, wait for the processing to complete. The status should change from **In progress** to **Ready**.

   ![Knowledge Processing](../media/knowledge-processing.png)

   > **Processing Time:** Knowledge source processing time varies based on document size and complexity. Always wait for "Ready" status before testing.

1. Test the enhanced agent with company-specific queries if you've added additional knowledge sources:

   ```
   What is our company travel policy?
   ```

   ![Company Policy Query](../media/company-policy-query.png)

## Summary

In this exercise, you successfully created your first AI agent using Microsoft Copilot Studio's Safe Travels template and deployed it across your Microsoft 365 environment. You learned how to leverage pre-built templates to accelerate agent development, customize knowledge sources for company-specific needs, and publish agents to enterprise channels for organization-wide access.

Key accomplishments include:
- ✅ Created and configured the Safe Travels agent from template
- ✅ Tested agent functionality and conversational capabilities  
- ✅ Published agent to Microsoft Teams and Microsoft 365 Copilot
- ✅ Validated enterprise deployment and user accessibility
- ✅ Enhanced agent with additional knowledge sources

Your Safe Travels agent is now ready to assist employees with travel-related inquiries and serves as the foundation for more advanced agent development scenarios. The skills you've gained in this exercise will be essential as you progress to building custom Agent Flows and implementing multi-agent orchestration in the following exercises.

### You have successfully completed this exercise. Click **Next >>** to continue to Exercise 2.