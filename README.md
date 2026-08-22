# Cotswold Jet Photography — site source

Single static page, no build step, no backend. Fonts load from Google Fonts at runtime; everything else is self-contained in `index.html`.

## Before this goes anywhere public

Two placeholder contact details are in the Contact section of `index.html` — search for them and swap in the real ones:
- `hello@cotswoldjetphotography.co.uk`
- `@cotswoldjetphotography` (Instagram)

## Get it live

**Fastest — no account setup needed to preview:**
Go to https://app.netlify.com/drop and drag this folder in. It's live at a random `*.netlify.app` URL in seconds. Add a custom domain (e.g. via GoDaddy, same as freelancepilots.uk) from the site's Netlify dashboard afterwards.

**Same flow as freelancepilots.uk (git-based, continuous deploy):**
1. `git init` has already been run in this folder — create a new empty repo on GitHub, then:
   ```
   git remote add origin <your-repo-url>
   git branch -M main
   git push -u origin main
   ```
2. In Netlify: "Add new site" → "Import an existing project" → pick the repo. Build command: none. Publish directory: `.`
3. Point your domain at it the same way you did for freelancepilots.uk.

**Have Claude deploy it directly:**
Connect the Netlify connector (and Supabase, if you want a real working enquiry form later) via claude.ai's connector settings, then ask Claude to create and deploy the site — same tools, done from chat.

## About Supabase

The site is fully static right now (the Contact section just uses `mailto:` and an Instagram link), so there's nothing for Supabase to do yet. If you want a proper enquiry form that emails you and stores leads — the way freelancepilots.uk uses Supabase + Resend — say the word and that can be added once the real contact details are confirmed.
