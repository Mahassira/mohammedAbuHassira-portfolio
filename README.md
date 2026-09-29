# Mohammed H. Abu Hassira — Portfolio

This is my personal portfolio site. One page, no backend, no build step — just an HTML file with a Three.js tunnel running behind the content and GSAP handling the scroll animations.

I wanted something that felt less like a CV and more like an actual piece of work, since most of what I do day to day is exactly that — building systems, not writing bullet points about myself. So instead of a normal "About / Experience / Contact" layout, you scroll through a tunnel and the sections (career journey, capabilities, projects, stack, experience, contact) appear along the way.

## What's in here

- `index.html` — the whole site. Everything is in this one file on purpose, so it's easy to drop anywhere without worrying about paths or missing assets.

## Stack

- [Three.js](https://threejs.org/) (r128) — the procedural tunnel, particles and the glow points
- [GSAP](https://gsap.com/) + ScrollTrigger — scroll-driven camera movement and the text reveals
- Poppins for headings, Open Sans for body text (both from Google Fonts)
- No frameworks, no npm, no bundler. Just open the file.

## Running it locally

There's nothing to install. Either:

- Double-click `index.html` and it'll open in your browser, or
- If you want it served properly (some browsers are picky about local file fonts/CORS), run:

```bash
python3 -m http.server 8000
```

then open `http://localhost:8000`.

## Deploying

I'm hosting this for free on GitHub Pages. If you're doing the same:

1. Rename the file to `index.html` (already done here).
2. Push it to a repo.
3. Go to **Settings → Pages**, set the source to the `main` branch, root folder.
4. Wait a minute, then it's live at `https://<your-username>.github.io/<repo-name>`.

Netlify Drop also works if you just want to drag-and-drop a file and get a link with zero setup.

## Customizing

A few things worth knowing if you (or future me) want to tweak this:

- Colors are CSS variables at the top of the `<style>` block (`--indigo`, `--cyan`, `--violet` — names are leftover from an earlier color scheme, the actual colors have changed a couple of times already).
- The tunnel path is a `CatmullRomCurve3` with a handful of control points — change `NUM_CP` or the sine/cosine offsets to make the path wind differently.
- Particle counts are lower on mobile (`isMobile` check) to keep frame rate sane on phones.
- Text content lives directly in the HTML, section by section — no CMS, no JSON file, just find the section and edit it.

## Known rough edges

- It's a single big file, which is great for portability and slightly annoying for editing — I just use my editor's search a lot.
- Performance on older phones can dip a bit with the particle field at full count; happy to tune it further if it becomes an issue.
- No contact form yet — it's just a `mailto:` and `tel:` link for now.

## Contact

Mohammed H. Abu Hassira
mahassira@outlook.com · +20 102 216 7209 · [linkedin.com/in/mohammedabuhassira](https://linkedin.com/in/mohammedabuhassira)
