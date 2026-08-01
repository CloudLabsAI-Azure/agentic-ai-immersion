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

### **`azure-ai-agents/1-basics.ipynb`**

1. Open `azure-ai-agents/1-basics.ipynb`

   ![](../../images/azure-ai-agents-1-basics.png)

1. This notebook demonstrates how to build a Financial Services Advisor AI Agent using the Azure AI Foundry SDK. The agent is designed to provide general guidance on banking, loans, and investments while following responsible AI practices, incorporating regulatory disclaimers, and supporting observability through logging and tracing.

   - Initialize and connect to an Azure AI Foundry project using the azure-ai-projects SDK.
   - Create and configure a domain-specific Financial Services Advisor agent.
   - Manage conversations using threads, messages, and agent runs.
   - Enable logging and tracing with OpenTelemetry for monitoring and diagnostics.
   - Extend the agent with tools and implement financial disclaimers and responsible AI best practices.

1. Run all the cells individually to setup and build your Financial Services Agent.

1. After running all the cells in the notebook, you would've successfully built a Financial Services Advisor that can:

   - Respond to basic banking, loan, and financial questions.
   - Use disclaimers to ensure regulatory compliance and encourage professional consultation.
   - Provide general banking product and savings information.
   - Use the synergy of Microsoft Foundry modules to power the conversation.

### **`azure-ai-agents/2-code-interpreter.ipynb`**

1. Open `azure-ai-agents/2-code-interpreter.ipynb`

   ![](../../images/azure-ai-agents-2-code-interpreter.png)

1. This notebook demonstrates how to build a Loan Calculator AI Agent using the Azure AI Foundry SDK. The agent leverages Code Interpreter capabilities to perform financial calculations, analyze loan-related data, and generate insights for common lending scenarios while following responsible AI practices and providing appropriate financial disclaimers.

   - Initialize and connect to an Azure AI Foundry project using the Azure AI Foundry SDK.
   - Create and configure a Loan Calculator agent with Code Interpreter capabilities.
   - Perform common loan calculations, including monthly payments, amortization schedules, and interest analysis.
   - Analyze sample loan portfolio data to derive financial insights and trends.
   - Generate data-driven responses with appropriate financial disclaimers and responsible AI best practices.

1. Run all the cells individually to setup and build your Loan Calculator agent.

1. After running all the cells in the notebook, you will have successfully built a Loan Calculator Agent that can:
   
   - Perform loan calculations, including monthly payments, interest analysis, and amortization schedules.
   - Execute Python code securely using Code Interpreter for financial analysis.
   - Analyze loan portfolio data and generate financial insights.
   - Provide responses with appropriate financial disclaimers and responsible AI practices.
   - Combine Azure AI Foundry and Code Interpreter for intelligent financial assistance.

## Task 3: File Search & Bing Grounding

### **`azure-ai-agents/3-file-search.ipynb`**

1. Open `azure-ai-agents/3-file-search.ipynb`

1. This notebook demonstrates how to build a Banking Document Search AI Agent using the Azure AI Foundry SDK. The agent leverages the File Search tool to search banking documents, loan guidelines, and policy manuals, enabling it to answer questions based on uploaded content.

   - Initialize and connect to an Azure AI Foundry project using the Azure AI Foundry SDK.
   - Upload banking policy documents and loan guidelines to a vector store.
   - Create and configure an AI agent with File Search capabilities.
   - Search documents to retrieve relevant banking policies, regulations, and compliance information.
   - Answer customer and employee queries using information from uploaded documents.
  
1. Run all the cells individually to setup and build your Banking Document Search Agent.

1. After running all the cells in the notebook, you will have successfully built a Banking Document Search Agent that can:

   - Search uploaded banking documents using File Search and semantic search.
   - Retrieve information from banking policies, loan guidelines, and compliance documents.
   - Answer customer and employee queries using document-based knowledge.
   - Provide responses with appropriate financial disclaimers and responsible AI practices.
   - Leverage Azure AI Foundry and File Search for intelligent document retrieval.

### **`azure-ai-agents/4-web-search.ipynb`**

1. Open `azure-ai-agents/4-web-search.ipynb`

1. This notebook demonstrates how to build a Financial Market Research AI Agent using the Azure AI Foundry SDK. The agent leverages the Web Search tool to retrieve real-time financial information, market trends, interest rates, and news from the web, enabling it to provide up-to-date responses with inline citations.

   - Initialize and connect to an Azure AI Foundry project using the Azure AI Foundry SDK.
   - Create and configure an AI agent with Web Search capabilities.
   - Retrieve real-time financial news, market trends, and interest rate information from the web.
   - Answer financial market research queries using current web-based information.
   - Generate responses with inline citations and responsible AI best practices.
  
1. Run all the cells individually to setup and build your Financial Market Research Agent with Web Search.

1. After running all the cells in the notebook, you will have successfully built a Financial Market Research Agent that can:

   - Retrieve real-time financial news, market trends, and interest rate information using Web Search.
   - Answer market research queries with up-to-date web-based information.
   - Generate responses with inline URL citations for referenced sources.
   - Use location-aware web search to provide more relevant financial insights.
   - Leverage Azure AI Foundry and the Responses API for real-time, citation-backed responses.

