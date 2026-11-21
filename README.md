# Sarvesh Goyal · Portfolio (v2)

A static site with no build step. Hosted on GitHub Pages at <https://sarveshg88.github.io>.

## Files

- `index.html`: the whole site (styles and script are inline)
- `projects/kizuna/index.html`: the Kizuna case study (EMC Business Contest 2026)
- `projects/kizuna/app/index.html`: the Kizuna prototype, copied from `D:\EMC CONTEST\kizuna-app`. AI feedback is off on GitHub Pages because there's no `/api/ai` server; the app falls back to instant rubric checks and a scripted resident. To update it, copy the new `index.html` over this one.
- `projects/kizuna/media/`: pitch deck PDF, 3 slide PPTX, explainer video, web sized poster, and slide images for the deck viewer (made from the PDF)
- `404.html`: shown for any broken link
- `assets/sarvesh.jpg`: portrait
- `assets/Sarvesh_Goyal_Resume.pdf`: the resume all the Resume buttons link to. Replace it with a file of the same name to update it.

## Editing content

- **Hero pitch and numbers:** the `.sub` paragraph and `.stats` block in the hero.
- **Project order:** the cards in `.cases` show in the order they appear in the file.
- **Rotating headline word:** the `.rot` spans in the hero (fix, product, model, agent).
- **Root cause tracer cases:** the `CASES` array in the script (symptoms, root cause, fixes, note).
- **Periodic table skills:** the `ELEMENTS` array in the script, as `[symbol, name, family]`. Families are `tech`, `ana`, `exp` and `prod`.
- **Animated numbers:** any element with `data-count` counts up when it scrolls into view. `data-pre` and `data-suf` hold the text before and after the number.

## Libraries

Fonts come from Google Fonts (Geist, Geist Mono, Fraunces), icons from Phosphor (unpkg), and smooth scrolling from Lenis (jsDelivr, desktop only). Everything else is hand written in `index.html`. All motion turns off for visitors who set "reduce motion" on their device.

## How to update the site

The live site is whatever is on the `main` branch of github.com/sarveshg88/sarveshg88.github.io. Every push redeploys it, usually within a minute or two.

- **With Claude:** open this folder (`D:\Portfolio\site`), say what to change, and ask for it to be committed and pushed.
- **By hand on your laptop:** edit the files, then run `git add -A`, `git commit -m "what changed"` and `git push` from this folder.
- **In the browser:** open the file on GitHub, click the pencil icon, edit, then **Commit changes**. Run `git pull` here afterwards so this folder stays in sync.
- **Replace the resume:** overwrite `assets/Sarvesh_Goyal_Resume.pdf` with a file of the same name, then commit and push.

Every version is kept in the git history, so any change can be undone.

## Preview locally

```
python -m http.server 5173 --directory D:\Portfolio\site
```

Then open http://localhost:5173.
