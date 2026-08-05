# Exercise 03: Observability, Evaluation, Responsible AI & Hosted Deployment 

## Scenario

## Overview

## Objectives

In this exercise, you will complete the following tasks:

- Task 1: Telemetry & Monitoring 
- Task 2: Agent & Tool Evaluation
- Task 3: Red Team Security Testing 
- Task 4: Deploying Hosted Agents

## Task 1: Telemetry & Monitoring 

### **`observability-and-evaluations/1-telemetry.ipynb`**

1. Open `observability-and-evaluations/1-telemetry.ipynb`

1. This notebook demonstrates how to implement Telemetry and Tracing for an Azure AI Wealth Management Advisory Agent using Azure Monitor and OpenTelemetry. You'll learn how to capture agent interactions, create custom trace spans, and monitor application behavior to support observability, compliance, and troubleshooting.

   - Configure Azure Monitor for AI agent telemetry.
   - Enable content recording to capture prompts and responses.
   - Create custom trace spans using OpenTelemetry.
   - View and analyze traces in Azure AI Foundry and Application Insights.
   - Build observable AI applications using production-ready monitoring and compliance practices.
  
1. Select the Python Kernel

1. Run all the cells individually to set up and build an Observable Wealth Management Advisory Agent with Telemetry and Tracing.

1. After running all the cells in the notebook, you will have successfully built an Observable Wealth Management Advisory Agent that can:

   - Capture telemetry and distributed traces for AI agent interactions.
   - Record prompts and responses for monitoring and auditing.
   - Create custom trace spans to track business-specific operations.
   - Monitor agent behavior through Azure AI Foundry and Application Insights.
   - Implement production-ready observability practices for compliance, diagnostics, and performance monitoring.
  
1. View Traces in Azure Portal:

   - Go to Azure Portal > Application Insights
   - Select Investigate > Search
   - Filter by the Trace ID shown above
  
## Task 2: Agent & Tool Evaluation

### **`observability-and-evaluations/2-agent-evaluation.ipynb`**

1. Open `observability-and-evaluations/2-agent-evaluation.ipynb`

1. This notebook demonstrates how to evaluate an Azure AI Financial Advisory Agent using Azure AI Foundry's built-in evaluators. You'll learn how to assess agent responses for quality, safety, and instruction adherence to ensure reliable and compliant AI behavior in financial services.

   - Create and configure a Financial Advisory AI agent.
   - Configure built-in evaluators to assess agent responses.
   - Run evaluations against representative financial queries.
   - Analyze evaluation results for quality, safety, and task adherence.
   - Build production-ready evaluation workflows for responsible AI applications.
  
1. Select the Python Kernel

1. Run all the cells individually to set up, build, and evaluate your Financial Advisory Agent using Azure AI Foundry Evaluators.

1. After running all the cells in the notebook, you will have successfully built and evaluated a Financial Advisory Agent that can:

   - Generate responses to financial advisory and loan-related queries.
   - Evaluate responses using built-in quality and safety evaluators.
   - Measure fluency, task adherence, and content safety.
   - Analyze evaluation results to identify areas for improvement.
   - Demonstrate production-ready AI evaluation practices for financial services applications.
  
1. Navigate to Foundry Portal > Evaluations, click on the Evaluation Run and view the results

### **`observability-and-evaluations/3-agent-evaluation-with-function-tools.ipynb`**

1. Open `observability-and-evaluations/3-agent-evaluation-with-function-tools.ipynb`

1. This notebook demonstrates how to evaluate an Azure AI Banking Agent that uses Function Tools with Azure AI Foundry Evaluators. You'll learn how to integrate custom function tools, handle tool calls during agent execution, and evaluate both the quality of responses and the correctness of tool usage.

   - Create and integrate function tools with an Azure AI agent.
   - Handle function calls and process tool outputs during agent execution.
   - Build a banking assistant with account balance lookup capabilities.
   - Evaluate tool-enabled agent responses using Azure AI Foundry evaluators.
   - Assess response quality, tool usage, and responsible AI practices.
  
1. Select the Python Kernel

1. Run all the cells individually to set up, build, and evaluate your Banking Assistant Agent with Function Tools.

1. After running all the cells in the notebook, you will have successfully built and evaluated a Banking Assistant Agent that can:

   - Invoke function tools to perform account balance lookups.
   - Process tool outputs and generate accurate banking responses.
   - Evaluate agent responses and function tool interactions.
   - Verify correct tool invocation and response quality.
   - Demonstrate production-ready evaluation practices for tool-enabled AI agents in financial services.
  
