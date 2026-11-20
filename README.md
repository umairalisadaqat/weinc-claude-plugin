# WeInc plugin for Claude Code

Connects Claude to WeInc (https://we.inc): a live website with its own link in seconds, without leaving the chat. Adds three skills:

- **make-website**: "make me a website". Builds a site from what you already said and publishes it when you say yes.
- **put-page-online**: "put this online". Takes a page or artifact from the chat and gives it its own live link.
- **own-domain**: "get a domain". Checks a name and puts your site on a domain you own.

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

- "Make me a website for my bakery" (or `/weinc:make-website`)
- "Put this page online" (or `/weinc:put-page-online`)
- "Put my site on mybakery.com" (or `/weinc:own-domain`)

## WeInc MCP server (any MCP client)

- Homepage: https://we.inc
- Remote MCP URL: `https://my.we.inc/api/mcp` (Streamable HTTP)
- Sign-in: OAuth 2.1 with dynamic client registration, so your client opens a WeInc sign-in page on first use. No API key.
- Official MCP Registry name: `io.github.umairalisadaqat/weinc`


### Main tools

All tools work on your own WeInc websites only. Nothing goes public until you say yes.

| Tool | What it does |
| --- | --- |
| `create_website` | Builds a complete draft website in your account in seconds from what you described. |
| `import_page` | Saves a page from the chat (an artifact or any HTML) as a website, and puts it live if you asked. |
| `publish_website` | Puts one of your websites online and returns its live link. |
| `read_website` / `edit_website` | Reads and changes a site's wording from the chat. |
| `check_domain` | Looks up whether a domain name is available. |
| `connect_domain` | Puts a site on a domain you already own. |
| `my_websites` | Lists your websites with status and live address. |
| `website_enquiries` | Shows messages visitors sent through a site's contact form. |

## Support

hey@we.inc · Privacy: https://we.inc/privacy
