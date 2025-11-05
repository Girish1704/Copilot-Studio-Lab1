# Exercise 2: Agent Flows and Multi-Agent Orchestration

### Estimated Duration: 30 Minutes

## Overview

In this exercise, you'll add business process automation to your Safe Travels agent and experience multi-agent orchestration. You'll create a simple Agent Flow for travel approvals and then add a second agent that specializes in leave management. This demonstrates how agents can work together and how businesses can automate processes using conversational AI.

This is where the magic happens - you'll see your agents come alive with real business functionality. By the end, you'll have a travel approval system that posts requests to Teams, plus a multi-agent setup where your Safe Travels agent can automatically hand off leave-related questions to a specialized Leave Manager agent.

## Objectives

You will be able to complete the following tasks:

- Task 1: Create a simple travel approval flow (15 mins)
- Task 2: Build a Leave Manager agent and set up multi-agent orchestration (15 mins)

## Prerequisites

- Completed **Exercise 1** with published Safe Travels agent
- Access to **Microsoft Teams** with team and channel creation permissions
- Understanding of basic workflow concepts and business process automation
- **Safe Travels agent** available in your Copilot Studio environment

## Task 1: Create Simple Travel Approval Flow (15 minutes)

In this task, you'll add a basic business process to your Safe Travels agent by creating a simple flow that can capture travel approval requests. This demonstrates how agents can trigger real business processes.

### Step 1: Quick Teams Setup (3 minutes)

1. Open **Microsoft Teams** and quickly create:
   - **Team name:** `HR Team`
   - **Channel name:** `Travel Approvals`
   - Skip adding members for this lab

   ![Quick Teams Setup](../media/quick-teams-setup.png)

   > **Quick Setup:** We're keeping this simple - just one team and channel for approval notifications.

### Step 2: Create Basic Agent Flow (7 minutes)

1. In **Copilot Studio**, go to your **Safe Travels** agent and select **Flows** from the left menu.

   ![Navigate to Flows](../media/navigate-flows.png)

1. Click **New agent flow** and set up:
   - **Trigger:** "When an agent calls the flow"
   - **Inputs:** Add two inputs:
     - `Employee ID` (Number)
     - `Purpose` (Text)

   ![Basic Flow Setup](../media/basic-flow-setup.png)

### Step 3: Add Teams Integration (5 minutes)

1. Add action: **Teams > Post message in a chat or channel**
2. Configure quickly:
   - **Team:** HR Team
   - **Channel:** Travel Approvals  
   - **Message:** "Travel request from Employee ID: [Employee ID], Purpose: [Purpose]"

   ![Teams Integration](../media/teams-integration-simple.png)

3. Add final action: **Respond to agent** and configure the output:
   - Click **Add an output**
   - **Output Type:** Select `Text`
   - **Name:** Enter `Output`
   - **Value:** Enter `Request submitted`
   - **Description:** Enter `Confirmation message for travel request`

   ![Configure Response Output](../media/configure-response-output.png)

   > **Important:** All fields must be filled to avoid "Invalid parameters" error.

4. **Save draft** first, then **Publish** your flow
5. Name it "Travel Approval Flow" in the Overview tab

   ![Flow Complete](../media/flow-complete.png)

### Step 4: Connect Flow to Safe Travels Agent (5 minutes)

1. Go back to your **Safe Travels** agent and navigate to the **Overview** page.

2. Scroll down and click **Add tool**.

   ![Add Tool](../media/add-tool.png)

3. Go to the **Flow** tab and select your **Travel Approval Flow**.

   ![Select Flow Tool](../media/select-flow-tool.png)

4. Click **Add to agent** to integrate the flow.

   ![Flow Added to Agent](../media/flow-added-agent.png)

5. Now create a topic to use this flow. Go to **Topics** and click **+ Add a topic** > **From blank**.

   ![Add Topic From Blank](../media/add-topic-from-blank.png)

6. Configure the topic details:
   - **Name:** `Travel Approval Request`
   - **Display name:** `Travel Approval Request`

   ![Topic Name Configuration](../media/topic-name-config.png)

7. In the topic designer, you'll see the trigger node. Add trigger phrases like:
   - `I need travel approval`
   - `Travel approval request`
   - `Request travel approval`

   ![Add Trigger Phrases](../media/add-trigger-phrases.png)

8. Add a **Question** node to collect Employee ID:
   - Click **+ Add a node** > **Ask a question**
   - **Question:** `What is your Employee ID?`
   - **Identify:** Choose `Number`
   - **Save response as:** `EmployeeID`

   ![Add Employee ID Question](../media/add-employee-id-question.png)

9. Add another **Question** node to collect Purpose:
   - Click **+ Add a node** > **Ask a question**  
   - **Question:** `What is the purpose of your travel?`
   - **Identify:** Choose `Text`
   - **Save response as:** `Purpose`

   ![Add Purpose Question](../media/add-purpose-question.png)

10. Add the flow action:
    - Click **+ Add a node** > **Call an action** > **Travel Approval Flow**
    - Map the variables:
      - **Employee ID:** Select `EmployeeID` variable
      - **Purpose:** Select `Purpose` variable

    ![Add Flow Action](../media/add-flow-action.png)

