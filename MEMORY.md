# Project Memory

Last updated: 2026-05-05

## Project

Personal landing page for Rishan Wilson.

## Location

`C:\Users\rishy\Documents\New project`

## Current Files

- `index.html`: Static landing page markup.
- `styles.css`: Minimal Swiss / Bauhaus visual system and responsive layout.
- `script.js`: Mobile navigation, reveal transitions, active nav state.
- `assets/rishan-wilson.png`: Portrait asset copied from `C:\Users\rishy\Desktop\Pic.png`.
- `.nojekyll`: GitHub Pages compatibility file.
- `README.md`: Local preview and GitHub Pages instructions.

## Content Source

Profile and career details were pulled from the applications/CV workstream under:

`C:\Users\rishy\Documents\Codex\Codex_Playground\projects\applications`

Key positioning:

- Rishan Wilson
- Berlin, Germany
- Enterprise Account Manager / Account Executive / Business Development
- 8+ years B2B technology sales and account management
- EUR 800K annual portfolio across 20+ enterprise accounts
- EUR 300K enterprise pharma account revenue target
- SaaS, IIoT, smart manufacturing, pharma/life sciences, track-and-trace, serialization, cold-chain monitoring

## Design Direction

Minimal personal landing page: Rick Rubin restraint, Swiss contemporary grid, Bauhaus accents.

Avoid:

- Generic SaaS landing page feel
- Heavy gradients
- Decorative floating cards
- Overly polished stock imagery

Prefer:

- Strong typography
- Dense but calm information
- Crisp grid structure
- Red, blue, yellow accent blocks used sparingly
- Real portrait as primary personal signal

## Verification

Headless Edge render check passed on desktop and mobile:

- No JavaScript errors
- No horizontal overflow
- Portrait image loaded
- Static server works via `http://127.0.0.1:5500/`

## Deployment State

Git and GitHub CLI were installed through `winget`.

GitHub CLI is authenticated as:

- `rishyanganwilson`

Primary user-site repository:

- Repo: `https://github.com/rishyanganwilson/rishyanganwilson.github.io`
- Intended URL: `https://rishyanganwilson.github.io/`
- Remote name: `origin`

Fallback project-site repository:

- Repo: `https://github.com/rishyanganwilson/rishan-wilson`
- Intended URL: `https://rishyanganwilson.github.io/rishan-wilson/`
- Remote name: `project`

Current deployment blocker:

- Both GitHub Pages builds are stuck in `building` / workflow `pending`.
- The public URLs currently return GitHub Pages `404`.
- The repository content is pushed correctly and Pages is configured from `main` `/`.
- GitHub Actions and Pages appear enabled by API, but jobs do not start normally.
- Likely account-level/manual GitHub blocker for the new account, such as email verification, first-run Actions approval, or a Pages settings banner in the GitHub UI.

Important GitHub docs note:

- GitHub says that if publishing from a branch does not happen automatically, someone with admin permissions and a verified email address must push to the publishing source.
- Commits were switched to the GitHub account-linked noreply address: `281940770+rishyanganwilson@users.noreply.github.com`.

Next manual checks:

1. Open GitHub account `Settings > Emails` and confirm the primary email is verified.
2. Open `https://github.com/rishyanganwilson/rishyanganwilson.github.io/actions` and check whether GitHub asks to enable or approve workflows.
3. Open `https://github.com/rishyanganwilson/rishyanganwilson.github.io/settings/pages` and check for a visible Pages build error or setup banner.
4. After any manual GitHub prompt is resolved, rerun Pages by pushing an empty commit or using the workflow dispatch.

## Vercel Deployment

Vercel CLI was installed locally inside `.vercel-cli/` and ignored by Git.

Production deployment succeeded:

- Live URL: `https://rishan-wilson.vercel.app/`
- Deployment URL: `https://rishan-wilson-bf668efgk-rishyanganwilson-4898s-projects.vercel.app`
- Vercel project: `rishan-wilson`
- Vercel project ID: `prj_ah2rsfpD17nMlaPC5c4DXzfU62uJ`
- Vercel owner/team ID used by CLI: `team_tgMSrlU5A5me7AgoTIWRVLo3`

Verification:

- `https://rishan-wilson.vercel.app/` returned HTTP 200.
- Response content contained `Rishan Wilson`.
- Response title matched `Rishan Wilson`.

GitHub-to-Vercel connection state:

- Attempted to connect Vercel project to GitHub repo `https://github.com/rishyanganwilson/rishan-wilson.git`.
- Vercel returned: `Failed to link rishyanganwilson/rishan-wilson. You need to add a Login Connection to your GitHub account first.`
- Next manual step: in Vercel, add GitHub as a login connection / account connection, then rerun:

```powershell
& 'C:\Program Files\nodejs\node.exe' '.\.vercel-cli\node_modules\vercel\dist\index.js' git connect 'https://github.com/rishyanganwilson/rishan-wilson.git'
```
