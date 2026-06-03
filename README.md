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
