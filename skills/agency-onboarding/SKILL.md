---
name: agency-onboarding
description: Help an agency set up a new client in WeInc with the client and project tools - create the client, create the project, share previews. Use when an agency or reseller onboards a client or manages client sites.
---

# Agency onboarding

These tools only work for accounts with agency (white-label) access. If a tool says the account lacks access, tell the user and stop; do not retry other ways.

## 1. Look before creating

- `list_clients`: check the client does not already exist (avoid duplicates).
- `list_plans`: show the plans available to assign, if the user asks about plans.
- `list_templates`: show design options for the client's industry.

## 2. Create the client

Collect: client business name, contact name, contact email (lowercase it), and the plan if the agency assigns one. Confirm with the user, then call `create_client`. Do not invent contact details.

## 3. Create the site

Gather a short brief (business, audience, services, main action, pages, contact details, style); the `website-brief` skill's interview works well here. Confirm, then call `create_project` for that client with the brief and any chosen template.

## 4. Review and share

- `get_project` to check status.
- `get_preview_urls` to get links the agency can send the client.
- `update_project` for changes the agency asks for (name, details).
- `list_projects` to see all client sites; `get_analytics` for a site's traffic when asked.

Report what was created with the links returned. Never claim a site is published unless the tools say so.