1. Navigate to Foundry Portal > Evaluations, click on the Evaluation Run and view the results

### **`observability-and-evaluations/4-tool-call-accuracy-evaluation.ipynb`**

1. Open `observability-and-evaluations/4-tool-call-accuracy-evaluation.ipynb`

1. This notebook demonstrates how to evaluate Tool Call Accuracy using Azure AI Foundry Evaluators. You'll learn how to verify whether an AI agent selects the correct function tools and supplies the appropriate parameters when responding to user requests.

   - Understand the concepts of Tool Call Accuracy evaluation.
   - Define tool schemas and expected tool calls for evaluation.
   - Create test scenarios with expected tool invocations.
   - Evaluate whether agents select the correct tools and parameters.
   - Build production-ready evaluation workflows for tool-enabled AI agents.
  
1. Select the Python Kernel

1. Run all the cells individually to set up and evaluate Tool Call Accuracy for your Banking AI Agent.

1. After running all the cells in the notebook, you will have successfully evaluated a Banking AI Agent that can:

   - Select the appropriate function tools for banking operations.
   - Invoke tools with the correct parameters based on user requests.
   - Validate tool selection against expected outcomes.
   - Measure tool call accuracy using Azure AI Foundry evaluators.
   - Demonstrate production-ready evaluation practices for reliable and compliant tool-enabled AI applications.
  
1. Navigate to Foundry Portal > Evaluations, click on the Evaluation Run and view the results

## Task 3: Red Team Security Testing 

### **`observability-and-evaluations/5-red-team-security-testing.ipynb`**

1. Open `observability-and-evaluations/5-red-team-security-testing.ipynb`

1. This notebook demonstrates how to perform AI Red Team Security Testing on an Azure AI Foundry Agent using the AI Red Teaming Agent. You'll learn how to launch automated adversarial scans, evaluate agent safety across multiple risk categories, and analyze security results using the Attack Success Rate (ASR) metric.

   - Understand AI red teaming concepts, including risk categories, attack strategies, and ASR.
   - Create a target AI agent for automated security testing.
   - Launch and monitor AI red-team scans using Azure AI Foundry.
   - Analyze scan results to identify potential safety and security vulnerabilities.
   - Build production-ready AI security validation workflows using red teaming.
  
1. Select the Python Kernel

1. Run all the cells individually to set up, configure, and perform an AI Red Team Security Scan on your Banking Assistant Agent.

1. After running all the cells in the notebook, you will have successfully performed an AI Red Team Security Assessment that can:

   - Launch automated adversarial security scans against an AI agent.
   - Evaluate agent behavior across multiple AI safety risk categories.
   - Measure the Attack Success Rate (ASR) to assess agent robustness.
   - Analyze security testing results to identify potential vulnerabilities.
   - Demonstrate production-ready AI safety validation and security testing practices using Azure AI Foundry.
  
## Task 4: Deploying Hosted Agents

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

1. Test the agent locally. Each agent has a test_local.py that builds the agent and runs one turn against your project. They read the workshop root .env (or the agent-local .env).

   ```
   python hosted-agents/benefits-review-invocations/test_local.py
   ```

1. Navigate to directory

   ```
   cd hosted-agents/benefits-advisor-responses
   ```

1. Install the extension

   ```
   azd extension install azure.ai.agents
   ```

1. Authenticate to azd cli

   ```
   azd auth login
   ```

1. Initiate and deploy the AI Agent

   ```
   azd ai agent init
   ```
   ```
   azd deploy
   ```

1. Click **Yes** on confirm installation prompt in the integrated terminal.

1. Click **Yes** for `agent.manifest.yaml`

1. Enter a name for your agent, click Enter

   ```
   benefits-advisor-responses
   ```

1. For your environemt name, enter

   ```
   benefits-advisor-responses
   ```

1. On how would you like to deploy your agent, choose **Source Code (ZIP)**

1. Choose Python 3.14 for deployment

1. File path choose main.py

1. Choose remote build

1. Choose an existing fundry resource

1. Choose subs

1. Choose the foundry resource/project

1. Choose existing model deployment gpt-5.4-mini

1. Choose 0.5 cores

1. enter a value for skills name

1. Enter a value for toolbox name

1. Run azd deploy and confirm installation by click Yes
