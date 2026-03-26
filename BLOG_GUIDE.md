# Blog Folder Structure Guide

## Your Content (the files you write)

| File/Folder | What it does |
|---|---|
| `_posts/` | Standard blog posts. Files must be named `YYYY-MM-DD-title.md` |
| `_blogs/` | Your Blog section posts (add `.md` files here) |
| `_books/` | Your Book section posts |
| `_recipes/` | Your Recipe section posts |
| `_careers/` | Your Career section posts |
| `_pages/` | Static pages like the archive pages for each section and the 404 page |

---

## Configuration (controls how the site behaves)

| File | What it does |
|---|---|
| `_config.yml` | The main brain of your site — sets title, theme, author info, collections, plugins, navigation behavior |
| `_data/navigation.yml` | Controls what links appear in the top navigation bar |
| `_data/ui-text.yml` | Translations for button labels and UI text (e.g. "Back to Top", "Read More") |
| `Gemfile` | Lists Ruby packages (gems) Jekyll needs to run locally |
| `minimal-mistakes-jekyll.gemspec` | Package definition for the Minimal Mistakes theme itself |
| `staticman.yml` | Configuration for Staticman (a comment system) — not currently active |

---

## Layouts (page templates)

Everything in `_layouts/` is an HTML template that wraps your content. You pick which one to use in a post's front matter with `layout: name`.

| File | What it does |
|---|---|
| `default.html` | The base shell — every page ultimately wraps into this |
| `home.html` | The homepage layout (shows recent posts) |
| `single.html` | Used for individual posts/pages (the most common layout) |
| `archive.html` | A base layout for listing pages |
| `blogs.html` / `recipes.html` / `books.html` / `careers.html` | The archive listing page for each of your sections |
| `blog.html` / `recipe.html` / `book.html` | Sub-archive pages (e.g. listing just your "Baking" recipes) |
| `splash.html` | A full-width hero/landing page layout |
| `search.html` | The search results page layout |
| `categories.html` / `tags.html` | Archive pages grouped by category or tag |
| `compress.html` | Strips whitespace from HTML output to make pages load faster |

---

## Includes (reusable HTML components)

Everything in `_includes/` is a small reusable chunk of HTML that gets inserted into layouts.

| File/Folder | What it does |
|---|---|
| `masthead.html` | The top navigation bar |
| `footer.html` | The bottom footer with social links |
| `sidebar.html` | The left sidebar with your author profile |
| `author-profile.html` | Your photo, name, bio, and social links in the sidebar |
| `archive-single.html` | How a single post looks when listed in an archive (title, date, excerpt) |
| `documents-collection.html` | Lists all posts from a collection (used by your section archive pages) |
| `breadcrumbs.html` | The "Home > Blog > Post Title" trail at the top of a page |
| `toc.html` | Table of contents (auto-generated from headings in a post) |
| `page__meta.html` | Shows read time, date, categories, tags on a post |
| `page__related.html` | "You may also like" section at the bottom of posts |
| `paginator.html` | The page 1, 2, 3… navigation for long lists |
| `social-share.html` | Share buttons (Twitter, Facebook, etc.) |
| `comments.html` | Comment section (disabled for now) |
| `analytics.html` | Google Analytics hook (disabled for now) |
| `seo.html` | Injects SEO meta tags into the `<head>` |
| `head.html` | The HTML `<head>` section (loads CSS, fonts, meta tags) |
| `scripts.html` | Loads JavaScript at the bottom of each page |
| `search/` | Search functionality files |
| `comments-providers/` | Different comment system integrations (Disqus, Giscus, etc.) |
| `analytics-providers/` | Different analytics integrations |

---

## Styling (controls how things look)

| File/Folder | What it does |
|---|---|
| `assets/css/main.scss` | The entry point for all CSS — imports everything else |
| `_sass/minimal-mistakes.scss` | Imports all the individual style files |
| `_sass/minimal-mistakes/` | Individual style files for each component (navigation, sidebar, footer, etc.) |
| `_sass/minimal-mistakes/skins/` | Color themes — your site uses `_contrast.scss` (set in `_config.yml`) |

---

## JavaScript

| File/Folder | What it does |
|---|---|
| `assets/js/main.min.js` | All JavaScript bundled and minified for production |
| `assets/js/plugins/` | Individual JS plugins (smooth scrolling, image popups, navigation) |
| `assets/js/lunr/` | Search engine that runs in the browser |
| `assets/js/vendor/jquery/` | jQuery library |

---

## GitHub / Project files (you can mostly ignore these)

| File | What it does |
|---|---|
| `index.html` | The homepage file — sets the `home` layout |
| `README.md` | Documentation for the theme (not shown on your site) |
| `CHANGELOG.md` | Theme version history |
| `LICENSE` | Open source license for the Minimal Mistakes theme |
| `.gitignore` | Tells git which files NOT to track (e.g. temporary build files) |
| `.github/workflows/` | Automated GitHub Actions (CI build checks) |
| `.travis.yml` | Old CI configuration — not relevant for your setup |
| `screenshot.png` | Preview image of the theme |
| `package.json` | Node.js config (used for theme development, not your blog content) |
| `Rakefile` | Ruby task runner (used for theme development) |

---

## Files you'll touch most often

As a blogger, the only files you really need to work with day-to-day are:

1. **`_blogs/`**, **`_recipes/`**, **`_books/`**, **`_careers/`** — drop new `.md` files here to write posts
2. **`_config.yml`** — update your bio, site title, social links
3. **`_data/navigation.yml`** — add/remove nav links
4. **`_pages/`** — add/edit static pages
