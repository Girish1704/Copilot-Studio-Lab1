# Exercise 3: Build Leave Manager Agent and Implement Multi-Agent Orchestration

### Estimated Duration: 20 Minutes

## Overview

In this advanced exercise, you will explore the cutting-edge world of multi-agent orchestration by building a specialized Leave Manager agent and integrating it with your existing Safe Travels agent. This exercise demonstrates how organizations can create sophisticated AI ecosystems where multiple specialized agents work collaboratively to provide comprehensive business solutions that span different domains and workflows.

You'll learn to design agents with specific expertise areas, integrate custom knowledge sources for domain-specific information, and configure intelligent task delegation between agents. This multi-agent approach represents the future of enterprise AI, where rather than relying on a single agent to handle everything, organizations deploy specialized agents that can collaborate automatically to solve complex, multi-faceted business challenges.

The Leave Manager agent will provide comprehensive leave management capabilities including balance tracking, policy information, and approval workflows, while seamlessly integrating with your Safe Travels agent to provide holistic employee assistance that considers both travel and leave requirements.

## Objectives

You will be able to complete the following tasks:

- Task 1: Create specialized Leave Manager agent with custom knowledge integration
- Task 2: Configure leave balance tracking and policy management capabilities  
- Task 3: Build custom Topics for leave management workflows
- Task 4: Implement multi-agent orchestration with the Safe Travels agent
- Task 5: Test collaborative agent scenarios and validate intelligent task delegation

## Prerequisites

- Completed **Exercise 1** and **Exercise 2** with functional Safe Travels agent
- Understanding of multi-agent systems and collaborative AI concepts
- Access to sample leave management data or policies for knowledge integration
- **Safe Travels agent** published and operational in your environment

## Task 1: Create Leave Manager Agent with Knowledge Integration

In this task, you will build a specialized Leave Manager agent from scratch, demonstrating how to create purpose-built agents for specific business domains. This agent will focus exclusively on employee leave management, policies, and related workflows.

1. Navigate to the **Copilot Studio** home page and select **Agents** from the left navigation.

   ![Agents Navigation](../media/agents-navigation-home.png)

1. Click **+ New agent** to create your specialized Leave Manager agent.

   ![Create New Agent](../media/create-new-leave-agent.png)

1. Select the **Configure** tab to create a custom agent rather than using a template.

   ![Configure Custom Agent](../media/configure-custom-agent.png)

1. Configure your Leave Manager agent with the following details:
   - **Name:** `Leave Manager Agent`
   - **Description:** `This agent is to track the leaves of all the employees, their leave balance and leave history to approve or reject any new leave requests.`
   - **Instructions:** `Track the leaves of employees. Track their leave balance. Apply/Reject leaves based on their balance.`

   ![Leave Agent Configuration](../media/leave-agent-configuration.png)

   > **Agent Specialization:** By creating focused agents with specific instructions, you ensure they develop expertise in their designated domain while maintaining clear boundaries and responsibilities.

1. Click **Create** to generate your Leave Manager agent.

   ![Create Leave Agent](../media/create-leave-agent-button.png)

1. Once the agent is created, navigate to the **Knowledge** section on the Overview page and click **+ Add knowledge**.

   ![Add Leave Knowledge](../media/add-leave-knowledge.png)

1. Click **select to browse** to upload leave management documentation.

   ![Browse Leave Documents](../media/browse-leave-documents.png)

   > **Note:** In a real scenario, you would upload company-specific leave policy documents, employee leave balance spreadsheets, or leave management system exports. For this lab, we'll simulate this process.

1. If you have access to leave management documents or sample files, upload them here. Otherwise, you can proceed with creating knowledge-based responses through topics.

   ![Upload Leave Files](../media/upload-leave-files.png)

1. Wait for any uploaded knowledge sources to process completely, showing **Ready** status before proceeding.

   ![Knowledge Processing Complete](../media/knowledge-processing-complete.png)

   > **Knowledge Integration:** Properly processed knowledge sources enable your agent to provide accurate, policy-compliant responses to leave-related inquiries.

## Task 2: Create Leave Balance Checker Topic

In this task, you will create a sophisticated topic that enables your Leave Manager agent to check employee leave balances and provide detailed leave information based on employee identification.

1. Navigate to the **Topics** section from the top navigation of your Leave Manager agent.

   ![Topics Navigation Leave](../media/topics-navigation-leave.png)

