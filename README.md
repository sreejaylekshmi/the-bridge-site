# Consultancy Website

Personal site: marketing data consultant, Cambridge. Plain HTML/CSS — no build
tools, no frameworks — so every file is readable, editable, and hosted free.

## Structure

```
index.html                  the whole main site (styles are inside it, in <style>)
blog/index.html             blog listing page
blog/posts/…                one HTML file per post (first post doubles as template)
images/                     put photos here, reference as images/filename.jpg
```

## Host it free on GitHub Pages

1. Create a repo on github.com (e.g. `yourname-site`). Public repo = free Pages.
2. Push this folder:
   ```bash
   git remote add origin git@github.com:YOURUSER/yourname-site.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Source: Deploy from branch → main / (root) → Save**
4. Two minutes later your site is live at `https://YOURUSER.github.io/yourname-site/`
5. Own domain later (~£12/yr): buy it, then Settings → Pages → Custom domain,
   and point the domain's DNS (CNAME → YOURUSER.github.io) at GitHub.

Every future edit = commit + push, live in ~1 minute. That IS your version control.

## Editing guide (start here)

Search `index.html` for **EDIT ME** — every place needing your real details is
marked: name (2 places), email (2 places), LinkedIn URL, About text.

| Want to… | Do this |
|---|---|
| Change colours/fonts | Edit the `:root { }` block at the top of each file's `<style>` |
| Add a blog post | Copy the post in `blog/posts/`, rename (keep `YYYY-MM-` prefix), write it, add a link block to `blog/index.html` **and** the teaser on `index.html` |
| Turn on testimonials | In `index.html`, find the TESTIMONIALS comment block and remove the comment markers as instructed there |
| Add a photo | Drop it in `images/`, then `<img src="images/me.jpg" alt="describe it">` |

## Later (when you're ready)

- **Analytics:** create a GA4 property and paste its snippet before `</head>`
  in each file — you of all people should practise what you preach.
- **Contact form:** the mailto link is fine to start. When you want a real form,
  formspree.io free tier works on static sites with three lines of HTML.
