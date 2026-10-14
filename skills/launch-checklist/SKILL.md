---
name: launch-checklist
description: Pre-publish check for a WeInc website - domain, contact details, SEO title and description, mobile view - then queue fixes with request_change. Use when the user is about to publish or launch a WeInc site.
---

# Launch checklist

## 1. Pick the site

Call `my_websites` and ask which site to check (skip if only one). Then call `website_details` for it. Only report what the tool actually returns; if something is not in the result, say you could not check it and ask the user to look in the editor.

## 2. Walk through, one item at a time

For each item, say what you found, then ask the user to confirm or correct it.

1. **Domain**: is a custom domain connected, or is the site still on its WeInc address? If they want their own domain, point them to the domain settings in the WeInc editor.
2. **Contact details**: phone, email, address, hours. Ask the user to confirm each one is correct and current. Placeholder-looking values (555 numbers, example.com, "Your Business") must be fixed.
3. **SEO title and description**: the title should name the business and what/where (about 50-60 characters). The description should say what the business offers and the main action (about 140-160 characters). Draft better versions if needed.
4. **Mobile**: ask the user to open the preview on their phone (or the editor's mobile view) and check: menu opens, text is readable, buttons are tappable, nothing overflows sideways. If `website_details` returns preview links, share them.
5. **Content truth**: no invented reviews, statistics, awards or prices the user did not give.
6. **Calls to action**: every main page leads to the action the user wants (call, book, quote).

## 3. Queue fixes

Collect all agreed fixes into one clear list and call `request_change` with it for that site. The tool opens the WeInc editor with the change pre-filled; the user reviews and sends it there. Tell them to re-run this checklist after the change lands, then publish from the editor.
