# MCP: Build Rich-Context AI Apps with Anthropic

## Intro 
- The Model Context Protocol, or MCP, is an open protocol that standardizes how your LLM applications can get access to context in terms of tools and data resources based on the client-server architecture.
- It defines how communication takes place between an MCP client hosted inside your own LLM application, and an MCP server that exposes tools and data resources and prompt templates to your application.
- MCP is model agnostic and is designed to be easy to plug into multiple applications. Say you're building a research assistant agent, and you'd like for this agent to interact with your GitHub repos, read notes from your Google Drive documents, maybe create a summary stored in your local system. Instead of you writing your own custom LLM tools, you can connect your agent to the GitHub, Google Drive and File System service, which will provide the tool or the API call definitions and also handle the tool execution.
- We'll first dive into the details of the MCP client-server architecture. You'll then work on a chatbot application to make it MCP compatible. You'll build and test an MCP server and connect your chatbot to it. Your MCP server will provide tools, prompt templates, and resources to your chatbot. You'll also connect your chatbot to other trusted third-party servers to extend its capabilities. You'll then re-use your MCP server and connect it to other MCP applications like Claude Desktop. Finally, you'll learn how you can deploy your MCP server remotely.
- MCP is a really important technology that's making it much easier for LLM application developers to connect the systems to many tools and data resources. And for teams building tools or providing data, it is also making it much easier to make what they build available to many developers. So this is a technology worth learning about.

## Why MCP 

 wE LEARN why connecting LLM applications to resources had been so difficult before, and how MCP addresses this.

 
