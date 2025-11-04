# Exercise 1: Create Safe Travels Agent and Deploy to Microsoft Teams

### Estimated Duration: 30 Minutes

## Overview

In this foundational exercise, you'll create your first AI agent using Microsoft Copilot Studio's Safe Travels template. This is a practical, hands-on introduction to conversational AI that will give you a working travel assistant agent deployed to Microsoft Teams by the end of 30 minutes.

The Safe Travels agent will help employees with travel-related questions, policy information, and guidance. You'll see how easy it is to create powerful AI agents using templates, test them thoroughly, and deploy them to your organization's collaboration platform. This exercise focuses on getting you comfortable with the core agent development workflow that applies to any business scenario.

## Objectives

You will be able to complete the following tasks:

- Task 1: Set up Power Platform environment and navigate to Copilot Studio
- Task 2: Create Safe Travels agent from template  
- Task 3: Test and validate agent functionality
- Task 4: Publish and deploy agent to Microsoft Teams

## Prerequisites

- Access to **Microsoft Copilot Studio** with agent creation permissions
- **Microsoft Teams** access for testing deployed agents
- **Admin tenant credentials** for publishing to enterprise channels
- Basic understanding of conversational AI and Microsoft 365 collaboration tools

## Task 1: Set Up Power Platform Environment

In this task, you will set up the Power Platform environment that will support your Copilot Studio agents with the necessary data sources and knowledge files.

1. Navigate to **Power Platform** and sign in with your admin tenant credentials. From the left navigation menu, select **Tables (1)** and click on **Create with Excel or .CSV file (2)** to set up your environment with the lab data files.

   ![Power Platform Tables](../media/ex1-travel-g1.png)

   > **Environment Foundation:** This step creates the foundational environment that will support your agents with company-specific data and knowledge sources.

1. In the **Create in new environment** dialog that appears, you'll see a message about permissions. Click **Create** to create a free developer environment.

   ![Create Environment Dialog](../media/ex1-travel-g2.png)

   > **Note:** The system will create a new developer environment which may take a moment to provision. You'll be redirected when it's ready.

1. Wait for the environment creation process to complete. The system will show progress indicators during setup.

   ![Environment Creation Progress](../media/ex1-travel-g3.png)

1. Once the environment is ready, you'll see the Tables interface with various creation options available. The environment is now configured for agent development.

   ![Environment Ready](../media/ex1-travel-g4.png)

1. Navigate to **Microsoft Copilot Studio** by opening a new browser tab and going to `https://copilotstudio.microsoft.com`.

   ![Navigate to Copilot Studio](../media/ex1-travel-g5.png)

1. Sign in to Copilot Studio with your admin tenant credentials. You'll see the Copilot Studio welcome interface.

   ![Copilot Studio Welcome](../media/ex1-travel-g6.png)

## Task 2: Create Safe Travels Agent from Template

In this task, you will create your first AI agent using the pre-built Safe Travels template, which provides a solid foundation with built-in travel assistance capabilities.

1. Once signed in to Copilot Studio, you'll see the main dashboard. From the left navigation pane, select **Create** to start building a new agent.

   ![Copilot Studio Dashboard](../media/ex1-travel-g7.png)

1. In the agent creation interface, you'll see different template options. Locate and click on the **Safe Travels** template to select it.

   ![Safe Travels Template Selection](../media/ex1-travel-g8.png)

   > **Template Benefits:** The Safe Travels template includes pre-configured conversational flows, travel-related knowledge sources, and common travel assistance scenarios, significantly reducing development time.

1. Review the template details and click **Use this template** to proceed with the Safe Travels template.

   ![Use Template](../media/ex1-travel-g9.png)

1. Configure your Safe Travels agent with the following details:
   - **Name:** `Safe Travels Agent`
   - **Description:** `A travel assistant agent that helps employees with travel planning, policies, and guidance`

   ![Agent Configuration](../media/ex1-travel-g10.png)

1. Review all the configuration settings and click **Create** to generate your Safe Travels agent.

   ![Create Agent](../media/ex1-travel-g11.png)

1. The system will process your agent creation. Wait for the creation process to complete.

   ![Agent Creation Progress](../media/ex1-travel-g12.png)

1. Once created successfully, you'll be taken to the agent's **Overview** page where you can see the agent details and configuration options.

   ![Agent Overview](../media/ex1-travel-g13.png)

   > **Success Indicator:** You should see the agent's overview page with various configuration options, knowledge sources, and the ability to test the agent immediately.

## Task 3: Test and Validate Agent Functionality

In this task, you'll test your Safe Travels agent to validate its functionality and responses to travel-related queries.

1. On the agent overview page, locate the **Test** button or panel on the right side of the screen to begin testing your agent.

   ![Test Agent Interface](../media/ex1-travel-g14.png)

1. In the test interface, start by testing the agent's passport information capabilities. Type the following query:

   ```
   How to apply for passport?
   ```

   ![Passport Information Query](../media/ex1-travel-g15.png)

   > **Expected Response:** The agent should provide comprehensive passport application information from its built-in travel knowledge base.

1. Test another travel-related query to validate the agent's knowledge. Ask about travel destinations:

   ```
   Tell me about travel to New York
   ```

   ![Travel Destination Query](../media/ex1-travel-g16.png)

