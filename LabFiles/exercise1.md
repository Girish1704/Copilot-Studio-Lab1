# Exercise 1: Create and Deploy Safe Travels Agent

### Estimated Duration: 30 Minutes

## Overview

In this exercise, you will create your first AI agent using Microsoft Copilot Studio's Safe Travels template. You'll learn the fundamentals of agent creation, test conversational AI capabilities, and successfully publish your agent to Microsoft Teams for real-world enterprise use. This exercise establishes your foundation in modern AI agent development and enterprise deployment.

The Safe Travels agent is a Business-to-Employee (B2E) conversational agent designed to provide comprehensive travel assistance to company employees. You'll customize this agent with company-specific knowledge and see how it can help employees with travel planning, policy questions, and destination information. By the end of this exercise, you'll have a working travel assistant deployed to Teams that employees can use immediately.

## Objectives

You will be able to complete the following tasks:

- Task 1: Set up Microsoft Copilot Studio environment and create Safe Travels agent from template
- Task 2: Test and customize the agent with company-specific knowledge sources
- Task 3: Publish the agent to Microsoft Teams for enterprise deployment

## Prerequisites

- Completion of **Getting Started** section with proper environment setup
- **Microsoft 365 Admin Tenant Credentials** with Copilot Studio permissions
- **Access to Microsoft Copilot Studio** environment with agent creation capabilities
- **Microsoft Teams** access for testing and deployment
- **Understanding of conversational AI concepts** and business process automation

## Task 1: Create Safe Travels Agent from Template

In this task, you'll set up your Copilot Studio environment and create your first AI agent using Microsoft's pre-built Safe Travels template.

### Step 1: Access Copilot Studio Environment

