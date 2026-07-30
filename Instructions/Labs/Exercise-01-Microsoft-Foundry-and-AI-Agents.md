# Exercise 01: Getting Started with Microsoft Foundry & AI Agents 

## Scenario

## Overview

## Objectives

In this exercise, you will complete the following tasks:

- Task 1: Environment & Microsoft Foundry Setup 
- Task 2: Agent Basics & Code Interpreter
- Task 3: File Search & Bing Grounding
- Task 4: Enterprise Search, MCP Tools & Foundry IQ

## Task 1: Environment & Microsoft Foundry Setup

1. Open **Visual Studio Code** on your Lab-VM.

   ![](../../images/vs.png)

1. Once the IDE opens, if you see the ***Welcome to VS Code*** sign-in pop-up for GitHub, simply close the window by clicking the **X** in the upper-right corner.

   ![](../../images/vsc-welcome-window-close.png)

1. From the **File** menu in VS Code, choose **Open Folder**.

   ![](../../images/vsc-open-folder.png)

1. Select the **C:\Users\azureuser\agentic-ai-immersion** folder and click **Select folder**.

   ![](../../images/vsc-select-folder-terraformlabs-01.png)

1. Now you will see another screen Do you trust the authors of the files in this folder?. Select the **checkbox (1)** *Trust the authors of all files in the parent folder 'azureuser'* and then click **Yes, I trust the authors (2)**.

   ![](../../images/vsc-trust-folder-terraformlabs-01.png)

1. Open the integrated terminal by selecting **Terminal → New Terminal**.

   ![](../../images/vsc-terraform-lab-new-terminal.png)

1. In the integrated terminal, verify that Python is installed by running the following command:

   ```bash
   python --version
   ```

1. Create and activate virtual environment

   ```
   python -m venv .venv
   .\.venv\Scripts\activate
   ```

1. Install dependencies (versions are pinned for consistency)

   ```
   pip install -r requirements.txt
   ```

1. Sign in to Azure from the integrated terminal:

   ```
   az login
   ```

   > 📌 **Note:** You only need to sign in to Azure once in this lab. Keep using the same integrated terminal session for the upcoming labs so that your Azure authentication remains active.

1. On the *Let’s get you signed in pop-up*, select **Work or school account**, then click **Continue**. You may need to minimize any open applications to bring this window into view.

   ![](../../images/az-select-work-or-school-account.png)

1. You'll see the Sign into Microsoft Azure tab. Here, enter your credentials:

   - **Email/Username:** <inject key="AzureAdUserEmail"></inject>
  
     ![](../../images/az-enter-username.png)
  
1. Next, enter the Temporary Access Pass:

   - **Temporary Access Pass:** <inject key="AzureAdUserPassword"></inject>
  
     ![](../../images/az-enter-tap.png)

1. On the *Sign in to all apps, websites, and services on this device?*, click **No, this app only**.

   ![](../../images/az-no-this-app-only.png)

1. You are now signed in to the Azure portal from your Visual Studio Code terminal. In Visual Studio Code integrated terminal, when prompted to select a subscription and tenant, press **Enter** to accept the default selection.

   ![](../../images/az-select-subs-enter-01.png)

1. Copy .env.example to .env at the repo root

   ```
   cp .env.example .env
   ```

1. Microsoft Foundry project (azure-ai-agents/ + observability notebooks)

   ```
   AI_FOUNDRY_PROJECT_ENDPOINT=https://<your-foundry>.services.ai.azure.com/api/projects/<your-project>
   AZURE_AI_MODEL_DEPLOYMENT_NAME=gpt-5.4
   EMBEDDING_MODEL_DEPLOYMENT_NAME=text-embedding-3-large
   ```

1. Agent Framework Foundry client convention (agent-framework/ notebooks)

   ```
   FOUNDRY_PROJECT_ENDPOINT=https://<your-foundry>.services.ai.azure.com/api/projects/<your-project>
   FOUNDRY_MODEL=gpt-5.4
   ```

1. Azure OpenAI v1 surface (agent-framework workflows / middleware / threads)

   ```
   AZURE_OPENAI_ENDPOINT=https://<your-foundry>.openai.azure.com/openai/v1
   AZURE_OPENAI_API_KEY=        # leave BLANK — this workshop uses Entra ID (az login), not keys
   ```

