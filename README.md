# lradenovic.com — static site

This is a hand-built replacement for the Weebly site, ready for GitHub Pages.

## 1. Before you upload: two things to fix

1. **Email address** — Weebly hides your email behind spam protection, so I
   couldn't read it. Open `contact.html`, find `REPLACE_WITH_YOUR_EMAIL`
   (it appears twice on that one line) and replace both with your real
   address, e.g.:
   ```html
   <a href="mailto:you@example.com">you@example.com</a>
   ```

2. **Images and the CV PDF** — I could not download binary files from this
   chat session, only read the page text. You'll need to save these
   yourself from the live Weebly site and drop them into the `images/`
   and `cv/` folders with the exact filenames below (right-click each
   image on lradenovic.com → "Save image as…"):

   | Save into      | Filename                        | Source (open in a browser)                                                                                                   |
   |----------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
   | images/        | hero-marshes.jpg                 | https://www.lradenovic.com/uploads/1/3/7/9/137909843/editor/glavna-slika-640px-martin-johnson-heade-sunlight-and-shadow-the-newbury-marshes-google-art-project_2.jpg |
   | images/        | counseling-header.jpg            | https://www.lradenovic.com/uploads/1/3/7/9/137909843/published/1200px-ivan-konstantinovich-aivazovsky-the-island-of-ischia-at-sunset-sunset-over-ischia_2.jpg |
   | images/        | counseling-emotions.jpg          | https://www.lradenovic.com/uploads/1/3/7/9/137909843/published/razgovor-o-emocija-slika-consolation-of-philosophy_2.jpg |
   | images/        | counseling-dilemmas.jpg          | https://www.lradenovic.com/uploads/1/3/7/9/137909843/published/moralne-dileme-slika-nesterov-florensky-bulgakov-1_2.jpg |
   | images/        | counseling-meaning.jpg           | https://www.lradenovic.com/uploads/1/3/7/9/137909843/published/samotranscedencija-slika-caspar-david-friedrich-wanderer-above-the-sea-of-fog_2.jpeg |
   | images/        | tutoring-manuscript.jpg          | https://www.lradenovic.com/uploads/1/3/7/9/137909843/published/miniature-showing-leontia-in-a-courtyard-studying-a-book-propped-up-on-a-lectern-8df483-640_2.jpg |
   | images/        | texts-header.jpg                 | https://www.lradenovic.com/uploads/1/3/7/9/137909843/published/ljilja-knjiga.jpg |
   | images/        | text-prolegomena.jpg             | https://www.lradenovic.com/uploads/1/3/7/9/137909843/published/images.jpg |
   | images/        | text-empathy.jpg                 | https://www.lradenovic.com/uploads/1/3/7/9/137909843/published/edvard-munch-consolation-1894-e1638911847715_2.webp |
   | images/        | text-desert-fathers.jpg           | https://www.lradenovic.com/uploads/1/3/7/9/137909843/published/temptations-of-saint-anthony-e1628524938460_2.webp |
   | images/        | text-faith.jpg                   | https://www.lradenovic.com/uploads/1/3/7/9/137909843/editor/evening-prayer-anna-ancher-e1631202284927_2.webp |
   | images/        | contact-phone.jpg                | https://www.lradenovic.com/uploads/1/3/7/9/137909843/editor/960px-rotarydial_2.jpg |
   | cv/            | cv_ljiljana_radenovic_2025.pdf   | https://www.lradenovic.com/uploads/1/3/7/9/137909843/cv_ljiljana_radenovic_2025.pdf |

   Tip: do this fast by opening each source link, right-clicking the image,
   "Save image as," and saving directly into the matching folder with the
   exact filename from the table (case-sensitive).

## 2. Upload to GitHub

1. Create a new **public** repository named exactly `lradenovic72-sys.github.io`.
2. On the repo page, click **Add file → Upload files**, then drag in
   *all* files and folders from this project (`index.html`, the other
   `.html` files, `styles.css`, the `images/` folder, the `cv/` folder,
   and `CNAME`).
3. Commit the upload to the `main` branch.
4. Go to **Settings → Pages**. Under "Build and deployment," set Source
   to "Deploy from a branch," branch `main`, folder `/ (root)`. Save.
5. Wait a minute, then visit `https://lradenovic72-sys.github.io/` to
   confirm it works.

## 3. Point lradenovic.com at GitHub

The `CNAME` file in this project already contains `lradenovic.com`, which
tells GitHub Pages to serve your custom domain once DNS is updated.

At your domain's registrar (find this via a WHOIS lookup on lradenovic.com,
or check old renewal emails), set:

- **A records** for the root domain (`@` / `lradenovic.com`) pointing to:
  - 185.199.108.153
  - 185.199.109.153
  - 185.199.110.153
  - 185.199.111.153
- **CNAME record** for `www` pointing to `lradenovic72-sys.github.io`

DNS changes can take anywhere from a few minutes to 24 hours. Once it's
live, go back to Settings → Pages and check "Enforce HTTPS."

Don't cancel your Weebly plan until the new domain is confirmed working —
keep it active as a fallback until DNS has fully propagated.
