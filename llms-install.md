# Installing the WeInc MCP server

WeInc (https://we.inc) is a hosted (remote) MCP server. There is nothing to clone, build or run locally.

1. Add this server to the MCP settings file:

```json
{
  "mcpServers": {
    "weinc": {
      "type": "streamableHttp",
      "url": "https://my.we.inc/api/mcp"
    }
  }
}
```

Use `"type": "http"` instead if the client does not recognise `streamableHttp`.

2. No API key or environment variables are needed. On first use the client opens a browser window where the user signs in to their WeInc account (OAuth 2.1 with dynamic client registration). A free account can be created at https://we.inc.

3. Verify by listing tools. Expected tools: create_website_from_template, publish_website, start_website, find_templates, my_websites, website_details, request_change.
