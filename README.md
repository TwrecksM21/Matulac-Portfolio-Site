# Rexmar Jim G. Matulac — Portfolio

A single-page portfolio site (content & video work), ready to publish on GitHub Pages.

## Files

- `index.html` — the entire site (HTML, CSS, and JS in one file; the profile photo is embedded as base64, so there are no separate image files to manage)
- `.nojekyll` — tells GitHub Pages to serve the file as-is, skipping Jekyll processing (not required for a plain HTML site, but included as good practice)

## How to publish on GitHub Pages

1. Create a new GitHub repository (e.g. `matulac-portfolio`).
2. Upload `index.html` and `.nojekyll` to the root of the repository (or push them with `git add`, `git commit`, `git push`).
3. In the repository, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Under **Branch**, choose `main` (or your default branch) and folder `/ (root)`, then **Save**.
6. GitHub will publish the site at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

If you'd rather use a personal/organization site (`https://<your-username>.github.io`), name the repository exactly `<your-username>.github.io` and follow the same steps.

## What was fixed from the original file

- The "Works / Feed" section was missing the actual link-input, button, and feed-grid elements that the page's JavaScript depends on — the "add a link" feature would fail silently. These are now in place.
- A malformed Google Drive link block (stray closing tag, unquoted `href`) was replaced with a properly formatted link card matching the rest of the site's design.
- The `#works` section was never closed, so the `#contact` section was nested inside it — this could cause unpredictable spacing/layout. It's now closed correctly.
- A stray unclosed `<p>` tag in the hero section was closed.
- A couple of small typos/spacing issues were cleaned up in the contact copy.

Everything else — fonts (loaded from Google Fonts via CDN), layout, animations, and the timeline scrubber — was already self-contained and works as-is.
