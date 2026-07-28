#  Agentic AI Immersion Workshop

### Overall Estimated Duration: 4 Hours 

## 📘 Lab Scenario

Contoso, a global retail organization, is looking to transform how employees and customer service teams access business information. Product catalogs, promotional campaigns, customer benefits, and operational policies are currently distributed across multiple repositories, making it difficult to quickly find accurate and consistent information.

To address this challenge, Contoso is implementing an AI-powered knowledge and decision platform using **Microsoft Foundry**. The solution enables intelligent agents to access trusted enterprise knowledge, understand user intent, and provide accurate, context-aware responses for product discovery, promotional inquiries, and inventory-related questions. By leveraging specialized agents and centralized knowledge sources, Contoso aims to improve customer experiences, streamline business operations, and empower users with faster access to actionable information through natural language interactions.

## 📖 Lab Overview

In this lab, you will learn how to build an enterprise-grade AI solution using **Microsoft Foundry**. You will start by integrating **enterprise knowledge** from business applications, databases, and document repositories to support AI-driven experiences.

Next, you will create **specialized AI agents**, enable tool calling and knowledge grounding, and orchestrate agent interactions through **workflows**. Finally, you will implement **observability**, **evaluations**, and **guardrails** to ensure secure, reliable, and governed AI operations. By completing this lab, you will gain hands-on experience building, managing, and governing intelligent agent-based solutions in Microsoft Foundry.

## 🎯Lab Objectives

- **Exercise 1: Foundry IQ Knowledge Integration:** In this exercise, participants will integrate enterprise knowledge into Microsoft Foundry using Foundry IQ by connecting Azure Blob Storage, Azure AI Search. By the end, they will gain hands-on experience in creating knowledge bases that enable secure, context-aware AI responses grounded in enterprise data.

- **Exercise 2: Build an Intelligent Agent:** In this exercise, participants will create specialized AI agents, define agent personas and instructions, attach enterprise knowledge sources, and implement tool-calling capabilities. By the end, they will gain practical experience building intelligent agents that can reason over structured and unstructured business data.

- **Exercise 3: Multi-Agent Orchestration and Validation:** In this exercise, participants will configure workflows to orchestrate multiple AI agents, enabling coordinated decision-making across business processes. They will validate end-to-end agent interactions, inspect execution paths, and gain hands-on experience in enterprise-scale agent orchestration.

- **Exercise 4: Observability, Evaluation, and Guardrails:** In this exercise, participants will implement guardrails, evaluations, and observability capabilities using Microsoft Foundry. They will configure responsible AI policies, evaluate agent performance, and monitor agent behavior to ensure secure, reliable, and governed AI operations.

## ⚙️ Prerequisites

Before starting this lab, ensure you have the following:

- An active Azure subscription with permissions to create and manage Azure resources.
- Access to Microsoft Foundry and the ability to create Foundry projects.
- Sufficient quota to deploy Azure OpenAI models, including gpt-5 and text-embedding-3-large.
- Permissions to create and manage Azure AI Search and Azure Blob Storage resources.
- An Azure AI Search index populated with relevant business data that can be used as a knowledge source for agent retrieval and grounding.
- An Azure Blob Storage container containing enterprise documents or knowledge assets that will be used by agents for contextual responses.
- Basic familiarity with Azure Portal navigation and cloud concepts.
- Basic understanding of AI agents, Retrieval-Augmented Generation (RAG), and enterprise knowledge retrieval.

## 🏗️ Architecture

The architecture uses **Microsoft Foundry IQ** as the central platform for building and orchestrating intelligent AI agents. User requests are first received by the **Supervisor Agent**, which analyzes the intent and routes the query to the most appropriate specialized agent, such as the **Sales Associate Agent** for product recommendations, the **Inventory Agent** for product catalog inquiries, or the **Rewards Campaign Agent** for promotional and return policy questions. These agents are powered by **Azure OpenAI models** and managed through **Microsoft Foundry Agent Service**, enabling intelligent reasoning and response generation. To provide grounded and accurate answers, Foundry IQ retrieves enterprise knowledge from **Azure AI Search**, which contains the indexed product catalog, and **Azure Blob Storage**, which stores business documents such as the Black Friday policy. This architecture enables agents to deliver context-aware, enterprise-ready responses while ensuring that all outputs are based on trusted organizational knowledge sources.

## 🖼️ Architecture Diagram