1. Continue testing with additional travel scenarios to ensure the agent responds appropriately to various travel-related questions.

   ![Additional Travel Testing](../media/ex1-travel-g17.png)

1. Test the agent's ability to handle travel policy questions:

   ```
   What should I know about business travel?
   ```

   ![Business Travel Query](../media/ex1-travel-g18.png)

   > **Knowledge Integration:** The agent leverages its built-in travel knowledge to provide helpful responses across various travel scenarios.

## Task 4: Publish and Deploy Agent to Microsoft Teams

In this task, you will publish your Safe Travels agent and deploy it to Microsoft Teams, making it accessible to your organization's employees.

1. After testing, click the **Publish** button in the top-right corner of the agent interface to begin the publishing process.

   ![Publish Agent](../media/ex1-travel-g19.png)

1. In the publish dialog, review the publishing details and click **Publish** to confirm and publish your agent.

   ![Publish Confirmation](../media/ex1-travel-g20.png)

   > **Publishing Process:** The agent will be packaged and made available for channel deployment. This process may take a few moments to complete.

1. Once published successfully, navigate to the **Channels** section to configure deployment channels for your agent.

   ![Navigate to Channels](../media/ex1-travel-g21.png)

1. In the Channels interface, you'll see available deployment options. Select **Microsoft Teams** to deploy your agent to Teams.

   ![Select Teams Channel](../media/ex1-travel-g22.png)

   > **Channel Benefits:** Deploying to Microsoft Teams provides users access through their familiar collaboration environment, increasing adoption and usage.

1. Configure the Teams channel settings and click **Save** or **Add** to add the Teams channel to your agent.

   ![Configure Teams Channel](../media/ex1-travel-g23.png)

1. Review the channel configuration and submit for approval if required by your organization's policies.

   ![Channel Configuration Review](../media/ex1-travel-g24.png)

1. Once the channel is configured, click **Open in Teams** or similar option to test the agent deployment in Microsoft Teams.

   ![Open in Teams](../media/ex1-travel-g25.png)

1. Microsoft Teams will open with your Safe Travels agent available. Click **Add** to add the agent to your Teams environment.

   ![Add Agent to Teams](../media/ex1-travel-g26.png)

1. After adding the agent, click **Open** to start a conversation with your Safe Travels agent in Teams.

   ![Open Agent Chat](../media/ex1-travel-g27.png)

1. Test the agent functionality within Teams by asking a travel-related question:

   ```
   I need help planning a business trip
   ```

   ![Test Agent in Teams](../media/ex1-travel-g28.png)

1. Verify that the agent responds appropriately within the Teams environment, maintaining the same functionality as in the Copilot Studio test environment.

   ![Agent Response in Teams](../media/ex1-travel-g29.png)

   > **Integration Success:** The agent should provide consistent responses regardless of the access channel (Copilot Studio or Teams).

1. Continue testing various travel scenarios to ensure full functionality in the Teams environment.

   ![Additional Teams Testing](../media/ex1-travel-g30.png)

1. Navigate back to Copilot Studio to review the agent deployment status and confirm successful channel configuration.

   ![Review Deployment Status](../media/ex1-travel-g31.png)

1. Verify that the Teams channel is active and the agent is successfully deployed.

   ![Deployment Verification](../media/ex1-travel-g32.png)

1. Review the agent analytics and usage metrics to understand how the agent is performing.

   ![Agent Analytics](../media/ex1-travel-g33.png)

1. Check the agent's conversation history and performance metrics to ensure optimal functionality.

   ![Performance Metrics](../media/ex1-travel-g34.png)

1. Validate that all agent features are working correctly across both Copilot Studio and Teams platforms.

   ![Feature Validation](../media/ex1-travel-g35.png)

1. Review the final agent configuration to ensure all settings are optimized for your organization's needs.

   ![Final Configuration Review](../media/ex1-travel-g36.png)

1. Confirm that the agent is ready for enterprise deployment and user access.

   ![Enterprise Readiness](../media/ex1-travel-g37.png)

1. Document the successful deployment and provide access instructions for end users.

   ![Deployment Documentation](../media/ex1-travel-g38.png)

1. Monitor the agent's initial performance and gather user feedback for potential improvements.

   ![Performance Monitoring](../media/ex1-travel-g39.png)

1. Complete the deployment process by confirming all systems are operational and the agent is accessible to intended users.

   ![Deployment Complete](../media/ex1-travel-g40.png)

   > **Deployment Success:** Your Safe Travels agent is now successfully published and available through Microsoft Teams for your organization's use.

## Summary

Excellent work! In just 30 minutes, you've successfully:

- ✅ Set up a Power Platform environment for agent development
- ✅ Created a working Safe Travels agent using Microsoft's template
- ✅ Tested the agent's travel assistance capabilities with real queries
- ✅ Published and deployed the agent to Microsoft Teams for your organization

Your Safe Travels agent is now live and ready to help employees with travel questions, passport information, and destination guidance. You've experienced the power of low-code AI development - creating enterprise-ready conversational agents without any programming.

**What's Next:** In Exercise 2, you'll enhance your agent with custom business processes and explore multi-agent orchestration capabilities.

### You have successfully completed Exercise 1. Click **Next >>** to continue to Exercise 2.