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

## Support

hey@we.inc · Privacy: https://we.inc/privacy