1. Click **+ Add a topic** and select **Add from description with Copilot**.

   ![Add Leave Topic](../media/add-leave-topic.png)

1. Configure your leave balance checking topic:
   - **Name:** `Leave Balance Checker`
   - **Create a topic to:** `Get the Employee ID from the user and check and reply with the leave balance based on the tracker added as knowledge source`

   ![Leave Topic Configuration](../media/leave-topic-configuration.png)

1. Click **Create** to generate your leave balance checking topic.

   ![Create Leave Topic](../media/create-leave-topic-button.png)

1. Review the generated topic structure to ensure it includes:
   - Employee ID collection node
   - Leave balance retrieval logic
   - Response formatting for user communication

   ![Leave Topic Structure](../media/leave-topic-structure.png)

1. If necessary, refine the topic by removing any extraneous nodes and ensuring a clean workflow from ID collection to balance response.

   ![Refine Leave Topic](../media/refine-leave-topic.png)

1. Click **Save** to preserve your leave balance checker topic.

   ![Save Leave Topic](../media/save-leave-topic.png)

## Task 3: Test Leave Manager Agent Functionality

In this task, you will validate your Leave Manager agent's capabilities by testing its leave balance checking functionality and ensuring it provides appropriate responses based on employee data.

1. Open the **Test** panel for your Leave Manager agent.

   ![Test Leave Agent](../media/test-leave-agent.png)

1. Initiate a leave balance inquiry:

   ```
   Check Leave balance
   ```

   ![Leave Balance Query](../media/leave-balance-query.png)

1. When prompted for Employee ID, provide a test value:

   ```
   1234
   ```

   ![Provide Employee ID](../media/provide-employee-id.png)

1. Review the agent's response to ensure it provides relevant leave balance information.

   ![Leave Balance Response](../media/leave-balance-response.png)

   > **Response Quality:** The agent should provide contextual leave information based on your knowledge sources or demonstrate appropriate handling of leave balance inquiries.

1. Test additional leave-related scenarios to validate the agent's knowledge breadth:

   ```
   What is the leave policy for sick days?
   ```

   ![Leave Policy Query](../media/leave-policy-query.png)

1. Verify the agent maintains its focus on leave management topics and provides domain-appropriate responses.

   ![Leave Policy Response](../media/leave-policy-response.png)

## Task 4: Publish Leave Manager Agent

In this task, you will publish your Leave Manager agent to make it available for multi-agent orchestration scenarios with your Safe Travels agent.

1. Click **Publish** to make your Leave Manager agent available for integration.

   ![Publish Leave Agent](../media/publish-leave-agent.png)

1. Wait for the publishing process to complete successfully.

   ![Leave Agent Published](../media/leave-agent-published.png)

   > **Publishing Requirement:** Agents must be published before they can be integrated into multi-agent orchestration scenarios.

## Task 5: Implement Multi-Agent Orchestration

In this task, you will configure your Safe Travels agent to automatically collaborate with the Leave Manager agent, creating an intelligent system where agents delegate tasks based on user intent and expertise areas.

1. Navigate back to your **Safe Travels** agent.

   ![Return to Safe Travels](../media/return-safe-travels.png)

1. First, test your Safe Travels agent's current response to leave-related queries to establish a baseline:

   ```
   Check Leave balance
   ```

   ![Test Safe Travels Leave](../media/test-safe-travels-leave.png)

1. Observe that the Safe Travels agent provides general information but lacks specific leave balance data.

   ![Safe Travels Leave Response](../media/safe-travels-leave-response.png)

   > **Before Orchestration:** The Safe Travels agent can only provide general guidance without access to specialized leave management capabilities.

1. Navigate to the **Agents** tab from the top navigation to configure multi-agent orchestration.

   ![Agents Tab Navigation](../media/agents-tab-navigation.png)

1. Click **+ Add** to integrate another agent into your Safe Travels agent.

   ![Add Agent Integration](../media/add-agent-integration.png)

1. Under **Choose how do you want to extend your agent**, select **Copilot Studio**.

   ![Select Copilot Studio](../media/select-copilot-studio.png)

1. From the available agents list, select your **Leave Manager Agent**.

   ![Select Leave Manager](../media/select-leave-manager.png)

   > **Agent Selection:** Only published agents will appear in the integration list. Ensure your Leave Manager agent is fully published before proceeding.