1. Azure AI Search (notebooks 5 & 8, context-providers/2)

   ```
   AZURE_AI_SEARCH_ENDPOINT=https://<your-search>.search.windows.net
   ```

## Task 2: Agent Basics & Code Interpreter

1. Open `azure-ai-agents/1-basics.ipynb`. This notebook is about Financial Services Advisor Agent Tutorial

   ![](../../images/azure-ai-agents-1-basics.png)

1. Run the first cell `1. Initial Setup`

   ![](../../images/azure-ai-agents-1-basics-01.png)

1. Select the Python kernel

1. You should be able to see the output that **Successfully Initialized AIProjectClient**

   ![](../../images/azure-ai-agents-1-basics-01-output.png)

1. Run the next cell `2. Creating our Financial Services Advisor Agent 🏦`

   ![](../../images/azure-ai-agents-1-basics-02.png)

1. You should be able to see the output that **🎉 Created financial services advisor agent (name: financial-services-advisor, version: 1)**

   ![](../../images/azure-ai-agents-1-basics-02-output.png)

1. Run the next cell `3. Managing Financial Service Conversations 💬`

   ![](../../images/azure-ai-agents-1-basics-03.png)

1. You should be able to see the output that **📝 Created a new conversation**

   ![](../../images/azure-ai-agents-1-basics-03-output.png)

1. Run the next cell `4. Asking Banking & Financial Questions 💳`

   ![](../../images/azure-ai-agents-1-basics-04.png)

1. You should be able to see the output that **🧪 Testing the Financial Services Advisor Agent...**

   ![](../../images/azure-ai-agents-1-basics-04-output.png)

1. Run the next cell `Example Financial Services Queries`

   ![](../../images/azure-ai-agents-1-basics-04-example.png)

1. You should be able to see the output that **Completed 4 tests conversations with our Financial Services Advisor!**

   ![](../../images/azure-ai-agents-1-basics-04-example-output.png)

1. Run the next cell `5. Final Test: Complex Financial Question 🧹`

   ![](../../images/azure-ai-agents-1-basics-05.png)

1. You should be able to see the output that **Final test successful!**

   ![](../../images/azure-ai-agents-1-basics-05-output.png)

1. Run the next cell `5. Cleanup 🧹` to delete your "Financial Services Advisor Agent"

   ![](../../images/azure-ai-agents-1-basics-cleanup.png)

1. Open `azure-ai-agents/2-code-interpreter.ipynb`. This notebook is about Loan Calculator Agent Tutorial

   ![](../../images/azure-ai-agents-2-code-interpreter.png)

1. Run the first cell `1. Initial Setup`

   ![](../../images/azure-ai-agents-2-code-interpreter-01.png)

1. Select the Python kernel

1. You should be able to see the output that **Successfully Initialized AIProjectClient**

   ![](../../images/azure-ai-agents-2-code-interpreter-01-output.png)

1. Run the next cell `2. Create Loan Calculator Agent 👩‍💻`

   ![](../../images/azure-ai-agents-2-code-interpreter-02.png)

1. You should be able to see the output that **🎉 Created agent: loan-calculator-agent (version: 1)**

   ![](../../images/azure-ai-agents-2-code-interpreter-02-output.png)

1. Run the next cell `3. Loan Payment Calculation with Code Interpreter`

   ![](../../images/azure-ai-agents-2-code-interpreter-03.png)

1. You should be able to see the output that **Loan calculation completed!**

   ![](../../images/azure-ai-agents-2-code-interpreter-03-output.png)

1. Run the next cell `4. Loan Comparison Analysis`

   ![](../../images/azure-ai-agents-2-code-interpreter-04.png)

1. You should be able to see the output that **Loan comparison completed!**

   ![](../../images/azure-ai-agents-2-code-interpreter-04-output.png)

1. Run the next cell `5. Portfolio Risk Analysis 📊`

   ![](../../images/azure-ai-agents-2-code-interpreter-05.png)

1. You should be able to see the output that **Portfolio analysis completed!**

   ![](../../images/azure-ai-agents-2-code-interpreter-05-output.png)

1. Run the next cell `6. Cleanup & Best Practices` to delete your "Loan Calculator Agent"

   ![](../../images/azure-ai-agents-2-code-interpreter-cleanup.png)

## Task 3: File Search & Bing Grounding

