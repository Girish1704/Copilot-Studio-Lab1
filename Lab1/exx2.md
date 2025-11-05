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

1. Open **Microsoft Teams** and select **See all your teams** option from the left pane.

   ![Open Teams](../media/ex2-travel-g1.png)

1. Select **Create team** to create a new team.

   ![Create Team](../media/ex2-travel-g2.png)

1. Enter the Team name as **HR Team** and First channel name as **Travel Approval Channel** and select **Create**.

   ![Team Details](../media/ex2-travel-g3.png)

1. Select **Skip** in the Add members to HR Team dialog.

   ![Skip Members](../media/ex2-travel-g4.png)

1. Now, the Team and Channel creation is completed.

   ![Team Created](../media/ex2-travel-g5.png)

   > **Quick Setup:** We're keeping this simple - just one team and channel for approval notifications.

### Step 2: Create Basic Agent Flow (7 minutes)

1. In **Copilot Studio**, go to your **Safe Travels** agent and select **Flows** from the left menu.

   ![Navigate to Flows](../media/ex2-travel-g6.png)

1. Click **New agent flow** to create a new flow.

   ![New Agent Flow](../media/ex2-travel-g7.png)

1. Select **Add a trigger**.

   ![Add Trigger](../media/ex2-travel-g8.png)

1. Select **When an agent calls the flow** under **AI capabilities**.

   ![Select Trigger](../media/ex2-travel-g9.png)

1. Select **+ Add an input**.

   ![Add Input](../media/ex2-travel-g10.png)

1. Select **Number** and name it as **Employee ID**. Then select **+ Add an input**.

   ![Employee ID Input](../media/ex2-travel-g11.png)

   ![Add Second Input](../media/ex2-travel-g12.png)

1. Now, select a **Text** input and name it as **Purpose**.

   ![Purpose Input](../media/ex2-travel-g13.png)

### Step 3: Add Teams Integration (5 minutes)

1. Select **Add an action** below the trigger node.

   ![Add Action](../media/ex2-travel-g14.png)

1. Search for **Teams** and click on **See more** under the Teams group of actions.

   ![Search Teams](../media/ex2-travel-g15.png)

1. Select **Post message in a chat or channel**.

   ![Post Message Action](../media/ex2-travel-g16.png)

1. Select **Sign in** and **login** using your credentials.

   ![Sign In](../media/ex2-travel-g17.png)

   ![Login Credentials](../media/ex2-travel-g18.png)

1. Select the below details:
   - Post as – Select **User**
   - Post in – Select **Channel**
   - Team – Select **HR Team**
   - Channel – Select **Travel Approval Channel**

   ![Configure Teams](../media/ex2-travel-g19.png)

1. In the Message field, enter the following:
   
   Travel Request from 
   Employee ID - < **Employee ID** >
   Purpose - < **Purpose** >
   
   Replace < **Employee ID** > and < **Purpose** > with the dynamic content variables, **Employee ID** and **Purpose** as in the below screenshots.

   ![Message Configuration](../media/ex2-travel-g20.png)

   ![Dynamic Content](../media/ex2-travel-g21.png)

1. The Parameters tab will now look like below.

   ![Parameters Complete](../media/ex2-travel-g22.png)

1. Close the Parameters tab.

   ![Close Parameters](../media/ex2-travel-g23.png)

1. Add another **action** after the Post message node.

   ![Add Second Action](../media/ex2-travel-g24.png)

1. Select **Respond to the agent** under **Skills**.

   ![Respond to Agent](../media/ex2-travel-g25.png)

1. Select **Add an output**. Add a **Text** output. Name it as **Output** and enter the value as **Request submitted**.

   ![Configure Output](../media/ex2-travel-g26.png)

1. Click on **Save draft** to save the flow.

   ![Save Draft](../media/ex2-travel-g27.png)

1. Once the flow is saved, select **Publish**.

   ![Publish Flow](../media/ex2-travel-g28.png)

1. Ensure that the flow has been published.

   ![Flow Published](../media/ex2-travel-g29.png)

1. Click on the **Overview** tab of the agent flow.

   ![Overview Tab](../media/ex2-travel-g30.png)

1. Select **Edit** and name the flow as **Request Travel Approval Flow** in the **Details** pane. Select **Save**.

   ![Name Flow](../media/ex2-travel-g31.png)

### Step 4: Connect Flow to Safe Travels Agent (5 minutes)

1. From the left pane, select **Agents**.

   ![Select Agents](../media/ex2-travel-g32.png)

1. Select the **Safe Travels** agent.

   ![Select Safe Travels](../media/ex2-travel-g33.png)

1. Scroll down in the Overview page and select **Add tool**.

   ![Add Tool](../media/ex2-travel-g34.png)

1. From the **Flow** tab, select the created **Request Travel Approval Flow**.

   ![Select Flow](../media/ex2-travel-g35.png)

1. Select **Add to agent**.

   ![Add to Agent](../media/ex2-travel-g36.png)

1. Once added, the flow will get listed under **Tools** section of the **Overview** page of the **agent**.

   ![Flow Added](../media/ex2-travel-g37.png)

1. Select **Topics** from the top menu. Select **+ Add a topic** -> **Add from description with Copilot**.

   ![Add Topic](../media/ex2-travel-g38.png)

1. Enter the below details and then select **Create**.

   **Name** - **Travel Approval**
   
   **Create a topic to** - **This topic should get the Employee ID (Number) and Purpose of travel (Text) details from the user and invoke the Tool "Request Travel Approval Flow"**

   ![Create Topic](../media/ex2-travel-g39.png)

1. The **Topic** gets created as below.

   ![Topic Created](../media/ex2-travel-g40.png)

   ![Topic Structure](../media/ex2-travel-g41.png)

1. See if the Flow is actually invoked. In this case, only a Message node stating that the flow is invoked is added. In such a case, delete such Message node and click on Add a node icon after the node where the Purpose is requested from the user.

   ![Check Flow](../media/ex2-travel-g42.png)

   ![Add Node](../media/ex2-travel-g43.png)

1. Select **Add a tool** -> **Request Travel Approval Flow**

   ![Add Tool Flow](../media/ex2-travel-g44.png)

1. Add the Variable **EmployeeID** for the flow variable **Employee ID.**

   ![Map Employee ID](../media/ex2-travel-g45.png)

1. Similarly add the Purpose of travel input.

   ![Map Purpose](../media/ex2-travel-g46.png)

1. Add a **Send a message** node and add the Output Variable to it as in the screenshots below.

   ![Add Message Node](../media/ex2-travel-g47.png)

   ![Configure Message](../media/ex2-travel-g48.png)

1. Select **Save** and then **Publish** to publish the agent.

   ![Save Topic](../media/ex2-travel-g49.png)

   ![Publish Agent](../media/ex2-travel-g50.png)

1. Select **Publish** in the confirmation dialog box.

   ![Confirm Publish](../media/ex2-travel-g51.png)

1. Select the Test icon and enter **Travel Approval** and send from the test pane.

   ![Test Travel Approval](../media/ex2-travel-g52.png)

1. Converse by giving the below details to the agent

   Employee ID – **1234**
   Purpose of travel - **Client meeting for finalizing proposal of XYZ project**

   ![Provide Details](../media/ex2-travel-g53.png)

1. Select **Allow** to allow connection.

   ![Allow Connection](../media/ex2-travel-g54.png)

1. You will get a **Request submitted** message from the agent.

   ![Request Submitted](../media/ex2-travel-g55.png)

1. Open the Teams Channel and you will see the details posted there for the Travel approval.

   ![Teams Notification](../media/ex2-travel-g56.png)

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