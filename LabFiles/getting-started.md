# Getting Started: Build and Enhance a Safe Travels Agent with Multi-Agent Orchestration

### Overall Estimated Duration: 1 Hour

## Overview

Welcome to your **Build and Enhance a Safe Travels Agent with Multi-Agent Orchestration** lab! In this focused hands-on experience, you will learn to build intelligent conversational agents using Microsoft Copilot Studio and explore cutting-edge multi-agent orchestration concepts.

Starting with Microsoft's Safe Travels agent template, you'll create and customize an AI agent that provides comprehensive travel assistance to employees, then enhance it with sophisticated business process automation and multi-agent capabilities. This practical lab is designed to be completed in exactly 60 minutes, focusing on the most essential skills: agent creation, Teams integration, and multi-agent orchestration.

You'll get hands-on experience with Microsoft's latest AI technologies while building something genuinely useful for business scenarios. By the end, you'll have a working travel assistant agent deployed to Teams, plus understand how specialized agents can work together to solve complex enterprise problems.

## Objectives

Learn essential AI agent development using Microsoft Copilot Studio in just 1 hour. By the end of this lab, you will be able to:

- **Create and Deploy AI Agents:** Build a working Safe Travels agent from template, customize it with knowledge sources, and successfully publish it to Microsoft Teams for real-world use.

- **Integrate with Business Processes:** Create sophisticated Agent Flows that automate travel approval requests and post them to Teams channels, demonstrating practical business automation.

- **Master Multi-Agent Concepts:** Experience how specialized agents can work together by adding a Leave Manager agent and seeing multi-agent orchestration in action.

- **Deploy to Enterprise Platforms:** Successfully publish your agents to Microsoft Teams and Microsoft 365 Copilot, making them accessible to end users in familiar environments.

## Prerequisites

- **Microsoft 365 Admin Tenant Credentials** with appropriate permissions for Copilot Studio and Teams administration
- **Access to Microsoft Copilot Studio** environment with agent creation and publishing permissions
- **Microsoft Teams** access for testing and deployment of published agents
- **Basic understanding** of conversational AI concepts and Microsoft 365 collaboration tools
- **Familiarity with business process automation** and enterprise workflow requirements

## Architecture Overview

You'll complete a focused two-exercise journey that delivers maximum value in 60 minutes:

1. **Safe Travels Agent Creation & Teams Deployment (30 mins):** Build and customize the Safe Travels agent from template, test its capabilities, and publish to Teams for immediate use by employees.

2. **Agent Flows & Multi-Agent Orchestration (30 mins):** Create sophisticated travel approval flows, set up multi-agent orchestration with a Leave Manager agent, and see how agents can work together to handle complex requests.

## Architecture Components

- **Microsoft Copilot Studio:** The primary development environment for creating, customizing, and managing AI agents, providing visual design tools, integration capabilities, and publishing options for enterprise-wide deployment.

- **Safe Travels Agent:** A Business-to-Employee (B2E) conversational agent designed to provide comprehensive travel assistance, including destination information, travel policies, approval workflows, and integration with company-specific knowledge sources.

- **Agent Flows & Power Platform Integration:** Sophisticated workflow automation capabilities that enable agents to perform complex business processes, integrate with external systems, send notifications to Teams channels, and maintain state across multi-step interactions.

- **Leave Manager Agent:** A specialized agent focused on employee leave management, including leave balance tracking, policy information, and approval workflows, demonstrating how multiple agents can serve different business functions.

- **Multi-Agent Orchestration:** Advanced AI scenario where multiple specialized agents collaborate automatically, delegate tasks based on user intent, and provide seamless user experiences across different business domains and use cases.

- **Microsoft Teams & Microsoft 365 Integration:** Enterprise-grade deployment and integration capabilities that make custom agents accessible across the Microsoft 365 ecosystem, providing consistent user experiences and centralized management.

## Getting Started with the Lab

Welcome to your **Safe Travels Agent and Multi-Agent Orchestration** lab! We've prepared a seamless environment for you to explore and learn how to build, configure, and test intelligent travel assistance agents. This lab will guide you through agent creation, business process automation, and multi-agent orchestration to deliver a comprehensive and efficient experience. Let's begin by making the most of this workshop!

### Accessing Your Lab Environment

Once you're ready to dive in, your virtual machine and Lab guide will be right at your fingertips within your web browser.

![](../media/gs-leave-1.png)

### Exploring Your Lab Resources

To get a better understanding of your Lab resources and credentials, navigate to the Environment tab.

![](../media/gs-leave-2.png)

### Utilizing the Split Window Feature

For convenience, you can open the Lab guide in a separate window by selecting the Split Window button from the Top right corner

![](../media/gs-leave-3.png)

### Managing Your Virtual Machine

From the **Resources (1)** tab, you can easily **start, stop, restart, or connect (2)** to your virtual machine—your experience is in your hands!

![](../media/gs-leave-4.png)

## Let's Get Started with Microsoft Copilot Studio

1. In the JumpVM, click on **Microsoft Edge** shortcut of Microsoft Edge browser which is created on desktop.

   ![](../media/gs-leave-5.png)

1. Open a new browser tab and navigate to [https://copilotstudio.microsoft.com/](https://copilotstudio.microsoft.com/) (Microsoft Copilot Studio).

   >Note: Since you are working within a VM, please copy the above link and open it in the browser inside the VM.

1. On the **Sign into Microsoft** tab, you will see the login screen. Enter the provided email or username, and click **Next** to proceed.

   - Email/Username: <inject key="AzureAdUserEmail"></inject>

     ![](../media/gs-2.png)

1. Now, enter the following password and click on **Sign in**.

   - Password: <inject key="AzureAdUserPassword"></inject>

     ![](../media/gs-3.png)

     >**Note:** If you see the Action Required dialog box, then select Ask Later option.
     
1. If you see the pop-up **Stay Signed in?**, click **No**.

   ![](../media/gs-4.png)

1. If the **Welcome to Microsoft Copilot Studio** pop-up appears, leave the default country/region selection and click **Get started**.

   ![](../media/cor-mn-e5-g-6.png)

1. You have now successfully logged in to Microsoft Copilot Studio. Keep the portal open, as you will be using it throughout the lab exercises.

   ![](../media/gs-5.png)

1. Also open Microsoft Teams by navigating to [https://teams.microsoft.com/](https://teams.microsoft.com/) in a new browser tab and signing in with the same credentials. You'll need Teams access for testing and deploying your agents.

   >**Important:** Ensure both Microsoft Copilot Studio and Microsoft Teams are accessible before proceeding to Exercise 1.

## Support Contact

The CloudLabs support team is available 24/7, 365 days a year, via email and live chat to ensure seamless assistance at any time. We offer dedicated support channels tailored specifically for both learners and instructors, ensuring that all your needs are promptly and efficiently addressed.Learner Support Contacts:

- Email Support: cloudlabs-support@spektrasystems.com
- Live Chat Support: https://cloudlabs.ai/labs-support

Now, click on the **Next** from lower right corner to move on next page.

   ![](../media/a-gs-g1.png)

## Happy Learning!!