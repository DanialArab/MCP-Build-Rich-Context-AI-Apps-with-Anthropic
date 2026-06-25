# MCP: Build Rich-Context AI Apps with Anthropic

## Intro 
- The Model Context Protocol, or MCP, is an open protocol that standardizes how your LLM applications can get access to context in terms of tools and data resources based on the client-server architecture.
- It defines how communication takes place between an MCP client hosted inside your own LLM application, and an MCP server that exposes tools and data resources and prompt templates to your application.
- MCP is model agnostic and is designed to be easy to plug into multiple applications. Say you're building a research assistant agent, and you'd like for this agent to interact with your GitHub repos, read notes from your Google Drive documents, maybe create a summary stored in your local system. Instead of you writing your own custom LLM tools, you can connect your agent to the GitHub, Google Drive and File System service, which will provide the tool or the API call definitions and also handle the tool execution.
- We'll first dive into the details of the MCP client-server architecture. You'll then work on a chatbot application to make it MCP compatible. You'll build and test an MCP server and connect your chatbot to it. Your MCP server will provide tools, prompt templates, and resources to your chatbot. You'll also connect your chatbot to other trusted third-party servers to extend its capabilities. You'll then re-use your MCP server and connect it to other MCP applications like Claude Desktop. Finally, you'll learn how you can deploy your MCP server remotely.
- MCP is a really important technology that's making it much easier for LLM application developers to connect the systems to many tools and data resources. And for teams building tools or providing data, it is also making it much easier to make what they build available to many developers. So this is a technology worth learning about.

## Why MCP

 - We learn why connecting LLM applications to resources had been so difficult before, and how MCP addresses this.
 - MCP makes AI development less fragmented and it standardizes connections between AI applications and external data sources.

![](https://github.com/DanialArab/images/blob/main/MCP%3A%20Build%20Rich-Context%20AI%20Apps%20with%20Anthropic/context_importance.png)

Everything that you're going to see with MCP can be done without MCP, but as we think about a world in which many different models communicate with many different data sources, and even with each other, we want to make sure that we're speaking the same language. We want to standardize how our AI applications interact with external systems, instead of building the same integration for a different data source over and over and over again, depending on the model or the data source, we're instead going to build once and use everywhere. The Model Context Protocol borrows a lot of its ideas from other protocols that aim to achieve similar kind of ideas. For example, LSP, or the Language Server Protocol developed in 2016 by Microsoft, standardizes how integrated development environments interact with language-specific tools. When you create extensions for particular languages for particular development environments, you don't want to have to write that over and over again for all of those development environments. So while MCP is very novel and what it's trying to do, it stands on the shoulders of many other protocols and ideas around standardization.

![](https://github.com/DanialArab/images/blob/main/MCP%3A%20Build%20Rich-Context%20AI%20Apps%20with%20Anthropic/MCP.png)


<img width="1535" height="601" alt="image" src="https://github.com/user-attachments/assets/c1aeb59a-1753-4719-b0bd-19d1b9e3e987" />

## MCP Architecture

MCP is based on a client-server architecture.

<img width="1734" height="686" alt="image" src="https://github.com/user-attachments/assets/719ac49f-d337-45f6-9de5-20e5777c99b6" />

<img width="1591" height="941" alt="image" src="https://github.com/user-attachments/assets/3c5fe490-0f98-43bf-8b22-363c1dbdcac4" />

<img width="1828" height="788" alt="image" src="https://github.com/user-attachments/assets/03b78068-fe5a-47c1-8cce-1b4bb2723eb0" />

<img width="1783" height="870" alt="image" src="https://github.com/user-attachments/assets/e092c2c4-4be5-4b77-8122-4734a33e5e49" />

<img width="1598" height="839" alt="image" src="https://github.com/user-attachments/assets/3b949f44-76cf-4fa2-8317-1a5450df1a86" />

<img width="1791" height="799" alt="image" src="https://github.com/user-attachments/assets/2c7fae25-0b67-45b0-9ca8-e00e1c11d892" />

<img width="1880" height="964" alt="image" src="https://github.com/user-attachments/assets/71a501c0-57d5-412b-acda-b1a40a7f8917" />

<img width="1853" height="829" alt="image" src="https://github.com/user-attachments/assets/9d011404-14c5-421c-9edd-7490d819a2f2" />

<img width="1238" height="742" alt="image" src="https://github.com/user-attachments/assets/0d773005-eb43-4f96-befd-a94099f07457" />

<img width="1356" height="814" alt="image" src="https://github.com/user-attachments/assets/379362a0-8fd6-45df-b49f-24500962cbea" />

<img width="1885" height="718" alt="image" src="https://github.com/user-attachments/assets/14e5277b-4dad-4f2b-9504-ad8acfec9a67" />

<img width="1217" height="947" alt="image" src="https://github.com/user-attachments/assets/3e9734fe-cf2b-4373-97ff-b5099f6b7e4c" />

<img width="911" height="1642" alt="image" src="https://github.com/user-attachments/assets/5ec3ba23-7890-4fef-aff0-8b45ce049cb4" />



