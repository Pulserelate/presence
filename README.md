# PulseRelate presence

Public one-page site for PulseRelate’s website and social media services. It is a static GitHub Pages site, separate from the CRM.

Live URL: https://presence.pulserelate.com

GitHub Pages also serves https://pulserelate.github.io/presence/ until the custom domain finishes provisioning.

## Google Form

The inquiry link lives in `index.html`:

```html
<script>
  const FORM_URL = "https://docs.google.com/forms/d/e/FORM_ID/viewform?usp=sharing";
</script>
```

Leave `FORM_URL` as `""` to show “Inquiry form opening soon.” When it is set, the page shows a button that opens the form in a new tab and embeds the form on the page. Commit and push to `main` to update the live site. No build step.

## GitHub Pages

The site is published from the `main` branch, at the repository root. `CNAME` sets the public host to `presence.pulserelate.com`.

In Cloudflare, that name needs its own record so it does not follow the wildcard to the CRM:

| Type | Name | Value | Proxy |
|---|---|---|---|
| CNAME | `presence` | `pulserelate.github.io` | DNS only |

`pulserelate.com` and `sites.pulserelate.com` stay on the CRM.
