# sagito-info

The public pages for **Sagito**, served by GitHub Pages at **info.sagito.app**. This is the
older address, kept alive because the app stores, every shipped build and links already
sent to people point at it (`/privacy`, `/support`, `/invite`, `/gift`, `/swap`).

**The main site is `www.sagito.app`**, served by `niqluong-commits/sagito-www`. **Since 25 November 2026 this site only holds the pages that must keep their address.**
`/privacy`, `/support`, `/terms`, `/invite`, `/gift`, `/swap` and the 404 page stay here as real
pages: the stores, the app and links already sent to people use them. Their header has one link,
"Sagito home", to `www.sagito.app`. `/`, `/faq`, `/about` and `/resources` are small redirect pages
(meta refresh and script, keeping any `?` and `#`) to the same path on `www`, because GitHub Pages
cannot send a real 301. **Edit marketing pages, resources and the blog in `sagito-www` only.** The PDFs
already published under `/resources/` are left in place so old links still work, but they are not
updated; the current ones are on `www`. The kept pages differ from `docs/legal/*-public.html` in the
app repo in one way: the header nav is replaced by the single "Sagito home" link and the logo links to
`www`. When you copy a changed `privacy`, `support` or `terms` page here, redo that header swap.

| Path | Page | Source of truth |
| --- | --- | --- |
| `/privacy` | Privacy notice | `docs/legal/privacy-public.html` in the app repo |
| `/invite`, `/gift`, `/swap` | Where a shared code lands | `docs/legal/join-public.html` in the app repo |
| `/terms`, `/support` | Site pages | `docs/legal/*-public.html` in the app repo (copied here and to `sagito-www`; header swapped, see above) |
| `/`, `/faq`, `/about`, `/resources` | Redirects to `www` | none: they hold no content |

**For privacy and shared-code pages, edit the app repo, not this one.** Those pages are sourced from
`niqluong-commits/sagito` and copied here; `docs/legal/PRIVACY.md` records the route,
and `docs/legal/joinPage.test.mjs` checks the landing page still builds a code the app
will accept. A change made only here is a change the tests cannot see.

The three code paths serve the same file. It works out which kind of code it is from
the path it was served at, so a new code type needs a new directory here.

**It moved from `privacy.sagito.app` on 9 September 2026**, because GitHub Pages allows
one custom domain per repository and two documents needed two addresses. The old
subdomain should redirect rather than 404 — a privacy URL given to an app store ought
to keep working.

Support images are unchanged approved assets from the app repository: `assets/brand/sagito-logo-horizontal.svg` and `docs/store-assets/screenshots-marketing/{2-cards,1-home,4-campsite}.png` (7 September 2026 captures). Recopy updated approved screenshots when the source set changes; do not paint over the captured UI.
