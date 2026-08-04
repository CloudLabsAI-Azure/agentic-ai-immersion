# Exercise 01: Microsoft Agent Framework - Business Agents & Multi-Agent Workflows

## Scenario

## Overview

## Objectives

In this exercise, you will complete the following tasks:

- Task 1: Agent Creation Patterns 
- Task 2: Context Providers & Middleware
- Task 3: Observability & Threads
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

## Task 2: Context Providers & Middleware

### **`agent-framework/context-providers/1-simple-context-provider.ipynb`**

1. Open `agent-framework/context-providers/1-simple-context-provider.ipynb`.

1. This notebook demonstrates how to build a Customer KYC Agent using a Simple Context Provider with the AzureAIProjectAgentProvider. You'll learn how to maintain conversation state, collect and manage customer profile information, and provide dynamic context to the agent to support Know Your Customer (KYC) compliance workflows.

   - Create and implement a custom ContextProvider class.
   - Extract structured customer information from conversations.
   - Provide dynamic context to the agent based on collected customer data.
   - Maintain conversation state across multiple interactions.
   - Build a KYC-focused AI agent while following responsible AI and data privacy best practices.
  
1. Select the Python Kernel

1. Run all the cells individually to set up and build your Customer KYC Agent using a Simple Context Provider.

1. After running all the cells in the notebook, you will have successfully built a Customer KYC Agent that can:

   - Collect and maintain customer profile information throughout a conversation.
   - Provide dynamic context to the agent before each response using a custom Context Provider.
   - Extract and persist structured customer data after each interaction.
   - Support multi-turn KYC workflows with stateful conversation management.
   - Demonstrate production-ready context management for customer onboarding and compliance scenarios.

### `agent-framework/context-providers/2-azure-ai-search-context-agentic.ipynb`

1. Open `agent-framework/context-providers/2-azure-ai-search-context-agentic.ipynb`

1. This notebook demonstrates how to build a Loan Underwriting Agent using Azure AI Search with Agentic Mode for Retrieval-Augmented Generation (RAG). You'll learn how to create a knowledge base, enable multi-hop reasoning, and retrieve underwriting guidance to support complex loan eligibility and risk assessment scenarios.

   - Configure the AzureAISearchContextProvider with Agentic Mode.
   - Create and use a Knowledge Base for underwriting policy documents.
   - Perform multi-hop reasoning across underwriting guidelines and eligibility criteria.
   - Answer complex loan underwriting and risk assessment questions using AI Search.
   - Build a knowledge-grounded underwriting agent while following responsible AI and financial best practices.

1. Select the Python Kernel

1. Run all the cells individually to set up and build your Loan Underwriting Agent using Azure AI Search with Agentic Mode.

1. After running all the cells in the notebook, you will have successfully built a Loan Underwriting Agent that can:

   - Retrieve underwriting policies and eligibility criteria using Azure AI Search.
   - Perform multi-hop reasoning across multiple knowledge sources with Agentic Mode.
   - Answer complex loan eligibility, DTI, LTV, and documentation-related questions.
   - Leverage a knowledge base to provide grounded, context-aware underwriting guidance.
   - Demonstrate intelligent RAG patterns for loan underwriting while following responsible AI practices.

### **`agent-framework/middleware/1-agent-and-run-level-middleware.ipynb`**

1. Open `agent-framework/middleware/1-agent-and-run-level-middleware.ipynb`

1. This notebook demonstrates how to implement Agent-Level and Run-Level Middleware using an Azure AI Agent in a Transaction Compliance Monitoring scenario. You'll learn how middleware can be applied at different stages of agent execution to support security, monitoring, auditing, priority handling, and caching for financial services applications.

   - Understand the differences between Agent-Level and Run-Level middleware.
   - Configure middleware to handle security validation, audit logging, and performance monitoring.
   - Apply Run-Level middleware for priority handling, debugging, and caching.
   - Explore middleware execution order during agent processing.
   - Build a transaction compliance monitoring solution using production-ready middleware patterns.

1. Select the Python Kernel

1. Run all the cells individually to set up and build your Transaction Compliance Monitoring Agent with Agent-Level and Run-Level Middleware.

