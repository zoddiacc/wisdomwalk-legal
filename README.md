# Wisdom Walk — Legal pages (host these two)

Two web pages Google Play **requires** before publishing. Both are self-contained HTML — no build step, no dependencies.

## Files
- `privacy-policy.html` — Privacy Policy (required for every app)
- `delete-account.html` — Account & data deletion request page (required because the app has account sign-in)

They cross-link to each other with relative links, so host them **in the same folder**.

## How to host (pick one — all free)
- **GitHub Pages:** push this `legal/` folder to a repo, enable Pages → your URLs become
  `https://<user>.github.io/<repo>/privacy-policy.html` and `.../delete-account.html`
- **Netlify / Vercel / Cloudflare Pages:** drag-drop the `legal/` folder → get a public URL.
- **Any existing website:** upload both files to a `/legal/` path.

## Where the URLs go in Play Console
| URL | Play Console location |
|-----|----------------------|
| Privacy Policy URL | App content → Privacy policy, **and** Main store listing |
| Delete Account URL | App content → Data safety → Data deletion questions |

## Before publishing — confirm these match reality
- The in-app **Profile → Delete account** flow described in both pages must actually exist. If it isn't built yet, either build it or remove the "Option 1 / in-app" wording so the page only offers email deletion (email-only is acceptable to Google).
- Update the support email if `sanjay@wisdomwalk.live` isn't the public support address.
