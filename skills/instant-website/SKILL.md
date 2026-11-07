---
name: instant-website
description: Make a finished WeInc website for the user's business in seconds and, if they want, put it online. Use when someone asks for a website and wants it now, without a long interview.
---

# Instant website

Goal: the user has a real website in their WeInc account within a minute, and a live address if they want one.

## 0. Make sure WeInc is connected

If the WeInc tools are not available or say you are not signed in, tell the user how to connect, then continue:
- Claude Code: run `/mcp`, pick **weinc** and sign in (a WeInc account is free to create on the sign-in page).
- Claude web, desktop or mobile: open https://claude.ai/directory/weinc, choose Connect and sign in.

## 1. Get the basics (one short message)

You need the business name and what the business does. City, phone, email and a one-line description help. Skip anything the user already said. Never make up contact details, reviews or numbers.

## 2. Make the site

Call `create_website_from_template` with what you have. Leave `template_id` out to get the best-matching design, or call `find_templates` first if the user wants to choose a look. This uses no AI credits.

Show the result: the site name, the preview and the editor link.

## 3. Offer to publish

Ask: "Want me to put it online now?" Only if the user says yes, call `publish_website` with the site id. Share the live address it returns. If the free plan's limit is reached, say so plainly and share the link the tool returns.

## 4. Next steps

Offer to change anything ("change the headline", "add opening hours") with `request_change`, or a custom AI-designed site with the `website-brief` skill.
