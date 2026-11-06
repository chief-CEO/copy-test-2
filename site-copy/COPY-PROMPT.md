# Rebuild scalogy.com: instructions for your AI agent

You are rebuilding https://scalogy.com/ as a plain HTML and CSS website in the owner's GitHub repository, then publishing it free on GitHub Pages. The `site-copy/` folder in this repository came from Scalogy's Copy my website tool on 2026-11-06. The owner proved they run scalogy.com before it was made.

Publishing is already set up: GitHub Pages publishes this repository's `gh-pages` branch at https://chief-ceo.github.io/copy-test-2/. Whatever is merged into `gh-pages` goes live there about a minute later.

## What's in `site-copy/`

- `site-copy/pages/*.html`: each page's words and structure, with the builder's code removed. Links between pages already point to the matching file.
- `site-copy/screenshots/`: what each page looks like on a computer (`<page>-desktop-01.jpg`, `-02` and so on, one screen each, top to bottom) and on a phone (`<page>-phone-01.jpg` and on). Long pages keep the first few screens and the last one (the footer); `site-copy/site.json` lists every piece with its position. Your copy should match them.
- `site-copy/images/`: every image used on the pages, logo included.
- `site-copy/site.json`: the page list, the menu, contact details, brand colours and fonts, any structured data the site already had, and what was skipped.

## Steps

1. Work in this repository. Build the new site at the top of the repository (`index.html` at the root, not inside `site-copy/`), using the files in `site-copy/` as your source. The `index.html` there now is a "coming soon" placeholder: replace it. Keep `_config.yml`: it keeps `site-copy/` off the live site.
2. Rebuild each file in `site-copy/pages/` as a page with the same file name, with `index.html` as the home page. Match its desktop and phone screenshots: the same sections in the same order, with the same layout, colours, fonts and spacing. Keep every word exactly as it is.
3. Keep the header, menu and footer identical on every page and put the styles in one shared stylesheet, so later changes happen in one place.
4. Use only the files in `site-copy/images/` (copy them into the new site's own `images/` folder). Never copy the old builder's code, scripts, theme files or tracking, and don't link to the old site's image servers.
5. On every page, add `<link rel="canonical" href="...">` pointing to the same page on the original site (each page's `url` in `site-copy/site.json`). This stops the copy competing with the original in Google until the owner moves their domain.
6. Replace each form (marked `<!-- form -->` in the page files) with a simple email link to the first address in `site-copy/site.json` under `contact.emails`. If there is no address, ask the owner which one to use. Booking widgets and online stores become a plain link to the original page.
7. Put your work on the `gh-pages` branch. If you work on your own branch, open a pull request into `gh-pages` and merge it yourself if you can. Don't change the repository's settings: publishing is already on.
8. Before you finish, open each page you built next to its screenshots (in a browser, if you have one) and fix anything that doesn't match. If the site is already live, check the live pages too.
9. Never buy anything, enter payment details, change DNS settings or touch the original website. If a step would need any of that, stop and ask the owner.
10. Leave `site-copy/` where it is: `_config.yml` keeps it off the live site, and it stays handy if the owner wants changes later.
11. Finish with a short report for the owner: the pages you copied, anything that still doesn't match its screenshot, and what didn't carry over (see `skipped` in `site-copy/site.json`). If your work is merged into `gh-pages`, give the live address, https://chief-ceo.github.io/copy-test-2/. If it isn't (you couldn't merge it yourself), the owner has to do it, so end your report with this, word for word:

    > **One step left: merge my work.** On GitHub, open the pull request I made (if there isn't one yet, use the Create PR button in this app first), click **Merge pull request**, then **Confirm merge**. Your new site goes live at https://chief-ceo.github.io/copy-test-2/ about a minute later.

## Rules

- Plain HTML and CSS only: no frameworks and no build step. Use JavaScript only for a mobile menu, and only if the original has one.
- Use relative links and file paths (`about.html`, `images/logo.webp`), never ones that start with `/`: GitHub Pages serves the site from a sub-folder, where those break.
- Keep each image's alt text.
- Don't add pages, sections, offers or claims that aren't on the original site.
- If a screenshot and a page file disagree, the screenshot shows how it should look and the page file has the exact words.

## This copy has the first 10 of 100 pages

The rest are listed in `site-copy/site.json` under `not_copied`. The owner can get the full site free at https://scalogy.com/copy-my-website by adding their contact details. Copy the pages you have; link menu items for the missing pages to the original site for now.
