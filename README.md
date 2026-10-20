# PulseRelate presence

Public one-page site for PulseRelate’s website and social media services. It is a static GitHub Pages site, separate from the CRM.

Live URL, once Pages is enabled: https://pulserelate.github.io/presence/

## Google Form

The inquiry button stays hidden until a form link is set. Open `index.html` and paste the Google Form share link:

```html
<script>
  const FORM_URL = "https://docs.google.com/forms/d/e/FORM_ID/viewform?usp=sharing";
</script>
```

Leave `FORM_URL` as `""` until the form exists. Visitors then see “Inquiry form opening soon.”

After the link is set, the page shows a button that opens the form in a new tab and embeds the form on the page (about 900px tall). Commit and push to `main` to update the live site. No build step.

## GitHub Pages

The site is published from the `main` branch, at the repository root. Pages settings should stay on that source. Do not attach `pulserelate.com` here; that domain stays on the CRM.
