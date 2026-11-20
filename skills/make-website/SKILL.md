---
name: make-website
description: Use when the user asks for a website, for example "make me a website", "build a site for my business", "I need a landing page", "a page for my event". Builds a live-ready WeInc site in seconds from what the user has already said, then publishes it when they say yes.
---

# Make a website

Build the site from what the user has already told you. Do not interview them.

1. If the business name or what the business does is missing, ask one short question that covers both. Otherwise go straight to step 2.
2. Call `create_website`. Write the headline, subheadline, about text, services, highlights and FAQ from the user's own words. Pass only facts they gave: leave out phone numbers, emails, addresses, opening hours, costs, reviews or awards they did not mention.
3. Show the preview and editor link, and ask if they want it live.
4. Call `publish_website` only after the user says yes. Share the live link it returns.

Changes afterwards: use `read_website` and `edit_website` for wording, then publish again so the live site shows the change. `my_websites` lists their sites. `website_enquiries` shows messages visitors sent through the contact form.

If the WeInc tools are not connected, tell the user to connect WeInc (in Claude Code: `/mcp`, pick **weinc**, sign in).