11. Add a final message node:
    - Click **+ Add a node** > **Send a message**
    - **Message:** Use the flow output variable `Output`

    ![Add Final Message](../media/add-final-message.png)

12. **Save** and **Publish** your agent.

8. **Test it:** In the test panel, type "I need travel approval" and provide Employee ID: 1234 and Purpose: "Client meeting"

   ![Test Travel Approval](../media/test-travel-approval.png)

## Task 2: Multi-Agent Orchestration Setup (10 minutes)

Now for the exciting part - you'll create a second agent and see how agents can work together automatically!

### Step 1: Create Leave Manager Agent (7 minutes)

1. In Copilot Studio, click **+ New agent** and select **Configure** (not template).

2. Set up your Leave Manager agent:
   - **Name:** `Leave Manager Agent`
   - **Description:** `Helps employees check leave balances and policies`
   - **Instructions:** `Track employee leaves and provide leave balance information`

   ![Leave Agent Setup](../media/leave-agent-setup.png)

3. **Add Knowledge Source:** Click **+ Add knowledge** and upload **Leave balance Tracker.xlsx** from the lab files.

   ![Upload Leave Tracker](../media/upload-leave-tracker.png)

   > **File Content:** This Excel file contains employee leave balance data that will enable your agent to provide accurate, personalized leave information.

4. Wait for processing to complete (status shows "Ready").

4. Create a topic to handle leave balance queries. Select **+ Add a topic** → **Add from description with Copilot** from the **Topics** tab.

   ![Add Topic with Copilot](../media/add-topic-copilot.png)

6. Enter the following details and click **Create**:
   - **Name:** `Leave Balance Checker`
   - **Create a topic to:** `Get the Employee ID from the user and check and reply with the leave balance based on the tracker added as knowledge source`

   ![Leave Balance Topic Creation](../media/leave-balance-topic-creation.png)

7. Review the generated topic. The system should create nodes to:
   - Get the Employee ID from the user (as a Number)
   - Search and retrieve leave balance information from the knowledge source
   - Provide response with the employee's leave balance

   ![Review Leave Topic](../media/review-leave-topic.png)

8. Check if the topic has the node to get the Employee ID and then click **Save**. Here, we should have a node for getting the Employee ID and a Message node stating that the balance is being retrieved.

   Check the topic once and remove other nodes that have got created apart from the above ones. Then **Save** the topic.

   ![Enhanced Topic Structure](../media/enhanced-topic-structure.png)

9. Send a message **"Check Leave balance"** from the Test pane.

   ![Test Leave Balance](../media/test-leave-balance.png)

10. Enter **1234** for Employee ID when prompted.

   ![Enter Employee ID](../media/enter-employee-id.png)

11. Check the response from the agent. This should be retrieved from the knowledge asset added to the agent.

   ![Leave Balance Response](../media/leave-balance-response.png)

12. Select **Publish** and wait till the agent is published.

   ![Leave Agent Published](../media/leave-agent-published.png)

### Step 2: Connect Agents (Multi-Agent Magic!) (3 minutes)

1. Go back to your **Safe Travels** agent.

2. Navigate to **Agents** tab and click **+ Add**.

   ![Add Agent Integration](../media/add-agent-integration.png)

3. Select **Copilot Studio** and choose your **Leave Manager Agent**.

4. Click **Add agent** to connect them.

   ![Agent Connected](../media/agent-connected.png)

5. **Publish** your updated Safe Travels agent.

### Step 3: Test Multi-Agent Magic! (2 minutes)

1. In your Safe Travels agent test panel, try:
   ```
   Check my leave balance
   ```

2. Watch as your Safe Travels agent automatically hands off the request to the Leave Manager agent!

3. When prompted, enter Employee ID: `1234`

4. See how the Leave Manager responds through the Safe Travels interface - this is multi-agent orchestration in action!

   ![Multi-Agent Success](../media/multi-agent-success.png)

   > **Amazing!** You now have two agents working together - one handles travel, the other handles leave, but users only need to talk to one interface!

## Summary

**Incredible work!** In just 30 minutes, you've built something truly impressive:

### What You've Accomplished:
- Created a travel approval flow that posts to Teams automatically
- Built a specialized Leave Manager agent from scratch  
- Implemented multi-agent orchestration - agents working together!
- Experienced the future of enterprise AI automation

### The Magic You've Created:
Your employees can now talk to **one agent** (Safe Travels) and get help with:
- **Travel questions** → Handled directly by Safe Travels agent
- **Leave questions** → Automatically handed off to Leave Manager agent
- **Travel approvals** → Automatically posted to Teams for managers

This is **multi-agent orchestration** in action - specialized agents collaborating behind the scenes while providing a seamless user experience.

### Real Business Impact:
- Employees get instant help with travel AND leave questions
- Managers receive organized approval requests in Teams
- No manual routing or confusion about which system to use
- Everything works through familiar Microsoft 365 tools

**You've just built an enterprise-grade AI system in 1 hour!**

### Congratulations! You've completed the entire lab series!