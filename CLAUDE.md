# Zen Amplification — Project Rules for Claude Code

This is the Vault-50 product homepage: a single master `index.html`, edited in VS Code with Live Server. Plain HTML/CSS/JS, no framework. Images and assets on Cloudinary; PDFs on GitHub Pages (the `zen-assets` repo — `antonhagop.github.io/zen-assets/FILENAME.pdf`). Version control through GitHub Desktop, with a two-person Git workflow shared with a business partner.

## How to work with me

- I'm a beginner-to-novice coder. Be extremely descriptive about *where* a change goes.
- For a single-value change, give me the **line number** and the exact line — I'll edit it myself in VS Code.
- For structural changes or new sections, give complete paste-ready code, with **HTML, CSS and JS labelled separately**.
- Prefer **surgical edits in place** over whole-file rewrites, especially when local changes are in flight.
- **Never** call code "final," "bulletproof," "nuclear," or "the final word" before it's been proven in the browser. It works once I've confirmed it in the browser — not before.
- Short, concise replies. No hyperbole or flattery.
- Do what I ask first; raise suggestions or questions in the next round rather than pre-empting.
- Copy is **suggestions only** — never apply copy changes to the file. Flag jargon or house-style issues as notes, don't silently "correct" them.
- Before any significant structural change, confirm a git commit / fallback exists.
- New elements must use the site's **existing reveal system** automatically (the IntersectionObserver pattern the other sections use — `translateY(10px)`, ~700ms ease, staggered, ~25% threshold).
- For risky additions (new sections, reveal staging), build into a **standalone audition file first**, not straight into master. The `audition` skill carries the full procedure.
- Use Python assertion-based scripts for structural edits, operating on section banner comment markers, with tag-balance and orphaned-CSS-reference checks.

## Locked brand constants — do not change without being asked

- Background gradient: `#0A0A0A` → `#272727` at `90deg`
- Accent (steel blue): `#92a4b1`
- Font: Helvetica Neue stack
- Class namespace: `zvlt-` (BEM)
- **US spelling** throughout
- **No em dashes** (en dash is acceptable)
- Aesthetic: restrained premium (Rolex / BMW reference). No spinning or jarring effects.

## Copy / house style

- "sonic clone" is a branded term, set in the accent colour.
- Use **"recall"** for stored settings — not "restore" or "presets."
- Cornerstone closing phrase: "uncompromising players and demanding producers".
- Don't repeat "sonic" / "recreate" / "flexibility" across sections.
- Register: plain, confident, technically grounded, premium without corporate language.
- "Rebels vs Redcoats" is used elsewhere on the site — don't revisit it in the hero.

## Product facts (for accurate copy/context)

Vault-50: 50W dual-EL34/6L6 tube head that recreates 40 classic amplifiers via analog component-level switching (not digital modeling). 12AX7 preamp, 5-band GEQ, motorized pots with MIDI recall, reactive load, 48 IRs, variable boost, assignable reverb. Mercury Magnetics output transformer and Synergy Royal Mustard capacitors are key hardware proof points. $6,400 USD, handcrafted in Sydney.
