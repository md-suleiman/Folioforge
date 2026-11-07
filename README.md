# Folioforge

An interactive, single-page developer portfolio for **Mohammed Suleiman**. The site is built with plain HTML, CSS and JavaScript, with an animated swarm-style page reconstruction, custom cursor effects, a soundtrack, and portfolio sections for the owner's background, skills, projects and achievements.

> **Project status:** Personal portfolio source. Review the contact details, placeholder counters and reuse rights called out below before publishing it publicly.

## Features

- Full-page portfolio with Home, About, Skills, Projects, Achievements and Contact sections.
- Swarm-style page reconstruction launched by the supplied `swarm.js` script.
- Animated cursor companions, scroll progress, reveal effects, floating shapes and interactive card/button effects.
- Local soundtrack controlled by the page's volume control.
- Responsive navigation and mobile layout.
- Local profile cutout image.

## Project structure

```text
Folioforge/
├── index.html                         # Main page (latest supplied version)
├── swarm.js                           # Swarm reconstruction runtime
├── audio.mp3                          # Soundtrack used by the swarm tour
├── profile-photo-cutout.png           # Profile image
├── archive/
│   └── index-before-audio-unlock-update.html  # Earlier HTML variant
├── NOTICE.md                          # Source/reuse notes
└── .gitignore
```

## Run locally

No npm install or build step is required. Serve the folder over HTTP so the browser can load the local image, audio and JavaScript assets:

```bash
python -m http.server 8000
```

Then open <http://localhost:8000>.

You can also use VS Code's Live Server extension. Opening `index.html` directly with a `file://` URL may behave differently for media and browser autoplay policies.

## Deploy with GitHub Pages

1. Create a GitHub repository named `Folioforge`.
2. Upload the contents of this folder to the repository root (not the enclosing ZIP or parent folder).
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
5. Wait for GitHub Pages to publish the site; the published URL will be shown in the Pages settings.

A static host such as Netlify or Vercel can also serve this folder without a build command. Use the repository root as the output directory.

## Before publishing

- Replace `your.email@example.com` with the correct public contact email.
- Replace the generic YouTube link if you want to show a YouTube profile; otherwise remove that social icon.
- The About section currently contains zero-valued counters. Update them with accurate numbers or remove them.
- The contact form currently presents a client-side success interaction; it is **not connected to an email service or backend**, so submitted messages are not delivered. Connect a form provider or backend before relying on it.
- Browser autoplay rules can prevent the soundtrack from starting with sound until the visitor interacts with the page. Keep the visible mute/volume control.
- Check the page on mobile, keyboard navigation and reduced-motion settings before treating it as production-ready.

## Source and reuse note

The supplied `swarm.js` identifies itself as **Swarm Rebuild**. The upstream repository README says that the project has no license yet, adapts substantial motion-design and animation-engine work from Joel Califa's original Swarm project, and asks users not to reuse the code without checking with the relevant creator(s). See <https://github.com/DhvanilPatel/swarm-cursors>.

This repository therefore does not add an open-source license or claim ownership of that animation engine. Obtain the necessary written permissions and review upstream attribution requirements before making a public copy or redistributing the swarm runtime. See [NOTICE.md](NOTICE.md).
