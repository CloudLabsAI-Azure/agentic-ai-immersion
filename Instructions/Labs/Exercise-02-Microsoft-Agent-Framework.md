# Exercise 01: Microsoft Agent Framework - Business Agents & Multi-Agent Workflows

## Scenario

## Overview

## Objectives

In this exercise, you will complete the following tasks:

- Task 1: Agent Creation Patterns 
- Task 2: Context Providers & Middleware
- Task 3: Threads & Observability 
- Task 4: Multi-Agent Workflows 

## Task 1: Agent Creation Patterns

### **`agent-framework/agents/azure-ai-agents/1-azure-ai-basic.ipynb`**

1. Open `agent-framework/agents/azure-ai-agents/1-azure-ai-basic.ipynb`.

1. This notebook demonstrates the fundamentals of building an Azure AI Agent using the AzureAIProjectAgentProvider. You'll learn how to create an agent with function tools, interact with it using streaming and non-streaming responses, and manage agent resources using asynchronous programming patterns.

   - Set up and configure the AzureAIProjectAgentProvider.
   - Create and configure an AI Advisor agent with function tools.
   - Invoke function tools to perform banking-related operations.
   - Interact with the agent using both streaming and non-streaming responses.
   - Manage agent lifecycle and resources using asynchronous context managers.
  
1. Select the Python Kernel

1. Run all the cells individually to setup and build your AI Advisor agent with function tools using Microsoft Agent Framework.

1. After running all the cells in the notebook, you will have successfully built an Azure AI Advisor Agent that can:

   - Create and manage AI agents using the AzureAIProjectAgentProvider.
   - Invoke custom function tools to perform banking-related operations.
   - Generate both streaming and non-streaming responses.
   - Manage agent resources efficiently using asynchronous context managers.
   - Build function-enabled AI agents for common financial assistance scenarios.

### **`agent-framework/agents/azure-ai-agents/2-azure-ai-with-explicit-settings.ipynb`**

1. Open `agent-framework/agents/azure-ai-agents/2-azure-ai-with-explicit-settings.ipynb`.

1. This notebook demonstrates how to create an Azure AI Investment Advisor Agent using explicit configuration instead of relying on environment variable defaults. You'll learn how to configure the Azure AI client, project endpoint, and model deployment programmatically, providing greater control for production, governance, and compliance scenarios.

   - Configure Azure AI client settings using explicit parameters.
   - Specify the Azure AI Foundry project endpoint and model deployment directly.
   - Create and configure an Investment Advisor agent with custom settings.
   - Explore production-ready configuration patterns for governance and compliance.
   - Build a configurable AI agent for investment portfolio analysis and advisory scenarios.

1. Select the Python Kernel
  
1. Run all the cells individually to setup and build your Azure AI Investment Advisor Agent using explicit configuration.

1. After running all the cells in the notebook, you will have successfully built an Investment Advisor Agent that can:

   - Configure Azure AI client settings explicitly without relying on environment variables.
   - Connect to specific Azure AI Foundry project endpoints and model deployments.
   - Support dynamic configurations for different environments, client tiers, or compliance requirements.
   - Enable flexible deployment, testing, and governance through configurable agent settings.
   - Provide investment portfolio guidance using production-ready configuration patterns.
  
### **`agent-framework/agents/azure-ai-agents/4-azure-ai-with-function-tools.ipynb`**

1. Open `agent-framework/agents/azure-ai-agents/4-azure-ai-with-function-tools.ipynb`

1. This notebook demonstrates how to build an Azure AI Banking Agent with Function Tools using the AzureAIProjectAgentProvider. You'll learn how to integrate custom functions for banking operations, configure tools at both the agent and run levels, and enable the agent to coordinate multiple functions to handle financial assistance scenarios.

   - Define and integrate function tools for common banking operations.
   - Configure tools at the agent level and dynamically during agent execution.
   - Invoke multiple function tools to support banking-related workflows.
   - Explore different tool configuration patterns for flexible agent behavior.
   - Build a function-enabled banking agent while following responsible AI and financial best practices.
  
1. Select the Python Kernel

1. Run all the cells individually to set up and build your Azure AI Banking Agent with Function Tools.

1. After running all the cells in the notebook, you will have successfully built an Azure AI Banking Agent that can:

   - Invoke custom function tools for banking operations such as account management, transaction history, loan calculations, credit score checks, and investment portfolio reviews.
   - Configure function tools at both the agent level and per request for flexible tool execution.
   - Coordinate multiple banking functions to handle a variety of financial assistance scenarios.
   - Follow production-ready practices for tool definitions, parameter validation, and error handling.
   - Provide simulated banking assistance while incorporating appropriate financial disclaimers and responsible AI practices.

### **`agent-framework/agents/azure-ai-agents/5-azure-ai-with-code-interpreter.ipynb`**

1. Open `agent-framework/agents/azure-ai-agents/5-azure-ai-with-code-interpreter.ipynb`

1. This notebook demonstrates how to build an Azure AI Financial Analytics Agent using the Hosted Code Interpreter Tool with the AzureAIProjectAgentProvider. You'll learn how to enable the agent to execute Python code for financial calculations, analyze investment data, and generate insights for common financial scenarios.

   - Configure and integrate the Hosted Code Interpreter Tool with an Azure AI agent.
   - Execute Python code to perform financial calculations and data analysis.
   - Analyze portfolios, calculate compound interest, and generate loan amortization schedules.
   - Access and interpret Code Interpreter inputs and outputs.
   - Generate streaming responses while following responsible AI and financial best practices.
  
1. Select the Python Kernel

1. Run all the cells individually to set up and build your Azure AI Financial Analytics Agent with the Hosted Code Interpreter Tool.

1. After running all the cells in the notebook, you will have successfully built an Azure AI Financial Analytics Agent that can:

   - Execute Python code securely using the Hosted Code Interpreter Tool for financial calculations.
   - Perform portfolio analysis, compound interest calculations, loan amortization, and investment projections.
   - Generate data-driven financial insights and support what-if analysis.
   - Access and review Code Interpreter inputs, outputs, and executed code.
   - Support both streaming and non-streaming responses while following responsible AI and financial best practices.

### **`agent-framework/agents/azure-ai-agents/6-azure-ai-with-file-search.ipynb`**

1. Open `agent-framework/agents/azure-ai-agents/6-azure-ai-with-file-search.ipynb`

1. This notebook demonstrates how to build an Azure AI Financial Document Search Agent using the AzureAIProjectAgentProvider with File Search capabilities. You'll learn how to upload financial documents, create a vector store, configure file search, and enable the agent to answer questions using document-based knowledge.

   - Upload and manage financial documents for AI-powered search.
   - Create and manage a vector store for document retrieval.
   - Configure and integrate the File Search tool with an Azure AI agent.
   - Answer questions using loan policies, compliance documents, and financial reports.
   - Build a document-grounded AI agent while following responsible AI and financial best practices.
  
1. Select the Python Kernel

1. Run all the cells individually to set up and build your Azure AI Financial Document Search Agent with File Search.

1. After running all the cells in the notebook, you will have successfully built an Azure AI Financial Document Search Agent that can:

   - Upload and index financial documents in vector stores for efficient retrieval.
   - Search loan policies, compliance documents, and financial reports using File Search.
   - Answer document-based queries with grounded responses from uploaded content.
   - Manage document resources, including file uploads and vector stores, using production-ready practices.
   - Deliver intelligent document search and Q&A while following responsible AI and financial best practices.













   
