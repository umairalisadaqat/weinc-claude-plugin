---
name: put-page-online
description: Use when the user has a page, artifact or HTML in the chat and says things like "put this online", "publish this page", "host this", "give me a link to share this". Saves that exact page as a WeInc website with its own link.
---

# Put a page online

1. Take the finished page from the chat as one complete HTML document, with its styles and scripts inside. Do not rewrite or redesign it.
2. Call `import_page` with that HTML and a short site name. For a site with several pages, send the home page as `html` and the others in `pages` with short addresses such as "about".
3. If the user already asked for it to be public ("put it online", "publish it"), pass `confirmed: true` so it goes live in the same call. Otherwise it is saved as a private draft; publish with `publish_website` once they say yes.
4. Share the live link.

To update a page that is already saved, send the changed page again with its `projectId`.
