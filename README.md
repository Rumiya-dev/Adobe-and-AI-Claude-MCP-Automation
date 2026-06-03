# Adobe-and-AI-Claude-MCP-Automation
Adobe Claude MCP Automation — customized integration project

# Adobe Claude MCP Automation

A portfolio project focused on connecting Claude Desktop with Adobe Photoshop, Adobe InDesign, Adobe Illustrator and the local filesystem through MCP server automation.

This project is based on customizing and configuring existing MCP server workflows for Adobe applications. The goal was to enable Claude to interact with Adobe tools locally and support AI-assisted automation workflows.

## Features

- Claude Desktop integration with multiple MCP servers
- Adobe Photoshop MCP server configuration
- Adobe InDesign MCP server configuration
- Adobe Illustrator MCP server configuration
- Local filesystem MCP server setup
- Example Claude Desktop MCP configuration
- Adjustments and fixes for existing MCP server code
- Local automation workflow for Adobe applications

## Tech Stack

- Python
- Node.js / npx
- MCP servers
- Claude Desktop
- Adobe Photoshop
- Adobe InDesign
- Adobe Illustrator
- Local filesystem automation

My Contribution
Configured Claude Desktop to run multiple MCP servers
Connected Claude with Adobe Photoshop, InDesign and Illustrator workflows
Adjusted local Python server paths and startup commands
Tested local MCP server communication
Fixed setup and integration issues in existing MCP server files
Added a filesystem MCP server for local file access during automation tests
Prepared a safe example configuration without private paths or secrets
Example Use Cases
Ask Claude to interact with Adobe Photoshop through a local MCP server
Ask Claude to work with Adobe InDesign automation scripts
Test AI-assisted document and design automation workflows
Allow Claude to access a controlled local project folder through filesystem MCP
Important Note

This repository does not include API keys, private Claude configuration files, company documents, client files, real Adobe project files, or commercial materials.

The configuration file in this repository is an example only. Local paths must be adjusted by each user.


## MCP Configuration

The project uses a Claude Desktop configuration file to register multiple MCP servers.

Example:

```json
{
  "mcpServers": {
    "photoshop": {
      "command": "C:\\path-to-project\\.venv\\Scripts\\python.exe",
      "args": [
        "C:\\path-to-project\\mcp\\ps-mcp.py"
      ]
    },
    "indesign": {
      "command": "C:\\path-to-project\\.venv\\Scripts\\python.exe",
      "args": [
        "C:\\path-to-project\\mcp\\id-mcp.py"
      ]
    },
    "illustrator": {
      "command": "C:\\path-to-project\\.venv\\Scripts\\python.exe",
      "args": [
        "C:\\path-to-project\\mcp\\ai-mcp.py"
      ]
    },
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "C:\\path-to-test-folder"
      ]
    }
  }
}
