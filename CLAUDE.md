# Anton Hagop Mixing (AHM) — Project Rules for Claude Code

Personal site for Anton Hagop Mixing, a freelance audio mixing engineer. Plain HTML/CSS/JS, no framework, edited in VS Code with Live Server. Unlike Zen Amps (one master `index.html`), AHM is **multi-page**: each page is a clean, self-contained single-file HTML document. Current pages: `index.html`, `listen.html`, `mixing.html`, `contact.html`. Images are local in `/images`. Contact form via FormSubmit. Version control through GitHub Desktop, solo repo (no business partner). Repo: `antonhagop/AHMixing`. Live on GitHub Pages, custom domain `antonhagop.com.au`.

This is a **migration in progress**: porting the old WordPress/Elementor Pro site to pure HTML. See the Migration section below.

## How to work with me

- I'm a beginner-to-novice coder. Be extremely descriptive about *where* a change goes.
- For a single-value change, give me the **line number** and the exact line, and I'll edit it myself in VS Code.
- For structural changes or new sections, give complete paste-ready code, with **HTML, CSS and JS labelled separately**.
- Prefer **surgical edits in place** over whole-file rewrites, especially when local changes are in flight.
- **Never** call code "final," "bulletproof," "nuclear," or "the final word" before it's been proven in the browser. It works once I've confirmed it in the browser, not before.
- Short, concise replies. No hyperbole or flattery.
- Do what I ask first; raise suggestions or questions in the next round rather than pre-empting.
- Copy is **suggestions only**: never apply copy changes to the file. Flag issues as notes, don't silently "correct" them.
- Before any significant structural change, confirm a git commit / fallback exists.
- Because AHM is multi-page, a change to shared markup (nav, footer, head links, fonts) usually has to be **repeated across every page**. Call this out and give me the block once, clearly, so I can paste it into each file, or tell me which files are affected.

## Don't stop to ask — keep working

- **Do not pause to ask "Do you want me to proceed?", "Should I continue?", "Want me to go ahead?"** or any variant. Once a task is clear, run it through to completion without checking in mid-stream.
- Reading files, listing folders, grep/search, `git status` / `diff` / `log`, starting/refreshing Live Server, installing a needed package: all **pre-approved**. Never ask permission for these; just do them and report the result.
- Default to **acting, then reporting** what you did. Don't ask first for routine work.
- If you genuinely need my input, ask **once, batched, at the end of the turn**, not one prompt at a time.

### The only things I still want to be asked about

- A spec that's actually ambiguous (two reasonable readings that lead to different output).
- **Destructive or irreversible** actions: deleting files, `git reset --hard`, force-push, history rewrite, or overwriting a page while local edits are in flight.
- Anything that would change a **locked brand constant** (see below) or change **copy** in the file.
- Confirming a **git commit / fallback exists** before a significant structural change.

Everything outside that list: proceed without asking.

## Migration status — WordPress to pure HTML

- **Source of truth: the Simply Static export.** It's a full rendered copy of the old site (text, images, fonts, colours). The Elementor JSON export is **useless for an HTML port** (only re-imports into Elementor), so ignore it. View Page Source is backup only.
- **Approach:** rebuild each page clean as single-file HTML, using the export as reference, not a straight host of the machine-generated Elementor markup.
- **Media URL audit** (outstanding before old hosting is retired): the export can contain absolute WordPress upload URLs that won't rewrite themselves. Any reference pointing at the old WordPress domain must be localised to `/images` (or a CDN) before the WordPress/HostGator hosting is switched off, or images will 404.
- **Links:** file-style (`contact.html`, `mixing.html`), not folder-style. Stay consistent across all pages.
- **Forms:** FormSubmit (same as ZA).
- **Players:** plain `<audio>` tags and YouTube embeds survive static export; any old plugin-based player does not, so test playback after any rebuild.

## Hosting and deployment

- **Host:** GitHub Pages, repo `antonhagop/AHMixing`.
- **Domain / DNS:** `antonhagop.com.au`, DNS configured at HostGator pointing to GitHub Pages.
- **Winding down HostGator hosting** once the pure-HTML site is fully live. **Open item:** confirm whether an active email mailbox at `antonhagop.com.au` needs preserving or migrating **before** HostGator hosting is cancelled, since cancelling may kill the mailbox. Resolve this before pulling the plug.
- Publish workflow: commit and push via GitHub Desktop, then GitHub Pages redeploys.

## Running Claude Code (launch setup — not enforced by this file)

This file shapes *behaviour*; the actual permission dialogs are controlled at **launch / `settings.json`**, not here. To pre-approve those:

- **Preferred: auto mode.** Skips routine permission prompts and nudges Claude to keep working without stopping for clarifying questions, while a safety classifier still blocks clearly dangerous actions.
- **Allowlist (most surgical).** Pre-approve only trusted commands in `.claude/settings.json` (`permissions.allow`), deny everything else.
- **Full bypass: `claude --dangerously-skip-permissions`.** Disables *all* prompts. Only safe in an isolated container or VM, not on this machine. Avoid here.

## Locked brand constants — do not change without being asked

Colours, fonts and namespace aren't captured for AHM yet. Pull them once from the old site via Chrome DevTools (right-click an element, Inspect, read the computed colour/font), then fill in and lock:

- Primary / background colour(s): **[CONFIRM]**
- Accent colour: **[CONFIRM]**
- Font stack: **[CONFIRM]** (and: Google-hosted via `<link>`, or localised into the folder?)
- Class namespace: **[CONFIRM]**. ZA uses `zvlt-` (BEM). Suggest `ahm-` for AHM, but your call.
- Aesthetic direction: **[CONFIRM]**
- **Spelling: AU / UK** throughout (colour, organise, centre, licence). Locked.
- **Dashes: minimal.** Prefer commas, colons and parentheses; use a dash only where it genuinely aids clarity. Locked.

## Copy / house style — [CONFIRM]

- Register / tone of voice: **[CONFIRM]**
- Any branded terms or phrases to keep consistent: **[CONFIRM]**
- Terms to avoid or preferred wording: **[CONFIRM]**

## Notes / optional carry-overs from ZA

- If you want the same **reveal-on-scroll** feel as Zen (IntersectionObserver, `translateY(10px)`, ~700ms ease, staggered, ~25% threshold), say so and I'll establish one shared pattern to reuse across all AHM pages. Not assumed by default.
- For risky changes, work in a throwaway copy of the page first, confirm in the browser, then fold into the real file.