1. After running all the cells in the notebook, you will have successfully built a Transaction Compliance Monitoring Agent that can:

   - Apply Agent-Level Middleware for security validation, performance monitoring, and audit logging.
   - Apply Run-Level Middleware for request-specific behaviors such as priority handling and caching.
   - Process transactions using a layered middleware execution pipeline.
   - Monitor and manage compliance workflows using production-ready middleware patterns.
   - Demonstrate flexible middleware design for secure and compliant financial services applications.

### **`agent-framework/middleware/4-decorator-middleware.ipynb`**

1. Open `agent-framework/middleware/4-decorator-middleware.ipynb`

1. This notebook demonstrates how to implement Decorator-Based Middleware for an Azure AI Portfolio Rebalancing Agent using the @agent_middleware and @function_middleware decorators. You'll learn how to simplify middleware development while applying trading validations and logging to support portfolio management workflows.

   - Implement middleware using the @agent_middleware and @function_middleware decorators.
   - Simplify middleware development with cleaner, decorator-based syntax.
   - Validate trading requests before portfolio operations are executed.
   - Log portfolio changes during agent execution.
   - Build a portfolio rebalancing agent using production-ready middleware patterns.

1. Select the Python Kernel

1. Run all the cells individually to set up and build your Portfolio Rebalancing Agent using Decorator-Based Middleware.

1. After running all the cells in the notebook, you will have successfully built a Portfolio Rebalancing Agent that can:

   - Implement middleware using @agent_middleware and @function_middleware decorators.
   - Validate trading requests by enforcing trading window checks.
   - Log portfolio updates and middleware activity during agent execution.
   - Simplify middleware implementation through automatic context injection.
   - Apply clean, production-ready middleware patterns for portfolio management scenarios.

### **`agent-framework/middleware/7-middleware-termination.ipynb`**

1. Open `agent-framework/middleware/7-middleware-termination.ipynb`

1. This notebook demonstrates how to implement Middleware Termination in an Azure AI Transaction Compliance Agent. You'll learn how middleware can terminate the execution pipeline early to enforce compliance rules, block prohibited transactions, and return immediate responses when policy conditions are met.

   - Understand how middleware can terminate the agent execution pipeline.
   - Implement pre-termination logic to block prohibited transaction requests.
   - Apply post-termination logic for scenarios such as rate limiting.
   - Return immediate compliance responses using short-circuit middleware.
   - Build a transaction compliance agent using production-ready middleware patterns.

1. Select the Python Kernel

1. Run all the cells individually to set up and build your Transaction Compliance Agent with Middleware Termination.

1. After running all the cells in the notebook, you will have successfully built a Transaction Compliance Agent that can:

   - Terminate the middleware pipeline to enforce compliance policies.
   - Block prohibited transactions before agent execution.
   - Apply rate limiting and short-circuit responses when required.
   - Return immediate compliance decisions without invoking the agent.
   - Demonstrate production-ready middleware termination patterns for financial services applications.

## Task 3: Observability & Threads

### **`agent-framework/observability/1-agent-with-foundry-tracing.ipynb`**

1. Open `agent-framework/observability/1-agent-with-foundry-tracing.ipynb`

1. This notebook demonstrates how to implement Observability for an Azure AI Agent using Azure AI Foundry Tracing. You'll learn how to configure telemetry, collect traces, and monitor agent execution with Application Insights, enabling end-to-end visibility into agent performance and operations.

   - Configure Azure AI Foundry Tracing for AI agents.
   - Integrate Application Insights to collect telemetry and diagnostics.
   - Capture trace IDs to monitor agent requests across distributed systems.
   - Monitor agent execution and performance using live metrics and traces.
   - Build an observable AI agent using production-ready monitoring practices.

1. Create the Application Insights connection within your Microsoft Foundry resource.

1. Select the Python Kernel

1. Run all the cells individually to set up and build your Azure AI Agent with Foundry Tracing for observability.

1. After running all the cells in the notebook, you will have successfully built an Observable Azure AI Agent that can:

   - Collect telemetry and traces using Azure AI Foundry Tracing.
   - Monitor agent performance with Application Insights.
   - Track requests end-to-end using trace IDs for distributed diagnostics.
   - Observe agent execution through live metrics and telemetry data.
   - Implement production-ready observability practices for AI applications.

