# ClipFSCSS

[Build](https://github.com/fscss-ttr/clipfscss/actions/workflows/compile.yml/badge.svg)
[Pages](https://img.shields.io/badge/GitHub%20Pages-Live-success)
[License](https://img.shields.io/badge/license-MIT-blue)

## Example project demonstrating automatic compilation of FSCSS → CSS using GitHub Actions and deployment with GitHub Pages.

This repository shows how ".fscss" files can be compiled automatically into CSS whenever changes are pushed.

---

## Live Demo

**View the demo page:**

https://fscss-ttr.github.io/clipfscss/demo

---

## Project Structure
```
repo/
│
├── .github/workflows
│   ├── compile.yml
│   └── page.yml
│
├── .gitignores
|
├── src/
│   └── style.fscss
│
├── dist/
│   └── f.css
│
├── assets/styles
│   └── style.css
│
├── demo/
│   ├── index.html
|   └── assets/styles
│             └── style.css
│
├── node_modules/
│
├── fscss_exec.js
├── package.json
└── package-lock.json
```
---

## How It Works

**The workflow automatically compiles FSCSS to CSS.**

src/style.fscss
        ↓
GitHub Action runs
        ↓
FSCSS compiler executes
        ↓
dist/f.css generated
        ↓
CSS committed to repository
        ↓
GitHub Pages serves demo

---

Installation

Install dependencies:

npm install

---

Compile CSS Locally

Run:

npm run build:css

This compiles:

src/style.fscss

into:

dist/f.css

---

package.json

```json
{
  "dependencies": {
    "fscss": "^1.1.17"
  },
  "scripts": {
    "build:css": "fscss src/style.fscss dist/f.css"
  }
}
```
---

## GitHub Action: Compile FSCSS

Workflow file:

`.github/workflows/compile.yml`

**Steps performed:**

1. Checkout repository
2. Install dependencies
3. Run FSCSS compiler
4. Generate CSS
5. Commit compiled CSS

This keeps the compiled stylesheet synchronized with the FSCSS source.

---

##cGitHub Pages Deployment

The static demo site is deployed automatically.

**Workflow file:**

`.github/workflows/pages.yml`

Each push to the main branch updates the site.

---

### Example Usage

HTML example:
```html
<link rel="stylesheet" href="../dist/f.css">
```
---

## Purpose of This Repository

**This repo demonstrates:**

• FSCSS compilation workflow
• GitHub Actions automation
• Static site deployment
• Simple CI/CD integration
• Example FSCSS project structure

---

## Related Project

**Main FSCSS project:**

https://github.com/fscss-ttr/FSCSS

---

License

MIT
