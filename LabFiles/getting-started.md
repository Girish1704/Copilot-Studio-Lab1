# Build and Enhance a Safe Travels Agent with Multi-Agent Orchestration

### Overall Estimated Duration: 1 Hour

## Overview

In this comprehensive hands-on lab, you will master the art of building intelligent conversational agents using Microsoft Copilot Studio and implement advanced multi-agent orchestration scenarios. Starting with the Safe Travels agent template, you'll learn to create, customize, and enhance AI agents that provide personalized travel assistance to employees. You'll discover how to integrate external knowledge sources, create sophisticated Agent Flows for business process automation, and build seamless connections between Copilot Studio and Microsoft Teams for enterprise-wide deployment.

The lab progresses from basic agent creation to advanced multi-agent orchestration, where you'll build a Leave Manager agent and configure it to work collaboratively with your Safe Travels agent. This powerful combination demonstrates how multiple specialized agents can work together to provide comprehensive business solutions, showcasing the future of AI-driven workplace automation. Through practical exercises with detailed screenshots and step-by-step guidance, you'll gain hands-on experience with the latest Microsoft AI technologies and enterprise integration capabilities.

## Objective

Master comprehensive AI agent development and multi-agent orchestration using Microsoft Copilot Studio. By the end of this lab, you will be able to:

- **Create and Customize AI Agents:** Build intelligent conversational agents from templates in Copilot Studio, customize them with company-specific knowledge sources, and configure them to meet specific business requirements for employee assistance and automation.

- **Implement Agent Flows and Business Process Integration:** Design and deploy sophisticated Agent Flows that automate business processes, integrate with Microsoft Teams channels, and create seamless workflows for tasks like travel approval requests and employee communications.

- **Deploy Agents Across Microsoft 365 Ecosystem:** Publish and distribute custom agents to Microsoft Teams and Microsoft 365 Copilot, ensuring enterprise-wide accessibility and integration with existing collaboration tools and workflows.

- **Build Multi-Agent Orchestration Systems:** Create specialized agents for different business functions (travel assistance, leave management) and configure them to work collaboratively, demonstrating advanced multi-agent scenarios where agents delegate tasks and share information.

- **Configure Enterprise Integration and Security:** Set up proper environment management, implement secure authentication flows, and establish governance practices for AI agent deployment in enterprise environments.

- **Optimize Agent Performance and User Experience:** Fine-tune agent responses, implement custom topics and knowledge integration, and create intuitive conversational interfaces that provide value to end users.

## Pre-requisites

- **Microsoft 365 Admin Tenant Credentials** with appropriate permissions for Copilot Studio and Teams administration
- **Access to Microsoft Copilot Studio** environment with agent creation and publishing permissions
- **Microsoft Teams** access for testing and deployment of published agents
- **Basic understanding** of conversational AI concepts and Microsoft 365 collaboration tools
- **Familiarity with business process automation** and enterprise workflow requirements

## Architecture

You'll progress through a comprehensive three-exercise journey designed for maximum learning impact:

1. **Safe Travels Agent Creation & Deployment (20 mins):** Build and customize the Safe Travels agent from template, integrate company travel policies, and publish to Teams and Microsoft 365 Copilot for enterprise access.

2. **Agent Flows & Business Process Automation (20 mins):** Create sophisticated Agent Flows for travel approval workflows, integrate with Teams channels for automated notifications, and build custom topics that leverage flow-based automation.

3. **Multi-Agent Orchestration & Advanced Integration (20 mins):** Develop a specialized Leave Manager agent, implement multi-agent collaboration scenarios, and configure intelligent task delegation between agents for complex business processes.

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