1. Click **Add agent** to establish the multi-agent connection.

   ![Add Leave Manager to Safe](../media/add-leave-manager-safe.png)

1. Confirm the agent integration is successful.

   ![Agent Integration Success](../media/agent-integration-success.png)

1. Wait for the integration to process completely, then click **Publish** to update your Safe Travels agent with multi-agent capabilities.

   ![Publish Multi-Agent](../media/publish-multi-agent.png)

## Task 6: Test Multi-Agent Orchestration

In this task, you will validate that your multi-agent orchestration is working correctly by testing scenarios where the Safe Travels agent automatically delegates leave-related queries to the Leave Manager agent.

1. Allow a few minutes for the multi-agent integration to fully activate after publishing.

1. In the Safe Travels agent test panel, initiate a leave balance query:

   ```
   Check Leave balance
   ```

   ![Test Multi-Agent Leave](../media/test-multi-agent-leave.png)

1. Observe that the Safe Travels agent now automatically accesses the Leave Manager agent to handle the request.

   ![Multi-Agent Delegation](../media/multi-agent-delegation.png)

   > **Intelligent Delegation:** The system automatically routes leave-related queries to the specialized Leave Manager agent while maintaining the conversational context.

1. When prompted by the Leave Manager agent (via the Safe Travels interface), provide an Employee ID:

   ```
   1234
   ```

   ![Multi-Agent Employee ID](../media/multi-agent-employee-id.png)

1. Verify that you receive specialized leave balance information through the Safe Travels agent interface.

   ![Multi-Agent Leave Response](../media/multi-agent-leave-response.png)

   > **Seamless Integration:** Users interact with a single interface while benefiting from multiple specialized agents working collaboratively behind the scenes.

1. Test the system with travel-related queries to ensure the Safe Travels agent continues to handle its primary domain effectively:

   ```
   I need travel information for New York
   ```

   ![Test Travel After Integration](../media/test-travel-after-integration.png)

1. Confirm that travel queries remain with the Safe Travels agent while leave queries are automatically delegated.

   ![Travel Response Multi-Agent](../media/travel-response-multi-agent.png)

## Task 7: Advanced Multi-Agent Scenarios

In this task, you will explore advanced multi-agent scenarios where users can seamlessly transition between travel planning and leave management within a single conversation.

1. Test a complex scenario that might require both agents:

   ```
   I'm planning a business trip to Seattle next month. Do I have enough vacation days available?
   ```

   ![Complex Multi-Agent Query](../media/complex-multi-agent-query.png)

1. Observe how the system handles the dual-domain request, potentially engaging both agents or routing appropriately based on the primary intent.

   ![Complex Query Response](../media/complex-query-response.png)

1. Test follow-up scenarios to validate conversation context maintenance:

   ```
   What about my sick leave balance?
   ```

   ![Follow-up Leave Query](../media/followup-leave-query.png)

1. Verify that the system maintains appropriate context and continues to leverage the Leave Manager agent for specialized queries.

   ![Follow-up Response](../media/followup-response.png)

   > **Context Preservation:** Advanced multi-agent systems maintain conversation context across agent delegations, providing seamless user experiences.

## Summary

In this exercise, you successfully implemented advanced multi-agent orchestration, creating a sophisticated AI ecosystem where specialized agents collaborate automatically to provide comprehensive business solutions. You learned how to design domain-specific agents, integrate them with existing systems, and configure intelligent task delegation based on user intent and agent expertise.

Key accomplishments include:
- ✅ Created specialized Leave Manager agent with domain-specific capabilities
- ✅ Integrated custom knowledge sources for leave management functionality
- ✅ Built sophisticated topics for leave balance checking and policy management
- ✅ Implemented seamless multi-agent orchestration between Safe Travels and Leave Manager agents
- ✅ Validated intelligent task delegation and context preservation across agent interactions
- ✅ Tested complex scenarios requiring collaboration between multiple specialized agents

Your multi-agent system now demonstrates the future of enterprise AI, where specialized agents work collaboratively to solve complex business challenges while maintaining seamless user experiences. This approach enables organizations to build comprehensive AI solutions that scale across multiple domains and business processes while preserving the benefits of specialized expertise and focused functionality.

The skills and concepts you've mastered in this exercise provide the foundation for building even more sophisticated multi-agent systems that can handle complex enterprise scenarios spanning multiple departments, systems, and business processes.

### You have successfully completed this exercise and the entire lab series!