[![MseeP.ai Security Assessment Badge](https://mseep.net/mseep-audited.png)](https://mseep.ai/app/hanweg-mcp-pdf-tools)

# WORK IN PROGRESS - USE WITH CAUTION - Windows:

# MCP PDF Tools Server

An MCP (Model Context Protocol) server that provides PDF manipulation tools. This server allows LLMs to perform operations like merging PDFs and extracting pages through the Model Context Protocol.

<a href="https://glama.ai/mcp/servers/fqtuoh05xi"><img width="380" height="200" src="https://glama.ai/mcp/servers/fqtuoh05xi/badge" alt="mcp-pdf-tools MCP server" /></a>

## Features

- Merge multiple PDF files into a single PDF
- Merge multiple PDF files into a single PDF in user specified order
- Extract specific pages from a PDF file
- Search PDFs *filesystem search or Everything search works better than this*
- Find (and merge) related PDFs based on text extraction and regex pattern matching from a target input PDF

## Installation

1. Clone this repository
2. 
```bash
cd mcp-pdf-tools

# Create and activate virtual environment
uv venv
.venv\Scripts\activate

# Install the package
uv pip install -e .
```

## Usage with Claude Desktop

Add this to your Claude Desktop configuration file (claude_desktop_config.json):

```json
{
    "mcpServers": {
        "pdf-tools": {
            "command": "uv",
            "args": [
                "--directory",
                "PATH_TO\\mcp-pdf-tools",
                "run",
                "pdf-tools"
            ]
        }
    }
}
```
