# WeInc plugin for Claude Code

Connects Claude Code to WeInc (https://we.inc) and adds three skills:

- **website-brief**: interviews you about your business, writes a full brief, and starts the build (you confirm in your browser).
- **launch-checklist**: before publishing, checks domain, contact details, SEO title/description and mobile view, then opens the editor with fixes pre-filled.
- **agency-onboarding**: for agency accounts: create a client, create their site, share preview links.

## Install

Inside Claude Code:

```
/plugin marketplace add umairalisadaqat/weinc-claude-plugin
/plugin install weinc@weinc
```

Or from your shell:

```
claude plugin marketplace add umairalisadaqat/weinc-claude-plugin
claude plugin install weinc@weinc
```

To try it from a local copy: `claude plugin marketplace add .`.

Then run `/mcp`, pick **weinc**, and sign in with your WeInc account. The connection uses `https://my.we.inc/api/mcp` with standard sign-in (OAuth); no API key needed.

## Use

- "Build me a website for my bakery" (or `/weinc:website-brief`)
- "I'm about to publish, check my site" (or `/weinc:launch-checklist`)
- "Onboard a new client for my agency" (or `/weinc:agency-onboarding`)

## WeInc MCP server (any MCP client)

- Homepage: https://we.inc
- Remote MCP URL: `https://my.we.inc/api/mcp` (Streamable HTTP)
- Sign-in: OAuth 2.1 with dynamic client registration, so your client opens a WeInc sign-in page on first use. No API key.
- Official MCP Registry name: `io.github.umairalisadaqat/weinc`

### One-click install

- Cursor: [Add WeInc to Cursor](https://cursor.com/install-mcp?name=weinc&config=eyJ1cmwiOiJodHRwczovL215LndlLmluYy9hcGkvbWNwIn0=)
- VS Code: [Add WeInc to VS Code](https://insiders.vscode.dev/redirect/mcp/install?name=weinc&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fmy.we.inc%2Fapi%2Fmcp%22%7D)
- Claude Code: `claude mcp add --transport http weinc https://my.we.inc/api/mcp`
- Claude.ai / ChatGPT and other clients: add `https://my.we.inc/api/mcp` as a custom connector.

Manual config for clients that read `mcp.json`:

```json
{
  "mcpServers": {
    "weinc": {
      "type": "http",
      "url": "https://my.we.inc/api/mcp"
    }
  }
}
```

### Tools (15)

For your own websites:

| Tool | What it does |
| --- | --- |
| `start_website` | Prepares a new website from a description of the business. Returns a link; nothing is built or charged until you confirm in your browser. |
| `find_templates` | Searches WeInc website templates by keyword or category. |
| `my_websites` | Lists your websites with live URL, editor link and last update. |
| `website_details` | Shows one website: published state, live URL, custom domains, last publish time. |
| `request_change` | Prepares a change to one of your websites and returns an editor link with the instruction already typed in. |

For agency (organization) accounts:

| Tool | What it does |
| --- | --- |
| `list_projects` | Lists the organization's builder projects. |
| `create_project` | Creates a project for one of your clients. |
| `get_project` | Gets one project by id. |
| `update_project` | Updates a project's name, description or status. |
| `get_preview_urls` | Gets published and preview URLs for a project. |
| `list_clients` | Lists your clients. |
| `create_client` | Creates a client. |
| `list_templates` | Lists your organization's templates. |
| `list_plans` | Lists your client-facing plans. |
| `get_analytics` | Aggregated analytics for the organization or one project. |

## Support

hey@we.inc · Privacy: https://we.inc/privacy