1. View Traces in Azure Portal:

   - Go to Azure Portal > Application Insights
   - Select Investigate > Search
   - Filter by the Trace ID shown above

### **`agent-framework/observability/2-azure-ai-agent-observability.ipynb`**

1. Open `agent-framework/observability/2-azure-ai-agent-observability.ipynb`

1. This notebook demonstrates how to implement Observability for an Azure AI Agent using the AzureAIClient. You'll learn how to enable automatic tracing, capture span context, and integrate with Application Insights to monitor agent interactions and diagnose application behavior.

   - Configure observability for Azure AI agents using the AzureAIClient.
   - Enable automatic tracing to capture agent execution details.
   - Track conversation flow using distributed trace spans and span context.
   - Integrate with Application Insights for centralized monitoring and diagnostics.
   - Build observable AI applications using production-ready monitoring practices.

1. Select the Python Kernel

1. Run all the cells individually to set up and build an Observable Azure AI Customer Service Agent using the AzureAIClient.

1. After running all the cells in the notebook, you will have successfully built an Observable Azure AI Customer Service Agent that can:

   - Enable automatic tracing for AI agent interactions.
   - Track conversation flow using distributed trace spans and span context.
   - Send telemetry and diagnostics to Application Insights for centralized monitoring.
   - Monitor agent execution to support troubleshooting and performance analysis.
   - Implement production-ready observability practices for AI-powered customer service applications.

1. View Traces in Azure Portal:

   - Go to Azure Portal > Application Insights
   - Select Investigate > Search
   - Filter by the Trace ID shown above
  
### **`agent-framework/threads/1-custom-chat-message-store-thread.ipynb`**

1. Open `agent-framework/threads/1-custom-chat-message-store-thread.ipynb`

1. This notebook demonstrates how to implement a Custom Chat Message Store for managing conversation threads in an Azure AI Agent. You'll learn how to store, serialize, and manage conversation history using custom storage backends to support compliance, auditing, and enterprise data governance requirements.

   - Create and configure a custom chat message store for conversation threads.
   - Store and serialize complete conversation histories for auditing.
   - Integrate custom storage backends to meet enterprise data requirements.
   - Manage conversation persistence while supporting data residency and retention policies.
   - Build compliance-ready AI applications using production-grade conversation management patte

1. Select the Python Kernel

1. Run all the cells individually to set up and build an Azure AI Agent with a Custom Chat Message Store.

1. After running all the cells in the notebook, you will have successfully built an Azure AI Agent that can:

   - Persist conversation threads using a custom Chat Message Store.
   - Create thread-specific storage instances using a chat_message_store_factory.
   - Serialize and deserialize conversation history for long-term persistence and auditability.
   - Integrate custom storage backends to support enterprise compliance and governance requirements.
   - Demonstrate production-ready thread management for secure, compliant AI applications.

### **`agent-framework/threads/3-suspend-resume-thread.ipynb`**

1. Open `agent-framework/threads/3-suspend-resume-thread.ipynb`

1. This notebook demonstrates how to suspend and resume conversation threads in Azure AI Agents, comparing service-managed threads with in-memory threads. You'll learn how to persist conversation state, resume interactions across sessions, and support seamless user experiences for long-running workflows.

   - Understand the differences between service-managed and in-memory conversation threads.
   - Suspend and resume conversation threads while preserving context.
   - Manage persistent conversation state across multiple sessions.
   - Support multi-device conversation continuity using Azure AI Agents.
   - Build production-ready thread management for long-running AI workflows.

1. Select the Python Kernel

1. Run all the cells individually to set up and build an Azure AI Agent with Suspend and Resume Conversation Threads.

1. After running all the cells in the notebook, you will have successfully built an Azure AI Agent that can:

   - Suspend and resume conversation threads while preserving conversation context.
   - Compare service-managed and in-memory thread management approaches.
   - Persist conversations across user sessions for long-running workflows.
   - Support conversation continuity across multiple devices and sessions.
   - Implement production-ready thread lifecycle management for enterprise AI applications.
  
## Task 4: Multi-Agent Workflows 
