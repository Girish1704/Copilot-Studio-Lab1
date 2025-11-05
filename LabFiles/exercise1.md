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

   - In Copilot Studio, click the **environment name** in the top bar (for example, **CloudLabs Sandbox (dev...)**).
   - In the panel, expand **Supported environments** by clicking the small **chevron**.
   - Click **ODL_User <inject key="Deployment ID" enableCopy="false"></inject>'s Environment** to switch.  

   ![Copilot Studio Welcome](../media/ex1-travel-g6.png)

## Task 2: Create Safe Travels Agent from Template

In this task, you will create your first AI agent using the pre-built Safe Travels template, which provides a solid foundation with built-in travel assistance capabilities.

1. Once signed in to Copilot Studio, you'll see the main dashboard. From the left navigation pane, select **Create** to start building a new agent.
1. In the agent creation interface, you'll see different template options. Locate and click on the **Safe Travels** template to select it.

    ![Copilot Studio Dashboard](../media/ex1-travel-g7.png)
   
1. Configure your Safe Travels agent with the following details:
   - **Name:** `Safe Travels Agent`
   - **Description:** `A travel assistant agent that helps employees with travel planning, policies, and guidance`
  
      ![Safe Travels Template Selection](../media/ex1-travel-g8.png)
  
1. Review the template details and click **Use this template** to proceed with the Safe Travels template.
1. Review all the configuration settings and click **Create** to generate your Safe Travels agent.

   ![Use Template](../media/ex1-travel-g9.png)

   > **Template Benefits:** The Safe Travels template includes pre-configured conversational flows, travel-related knowledge sources, and common travel assistance scenarios, significantly reducing development time.

1. Add knowledge to your Safe Travels Agent
   - Click the **Overview** tab.
   - Click **+ Add knowledge**.
     
   ![Agent Configuration](../media/ex1-travel-g10.png)

1. Upload a knowledge file

   - Click **Upload file** (or **select to browse**) and choose **Travel Policy.docx**.
   - Confirm it appears under **File name** as **Travel Policy.docx**.
   - Click **Add to agent**.

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
   ![Travel Destination Query](../media/ex1-travel-g16.png)

   > **Expected Response:** The agent should provide comprehensive passport application information from its built-in travel knowledge base.
   
   ![Additional Travel Testing](../media/ex1-travel-g17.png)
   
1. Test another travel-related query to validate the agent's knowledge. Ask about travel Policy:

   ```
   What is our company travel policy?
   ```
   ![Business Travel Query](../media/ex1-travel-g18.png)
   
1. Continue testing with additional travel scenarios to ensure the agent responds appropriately to various travel-related questions.

   > **Knowledge Integration:** The agent leverages its built-in travel knowledge to provide helpful responses across various travel scenarios.

## Task 4: Publish and Deploy Agent to Microsoft Teams

In this task, you will publish your Safe Travels agent and deploy it to Microsoft Teams, making it accessible to your organization's employees.

1. After testing, click the **Publish** button in the top-right corner of the agent interface to begin the publishing process.

   ![Navigate to Channels](../media/ex1-travel-g21.png)

1. In the publish dialog, review the publishing details and click **Publish** to confirm and publish your agent.

   ![Open Agent Chat](../media/ex1-travel-g27.png)

   > **Publishing Process:** The agent will be packaged and made available for channel deployment. This process may take a few moments to complete.

1. Open a new browser tab and navigate to [https://teams.microsoft.com/v2/](https://teams.microsoft.com/v2/). 

1. If you see a "Get to know Teams" welcome screen, click **Get Started** to proceed.

   ![Configure Teams Channel](../media/ex1-travel-g22.png)

1. If prompted with a Teams mobile app QR code popup, click the **X** button to close it and continue.

   ![Configure Teams Channel](../media/ex1-travel-g23.png)

1. If prompted to sign in, enter your **email address (1)** and click **Next (2)**.

   - **Email/Username:** <inject key="AzureAdUserEmail"></inject>

   ![Microsoft Sign In](../media/ex1-travel-g24.png)


1. Enter the **Temporary Access Pass (1)** and click **Sign in (2)**.

   - **Temporary Access Pass:** <inject key="AzureAdUserPassword"></inject>

   ![Open in Teams](../media/ex1-travel-g25.png)

1. When prompted to stay signed in, click **Yes** to continue.

   ![Add Agent to Teams](../media/ex1-travel-g26.png)

1. Once published successfully, navigate to the **Channels** section to configure deployment channels for your agent.

   ![Open Agent Chat](../media/ex1-travel-g28.png)

 - In the Channels interface, you'll see available deployment options. Select **Microsoft Teams** to deploy your agent to Teams.

   ![Agent Response in Teams](../media/ex1-travel-g29.png)

   > **Channel Benefits:** Deploying to Microsoft Teams provides users access through their familiar collaboration environment, increasing adoption and usage.

1. If prompted to download the Teams desktop app, click **Use the web app instead** to continue using Teams in your browser.

   ![Agent Response in Teams](../media/ex1-travel-g34.png)

1. In the Safe Travels Agent dialog, review the agent information and click **Add** to install the agent in your Teams environment.

   ![Add Agent to Teams](../media/ex1-travel-g35.png)

1. After successful installation, you'll see a confirmation message. Click **Open** to start using your Safe Travels Agent immediately.

   ![Agent Added Successfully](../media/ex1-travel-g36.png)

1. The Safe Travels Agent chat interface will open. Type your first message in the text box (1) and click the **Send** button (2) to test the agent.

   ![Agent Added Successfully](../media/ex1-travel-g39.png)

1. The Safe Travels Agent chat interface will open. Type your first message in the text box (1) and click the **Send** button (2) to test the agent.

   ![Agent Added Successfully](../media/ex1-travel-g40.png)

## Summary

Excellent work! In just 30 minutes, you've successfully:

- Set up a Power Platform environment for agent development
- Created a working Safe Travels agent using Microsoft's template
- Tested the agent's travel assistance capabilities with real queries
- Published and deployed the agent to Microsoft Teams for your organization

Your Safe Travels agent is now live and ready to help employees with travel questions, passport information, and destination guidance. You've experienced the power of low-code AI development - creating enterprise-ready conversational agents without any programming.

**What's Next:** In Exercise 2, you'll enhance your agent with custom business processes and explore multi-agent orchestration capabilities.

### You have successfully completed Exercise 1. Click **Next >>** to continue to Exercise 2.