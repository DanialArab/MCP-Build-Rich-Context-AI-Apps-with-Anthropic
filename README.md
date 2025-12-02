# MCP: Build Rich-Context AI Apps with Anthropic

- The Model Context Protocol, or MCP, is an open protocol that standardizes how your LLM applications can get access to context in terms of tools and data resources based on the client-server architecture.
- It defines how communication takes place between an MCP client hosted inside your own LLM application, and an MCP server that exposes tools and data resources and prompt templates to your application.
- MCP is model agnostic and is designed to be easy to plug into multiple applications. Say you're building a research assistant agent, and you'd like for this agent to interact with your GitHub repos, read notes from your Google Drive documents, maybe create a summary stored in your local system. Instead of you writing your own custom LLM tools, you can connect your agent to the GitHub, Google Drive and File System service, which will provide the tool or the API call definitions and also handle the tool execution.

