# HubSpot MCP

[![Verified by MCPForge](https://www.mcpforge.tech/api/badge/verified/hubspot-mcp)](https://www.mcpforge.tech/verified/hubspot-mcp)
[![smithery badge](https://smithery.ai/badge/kamolc4/hubspot-mcp)](https://smithery.ai/servers/kamolc4/hubspot-mcp)

MCP server for the [HubSpot CRM API](https://developers.hubspot.com/docs/api/overview), generated with [MCPForge](https://mcpforge.tech).

This MCP server exposes core HubSpot CRM operations as tools that Claude and other MCP-compatible AI agents can call directly — from managing contacts and deals to tracking companies and logging notes.

---

## Live Endpoint

```
https://www.mcpforge.tech/api/servers/hubspot-mcp-x44l7
```

No setup required — connect Claude Desktop or any MCP client to this endpoint and start using it immediately.

---

## Usage

### Claude Desktop

Add this to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "hubspot-mcp": {
      "url": "https://www.mcpforge.tech/api/servers/hubspot-mcp-x44l7",
      "transport": "http"
    }
  }
}
```

Config file location:
- **macOS**: `~/Library/Application Support/Claude/claude_desktop_config.json`
- **Windows**: `%APPDATA%\Claude\claude_desktop_config.json`

### Cursor

Add to your Cursor MCP settings:

```json
{
  "mcpServers": {
    "hubspot-mcp": {
      "url": "https://www.mcpforge.tech/api/servers/hubspot-mcp-x44l7",
      "transport": "http"
    }
  }
}
```

---

## Available Tools

12 tools across contacts, deals, companies, and notes:

### Contacts

| Tool | Description |
|------|-------------|
| `getContact` | Retrieve a contact by ID |
| `createContact` | Create a new CRM contact |
| `updateContact` | Update an existing contact's properties |
| `listContacts` | List contacts with optional filters |

### Deals

| Tool | Description |
|------|-------------|
| `getDeal` | Retrieve a deal by ID |
| `createDeal` | Create a new deal in the pipeline |
| `updateDeal` | Update deal properties or stage |
| `listDeals` | List deals with optional filters |

### Companies

| Tool | Description |
|------|-------------|
| `getCompany` | Retrieve a company by ID |
| `createCompany` | Create a new company record |
| `listCompanies` | List companies with optional filters |

### Notes

| Tool | Description |
|------|-------------|
| `createNote` | Log a note against a contact, deal, or company |

### Requires Approval ⚠️

These tools permanently delete CRM records and require human approval before execution:

| Tool | Description |
|------|-------------|
| `deleteContact` | Permanently delete a contact _(approval required)_ |
| `deleteDeal` | Permanently delete a deal _(approval required)_ |

> Configure approval workflows in your MCPForge dashboard under **Governance → Approvals** to require human sign-off before these tools execute.

---

## Security Report

**Security Score: 80 / 100 · Verified**

| Dimension | Result |
|-----------|--------|
| Tool Quality Score | 78 / 100 |
| Standard tools | 12 |
| Approval-required tools | 2 |
| Governance controls | 3 / 5 |

Full report: [mcpforge.tech/verified/hubspot-mcp](https://www.mcpforge.tech/verified/hubspot-mcp)

---

## Generated with MCPForge

[MCPForge](https://mcpforge.tech) converts any OpenAPI spec into a hosted, governed MCP server in under 60 seconds.

- **Verify** any MCP server for free at [mcpforge.tech/verify](https://mcpforge.tech/verify)
- **Browse** the verified MCP directory at [mcpforge.tech/verified](https://mcpforge.tech/verified)
- **Generate** your own MCP server at [mcpforge.tech](https://mcpforge.tech)
