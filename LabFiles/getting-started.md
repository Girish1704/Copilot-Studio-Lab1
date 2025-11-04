# Build and Enhance a Safe Travels Agent with Multi-Agent Orchestration

### Overall Estimated Duration: 1 Hour

## Overview

In this focused hands-on lab, you will learn to build intelligent conversational agents using Microsoft Copilot Studio and explore multi-agent orchestration concepts. Starting with the Safe Travels agent template, you'll create and customize an AI agent that provides travel assistance to employees, then enhance it with basic business process automation and multi-agent capabilities.

This practical lab is designed to be completed in exactly 60 minutes, focusing on the most essential skills: agent creation, Teams integration, and a taste of multi-agent orchestration. You'll get hands-on experience with Microsoft's latest AI technologies while building something genuinely useful for business scenarios. By the end, you'll have a working travel assistant agent deployed to Teams, plus understand how agents can work together to solve complex problems.

## Objective

Learn essential AI agent development using Microsoft Copilot Studio in just 1 hour. By the end of this lab, you will be able to:

- **Create and Deploy AI Agents:** Build a working Safe Travels agent from template, customize it with knowledge sources, and successfully publish it to Microsoft Teams for real-world use.

- **Integrate with Business Processes:** Create a basic Agent Flow that automates travel approval requests and posts them to Teams channels, demonstrating practical business automation.

- **Understand Multi-Agent Concepts:** Experience how specialized agents can work together by adding a simple Leave Manager agent and seeing multi-agent orchestration in action.

- **Deploy to Enterprise Platforms:** Successfully publish your agents to Microsoft Teams and Microsoft 365 Copilot, making them accessible to end users in familiar environments.

## Pre-requisites

- **Microsoft 365 Admin Tenant Credentials** with appropriate permissions for Copilot Studio and Teams administration
- **Access to Microsoft Copilot Studio** environment with agent creation and publishing permissions
- **Microsoft Teams** access for testing and deployment of published agents
- **Basic understanding** of conversational AI concepts and Microsoft 365 collaboration tools
- **Familiarity with business process automation** and enterprise workflow requirements

## Architecture

You'll complete a focused two-exercise journey that delivers maximum value in 60 minutes:

1. **Safe Travels Agent Creation & Teams Deployment (30 mins):** Build and customize the Safe Travels agent from template, test its capabilities, and publish to Teams for immediate use by employees.

2. **Agent Flows & Multi-Agent Basics (30 mins):** Create a simple travel approval flow, set up basic multi-agent orchestration with a Leave Manager agent, and see how agents can work together to handle complex requests.

## Architecture Diagram

```
┌─────────────────────────────────────────────────────────────────────────────────┐
│                            Microsoft 365 Ecosystem                              │
├─────────────────────────────────────────────────────────────────────────────────┤
│  ┌──────────────────┐    ┌──────────────────┐    ┌──────────────────┐         │
│  │  Microsoft Teams │    │ Microsoft 365    │    │   SharePoint     │         │
│  │   Integration    │◄──►│   Copilot        │◄──►│   Knowledge      │         │
│  └──────────────────┘    └──────────────────┘    └──────────────────┘         │
├─────────────────────────────────────────────────────────────────────────────────┤
│                          Microsoft Copilot Studio                              │
├─────────────────────────────────────────────────────────────────────────────────┤
│  ┌──────────────────┐    ┌──────────────────┐    ┌──────────────────┐         │
│  │  Safe Travels    │◄──►│   Agent Flows    │◄──►│ Leave Manager    │         │
│  │     Agent        │    │  & Automation    │    │     Agent        │         │
│  └──────────────────┘    └──────────────────┘    └──────────────────┘         │
├─────────────────────────────────────────────────────────────────────────────────┤
│                     Multi-Agent Orchestration                                  │
└─────────────────────────────────────────────────────────────────────────────────┘
```

## Explanation of Components

- **Microsoft Copilot Studio:** The primary development environment for creating, customizing, and managing AI agents, providing visual design tools, integration capabilities, and publishing options for enterprise-wide deployment.

- **Safe Travels Agent:** A Business-to-Employee (B2E) conversational agent designed to provide comprehensive travel assistance, including destination information, travel policies, approval workflows, and integration with company-specific knowledge sources.

- **Agent Flows & Power Platform Integration:** Sophisticated workflow automation capabilities that enable agents to perform complex business processes, integrate with external systems, send notifications to Teams channels, and maintain state across multi-step interactions.

- **Leave Manager Agent:** A specialized agent focused on employee leave management, including leave balance tracking, policy information, and approval workflows, demonstrating how multiple agents can serve different business functions.

- **Multi-Agent Orchestration:** Advanced AI scenario where multiple specialized agents collaborate automatically, delegate tasks based on user intent, and provide seamless user experiences across different business domains and use cases.

- **Microsoft Teams & Microsoft 365 Integration:** Enterprise-grade deployment and integration capabilities that make custom agents accessible across the Microsoft 365 ecosystem, providing consistent user experiences and centralized management.

## Getting Started with the Lab

Once you're ready to dive in, your virtual machine and lab guide will be right at your fingertips within your web browser.

![](../media/copilot-studio-welcome.png)

## Virtual Machine & Lab Guide

Your virtual machine is your workhorse throughout the workshop. The lab guide is your roadmap to success.

## Exploring Your Lab Resources

To get a better understanding of your lab resources and credentials, navigate to the **Environment** tab.

![](../media/environment-tab.png)

## Utilizing the Split Window Feature

For convenience, you can open the lab guide in a separate window by selecting the **Split Window** button from the top right corner.

![](../media/split-window.png)

## Managing Your Virtual Machine

On the **Resources (1)** tab, use the **Action buttons (2)** next to your VM. Feel free to **start**, **stop**, or **restart** your Virtual Machine as needed. Your experience is in your hands!

![](../media/vm-management.png)

## Lab Guide Zoom In/Zoom Out

To adjust the zoom level for the environment page, click the **A↕ : 100%** icon located next to the timer in the lab environment.

![](../media/zoom-controls.png)

## Let's Get Started with Microsoft Copilot Studio

1. On the Lab VM, open **Microsoft Edge** browser from the taskbar.

   ![](../media/edge-browser.png)

1. Navigate to **Microsoft Copilot Studio** by entering the following URL in the address bar:

   ```
   https://copilotstudio.microsoft.com
   ```

   ![](../media/copilot-studio-url.png)

1. Sign in with your provided **Admin tenant credentials** when prompted:

   - **Email/Username:** <inject key="AzureAdUserEmail"></inject>

   ![](../media/login-email.png)

1. Enter the **password** and click **Sign in**.

   - **Password:** <inject key="AzureAdUserPassword"></inject>

   ![](../media/login-password.png)

1. If prompted with **"Stay signed in?"**, select **Yes** to maintain your session throughout the lab.

   ![](../media/stay-signed-in.png)

1. Welcome to **Microsoft Copilot Studio**! You're now ready to build intelligent conversational agents.

   ![](../media/copilot-studio-home.png)

## Support Contact

The CloudLabs support team is available 24/7, 365 days a year, via email and live chat.

**Learner Support Contacts:**
- Email: cloudlabs-support@spektrasystems.com  
- Live Chat: https://cloudlabs.ai/labs-support

Click **Next** at the bottom-right to begin your AI agent development journey!

## Happy Learning!!