1. From a browser, navigate to [https://copilotstudio.microsoft.com/](https://copilotstudio.microsoft.com/).

1. The **Start free trial** page opens. Select your country and click **Start free trial**.

   ![Safe Travels Template](../media/image1.png)

1. Select the **Dev One** environment to ensure proper workspace isolation.

   ![Environment Selection](../media/image2.png)

   ![Environment Confirmation](../media/image3.png)

   > **Important:** If Copilot Studio does not show the Environment selection option, follow these steps:
   > 1. Open [https://admin.powerplatform.microsoft.com/](https://admin.powerplatform.microsoft.com/)
   > 2. Select **Manage** > **Environments** and note the **EnvironmentID** value
   > 3. Navigate back to Copilot Studio using: `https://copilotstudio.microsoft.com/environments/<EnvironmentID>`

### Step 2: Create Agent from Safe Travels Template

1. Select **+ Create** from the left navigation pane to begin agent creation.

   ![Create New Agent](../media/image6.png)

1. Under **Start with an agent template**, select **Safe Travels** to use the pre-built template.

   ![Safe Travels Template Selection](../media/image7.png)

1. Review the Safe Travels template description. This template creates an agent designed to provide comprehensive travel assistance to company employees.

   ![Template Overview](../media/image8.png)

1. Browse through the setup page. Under **Knowledge**, you'll find that **US Travel Website** is already configured as a knowledge source. This can be customized later for your organization's specific needs.

   ![Knowledge Sources](../media/image9.png)

1. Select **Create** to generate the Safe Travels agent using the default template configuration.

   ![Create Agent](../media/image10.png)

1. The agent is successfully created and opens automatically, displaying the **Overview** page with agent configuration and capabilities.

   ![Agent Created Successfully](../media/image11.png)

## Task 2: Test and Customize the Agent

In this task, you'll test the agent's conversational capabilities and add company-specific knowledge to enhance its usefulness for your organization.

### Step 1: Test Basic Agent Functionality

1. Open the **Test** pane by clicking the Test icon in the top-right corner.

   ![Open Test Pane](../media/image12.png)

1. In the Test pane, enter **How to apply for passport?** and click **Send** to test the agent's knowledge capabilities.

   ![Test Basic Query](../media/image12.png)

1. Review the agent's response. Notice how it provides detailed information about passport applications using its built-in knowledge source.

   ![Agent Response](../media/image13.png)

### Step 2: Add Company-Specific Knowledge

1. From the **Overview** page, scroll down and select **+ Add knowledge** under the **Knowledge** section.

   ![Add Knowledge](../media/image30.png)

1. Click **select to browse** to upload company-specific documents.

   ![Browse Files](../media/image31.png)

1. From **C:\Labfiles\Lab Files** folder, select **Travel Policy.docx** and click **Open**.

   ![Select Travel Policy](../media/image32.png)

1. Click **Add to agent** to integrate the travel policy document into the agent's knowledge base.

   ![Add Document](../media/image33.png)

   ![Confirm Addition](../media/image34.png)

1. Wait for the knowledge source to process. The status will change from **In progress** to **Ready** when complete.

   ![Processing Status](../media/image35.png)

   ![Ready Status](../media/image36.png)

### Step 3: Test Enhanced Agent Capabilities

1. In the **Test** pane, enter **Need travel approval** to test how the agent handles company-specific travel policies.

   ![Test Travel Approval](../media/image28.png)

1. Review the agent's response. Notice how it now provides company-specific guidance based on the uploaded Travel Policy document.

   ![Enhanced Response](../media/image29.png)

## Task 3: Publish Agent to Microsoft Teams

In this task, you'll publish your Safe Travels agent to Microsoft Teams, making it available for employees across your organization.

### Step 1: Publish the Agent

1. Select **Publish** from the top-right corner of the agent interface.

   ![Publish Agent](../media/image15.png)

1. In the confirmation dialog, select **Publish** to make the agent available for deployment.

   ![Confirm Publish](../media/image16.png)

### Step 2: Configure Teams Channel

1. Select **Channels** from the top navigation bar to access deployment options.

   ![Access Channels](../media/image17.png)

1. Select **Teams and Microsoft 365 Copilot** from the available channel options.

   ![Select Teams Channel](../media/image18.png)

1. Select **Add channel** to begin the Teams integration process.

   ![Add Channel](../media/image19.png)

1. Click **See agent in Teams** to open the agent in Microsoft Teams for testing and deployment.

   ![View in Teams](../media/image20.png)

### Step 3: Deploy and Test in Teams

1. Microsoft Teams opens with your Safe Travels agent. Select **Add** to add the agent to your Teams environment.

   ![Add to Teams](../media/image21.png)

   ![Confirm Addition](../media/image22.png)

1. Once added, select **Open** to launch the agent in Teams.

   ![Open Agent](../media/image23.png)

1. Test the agent functionality directly within Microsoft Teams to ensure proper deployment.

   ![Test in Teams](../media/image24.png)

1. Return to Copilot Studio and close the Teams and Microsoft 365 Copilot channel configuration window.

   ![Close Configuration](../media/image25.png)

## Notes

- **Agent Templates** provide pre-configured starting points with built-in knowledge and conversation flows
- **Knowledge Sources** can be customized with company-specific documents, policies, and information
- **Teams Integration** makes agents accessible across the Microsoft 365 ecosystem
- **Testing** is crucial before deployment to ensure agent responses meet business requirements
- **Environment Management** ensures proper isolation and governance for enterprise deployments

## Summary

In this exercise, you successfully created your first AI agent using Microsoft Copilot Studio's Safe Travels template. You learned how to set up the Copilot Studio environment, customize agents with company-specific knowledge sources, and deploy agents to Microsoft Teams for enterprise use.

Key accomplishments include:
- Created a functional Safe Travels agent from Microsoft's pre-built template
- Enhanced the agent with custom knowledge sources (Travel Policy document)
- Successfully tested agent capabilities and conversational responses
- Published and deployed the agent to Microsoft Teams for organization-wide access
- Established foundation skills for AI agent development and enterprise deployment

You now have a working travel assistant agent that employees can use to get travel information, policy guidance, and assistance with travel-related questions. This agent serves as the foundation for the advanced multi-agent orchestration capabilities you'll explore in Exercise 2.