![](../media/foundry-iq-lab-architecture-diagram.png)

## 🔍 Explanation of Components

- **Foundry IQ:** Connects Azure AI Search and Azure Blob Storage as enterprise knowledge sources, enabling agents to retrieve grounded business information and generate context-aware responses.

- **Microsoft Foundry Project:** Provides the central workspace where AI models, knowledge sources, agents, and orchestration workflows are created and managed.

- **Azure AI Search:** Stores and indexes the product catalog, allowing agents to perform keyword and semantic searches to retrieve relevant product information.

- **Azure Blob Storage:** Stores enterprise documents such as the Black Friday policy, which are used by agents as a trusted knowledge source.

- **Azure OpenAI Models:** Provides the foundational AI capabilities for the lab, where **gpt-5** is used for reasoning, orchestration, and response generation, while **text-embedding-3-large** generates embeddings to enable semantic search and knowledge retrieval across enterprise data.

- **Microsoft Foundry Agent Service:** Hosts and manages the AI agents, enabling agent execution, orchestration, and interaction with connected tools and knowledge sources.

- **Agent Orchestration:** Coordinates interactions between multiple agents to ensure user requests are handled by the most relevant specialized agent.

- **Knowledge Sources:** Provides the trusted business context used by agents to generate accurate, grounded, and enterprise-ready responses.

## 🚀 Getting Started with the lab

Welcome to you **Foundry IQ - Business Intelligence to Intelligent Action** workshop! We've prepared an immersive environment for you to discover how Microsoft Foundry enables intelligent agents to retrieve enterprise knowledge, reason over business data, and drive actionable outcomes. Let's begin by making the most of this experience!

## Accessing Your Lab Environment

Once you're ready to dive in, your virtual machine and **Guide** will be right at your fingertips within your web browser.

![](../media/gs-03.png)

## Lab Guide Zoom In/Zoom Out

To adjust the zoom level for the environment page, click the **A↕** icon located next to the timer in the lab environment.

![](../media/zoom-new.png)

## Resize the Virtual Machine View
 
Use the **slider (three vertical dots)** located between the **Virtual Machine** and the **Lab Guide** panes to adjust the display size, allowing you to customize the layout based on your preference.

![](../media/vmresize-foundry.png)

## Virtual Machine & Lab Guide

Your virtual machine is your workhorse throughout the workshop. The lab guide is your roadmap to success.

## Exploring Your Lab Resources

To get a better understanding of your lab resources and credentials, navigate to the **Environment** tab.

![](../media/n-evn-aidev.png)

## Utilizing the Split Window Feature

For convenience, you can open the lab guide in a separate window by selecting the **Split Window** button from the Top right corner.

![](../media/fabric-iq-split-window-01.png)

## Managing Your Virtual Machine

Feel free to **Start, Stop, or Restart (2)** your virtual machine as needed from the **Resources (1)** tab. Your experience is in your hands!

![](../media/resources-01.png)

## 🌐 Let's Get Started with Azure Portal

1. On your virtual machine, click on the **Azure Portal** icon.

    ![](../media/ap-01.png)

2. You'll see the **Sign into Microsoft Azure** tab. Here, enter your credentials:

   - **Email/Username:** <inject key="AzureAdUserEmail"></inject>

     ![](../media/ap-02.png)

3. Next, provide your Temporary Access Pass:

   - **Temporary Access Pass:** <inject key="AzureAdUserPassword"></inject>

     ![](../media/ap-03.png)

1. If prompted to stay signed in, you can click **Yes**.

   ![Stay Signed in](../media/ap-04.png)     

1. If a **Welcome to Microsoft Azure** pop-up window appears, simply click **Maybe later** to skip the tour.

   ![Stay Signed in](../media/maybelaterimage.png)

## 📞 Support Contact

The **CloudLabs support** team is available 24/7, 365 days a year, via email and live chat to ensure seamless assistance at any time. We offer dedicated support channels tailored specifically for both learners and instructors, ensuring that all your needs are promptly and efficiently addressed.

Learner Support Contacts:

- Email Support: [cloudlabs-support@spektrasystems.com](mailto:cloudlabs-support@spektrasystems.com)
- Live Chat Support: https://cloudlabs.ai/labs-support

Click **Next** from the bottom right corner to embark on your Lab journey!

![](../media/nextpage.png)

## Happy Learning!!!
