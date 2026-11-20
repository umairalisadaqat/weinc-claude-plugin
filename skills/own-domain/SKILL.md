---
name: own-domain
description: Use when the user wants their site on its own address, for example "get a domain", "is this name available", "use my own domain", "put my site on mybusiness.com", "I want a proper link". Checks a domain name and puts a WeInc site on it.
---

# Own domain

1. Find the site with `my_websites` if it is not clear which one they mean.
2. To see whether a name is free, call `check_domain` with the name they gave and share the result as returned.
3. If they already own the domain, call `connect_domain` with the site and the domain, then pass on the setup steps it returns exactly.
4. If the site is not live yet, offer to publish it with `publish_website` and do so only on their yes.

Every published site also has a free weinc.app link, so the user always has a working address while a domain is being set up.
