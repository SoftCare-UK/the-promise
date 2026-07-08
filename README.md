# The Promise, Scotland

A static site exploring Scotland's commitment to children, young people and families in care, with three audience-specific pages off a shared landing page.

## Pages

- `index.html` — landing page, picks an audience
- `promise-quest.html` — for ages 7–11, a playful map journey
- `the-promise-teens.html` — for ages 12–18, "Have Your Say"
- `keeping-the-promise-staff.html` — for staff & practitioners, a reflective practice module that generates a personal pledge PDF

## Stack

Plain HTML / CSS / JS, no build step. The staff page uses jsPDF (loaded from CDN) to generate the downloadable Pledge.

## Local preview

Open `index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

Designed for Netlify. Either drag-and-drop the folder onto Netlify Drop, or connect this repo to Netlify with default settings (no build command, publish directory = repo root).


## Making changes (humans + agents)

- **Each page is standalone HTML** — no shared templates; a nav/footer change
  must be applied to every page by hand.
- The staff page's pledge PDF uses **jsPDF from a CDN** — the only external
  script. Test PDF generation after touching that page.
- **Factual grounding matters.** The Promise is a real national commitment
  (Scotland's Independent Care Review). Statements about it must be accurate
  and sourced; keep the tone respectful of care-experienced people — this is
  a sensitive subject, not marketing copy.
- Audience fit: `promise-quest.html` (7–11) stays playful; the teens page is
  direct and rights-focused; the staff page is reflective, not preachy.
- Accessibility: semantic structure, alt text, contrast — assume school
  Chromebooks and screen readers.

No analytics, no cookies, no personal data collected (the pledge PDF is
generated client-side and never uploaded) — keep it that way.

Maintained by the SoftCare team (SoftCare-UK) as a public-good resource.