## Task 4: Enterprise Search, MCP Tools & Foundry IQ

### **`azure-ai-agents/5-agents-aisearch.ipynb`**

1. Open `azure-ai-agents/5-agents-aisearch.ipynb`

1. This notebook demonstrates how to build a Banking Products Catalog AI Agent by integrating Azure AI Search with Azure AI Foundry Agent Service. The agent uses semantic search to retrieve information from a banking products catalog, enabling it to answer customer queries and provide product recommendations based on indexed financial data.

   - Initialize and connect to an Azure AI Foundry project using the Azure AI Foundry SDK.
   - Create and populate an Azure AI Search index with banking products such as loans, credit cards, and accounts.
   - Perform semantic searches to retrieve relevant banking product information.
   - Create and configure an AI agent integrated with Azure AI Search.
   - Answer banking product queries and recommendations using search-grounded responses while incorporating financial disclaimers and responsible AI best practices.
  
1. Create the Azure AI Search connection within your Microsoft Foundry resource. Copy the connection name.

1. Update the connection name within the notebook in `2. Create Banking Product Advisor Agent With Azure AI Search Tool`

1. Run all the cells individually to setup and build your Banking Products Catalog AI Agent by integrating Azure AI Search with Azure AI Foundry Agent Service.

1. After running all the cells in the notebook, you will have successfully built an Azure AI Search + Agent Service solution that can:

   - Perform semantic and vector-based search over a product catalog using Azure AI Search.
   - Retrieve relevant results using vector embeddings and semantic ranking for natural language queries.
   - Create an AI agent that leverages search-grounded responses to answer product-related questions.
   - Understand user intent beyond keyword matching using vector similarity and semantic search.
   - Integrate Azure AI Search, Azure OpenAI embeddings, and Azure AI Foundry Agent Service to deliver intelligent, context-aware responses.

### **`azure-ai-agents/7-mcp-tools.ipynb`**

1. Open `azure-ai-agents/7-mcp-tools.ipynb`

1. This notebook demonstrates how to build an AI Agent that integrates with the Azure AI Foundry MCP (Model Context Protocol) Server. The agent uses MCP tools to securely access Azure AI Foundry capabilities, enabling it to interact with external tools and services through a standardized protocol.

   - Understand the Azure AI Foundry MCP Server and its capabilities.
   - Configure an MCP tool connection within an Azure AI Foundry project.
   - Create and configure an AI agent with MCP tool integration.
   - Invoke MCP tools to access Azure AI Foundry capabilities through the agent.
   - Handle MCP approval requests and implement secure tool access using responsible AI best practices.
  
1. Navigate to Foundry > Build > Tools, click on Connect a tool > Catalog > Foundry MCP Server (preview) and then click on Create.

1. Copy the Project Connection ID and add it under `.env` file for `FOUNDRY_MCP_CONNECTION_ID`

1. Run all the cells individually to setup and build your Banking Products Catalog AI Agent by integrating Azure AI Search with Azure AI Foundry Agent Service.

1. After running all the cells in the notebook, you will have successfully built an AI Agent integrated with the Azure AI Foundry MCP Server that can:

   - Connect to Azure AI Foundry using an MCP tool connection.
   - Access Azure AI Foundry capabilities through standardized MCP tools.
   - Securely invoke tools by handling MCP approval requests.
   - Configure MCP connections using project connection IDs.
   - Extend agent capabilities through secure and standardized tool integration.
  
### **`azure-ai-agents/8-foundry-IQ-agents.ipynb`**

1. Open `azure-ai-agents/8-foundry-IQ-agents.ipynb`

1. This notebook demonstrates how to build a Fraud Investigation AI Agent using Azure AI Foundry IQ. The agent leverages Foundry IQ as a unified knowledge layer to retrieve information from multiple knowledge sources, enabling intelligent, grounded responses for fraud investigation and compliance scenarios.

   - Understand how Azure AI Foundry IQ provides a unified knowledge layer for AI agents.
   - Configure and connect multiple knowledge sources within Foundry IQ.
   - Create and configure a Fraud Investigation AI Agent using Foundry IQ.
   - Query fraud intelligence, regulatory compliance, and investigation procedure knowledge bases through a single agent.
   - Generate knowledge-grounded responses using multiple enterprise knowledge sources while following responsible AI best practices.

1. Run all the cells individually to setup and build your Fraud Investigation AI Agent using Azure AI Foundry IQ.
  
1. After running all the cells in the notebook, you will have successfully built a Foundry IQ-powered Fraud Investigation Agent that can:

   - Query multiple knowledge sources through a unified Foundry IQ knowledge base.
   - Retrieve fraud patterns, regulatory guidance, and investigation procedures using semantic search.
   - Generate knowledge-grounded responses for fraud investigation scenarios.
   - Leverage vector-enabled search indexes for intelligent information retrieval.
   - Combine Azure AI Foundry IQ and AI Agents to deliver context-aware fraud analysis and investigation support.
