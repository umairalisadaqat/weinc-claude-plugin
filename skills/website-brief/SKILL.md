---
name: website-brief
description: Interview the user about their business and write a complete website brief, then start the WeInc build with start_website. Use when someone wants a new website built with WeInc.
---

# Website brief

Goal: a brief so complete that the first version of the site is close to right.

## 1. Interview (one short group of questions at a time)

Ask, and skip anything the user already told you:

1. **Business**: name, what you do, where you are (city/area served), how long in business.
2. **Audience**: who the ideal customer is and what they need most.
3. **Services or products**: the main ones, with a line each. Prices only if the user wants them shown.
4. **What visitors should do**: call, book, request a quote, buy, visit, sign up.
5. **Tone and look**: e.g. friendly, premium, bold, calm. Brand colours, fonts, or sites they like.
6. **Pages**: suggest Home, Services, About, Contact (plus Menu, Gallery, Pricing, FAQ when relevant). Let the user adjust.
7. **Contact details**: phone, email, address, opening hours, social links. Use exactly what they give; never make these up.
8. **Photos and logo**: ask whether they have their own. If they do, tell them they can add them in the WeInc editor after the build starts.
9. **Proof**: real testimonials, awards or certifications only if the user supplies them. Never invent reviews, numbers or claims.

Optional: call `find_templates` with the business type and show the user a few matching designs to choose from.

## 2. Write the brief

Show it back in this shape and ask "Anything to change?":

- Business and location
- Audience
- Services / products
- Main action for visitors
- Tone and visual style
- Pages, with 1-2 lines on what each page contains
- Contact details (exactly as given)
- Photos / logo plan
- Things to avoid

Mark anything unknown as "to be added" instead of guessing.

## 3. Start the build

When the user approves, call `start_website` with the full brief as the description (and the chosen template, if one was picked). The tool returns a link. Tell the user to open it and confirm in their browser; the build starts there, not in this chat.

Afterwards, suggest the `launch-checklist` skill before they publish.
