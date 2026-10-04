# nabla-site

Public legal and support hub for the **Nabla** mobile app (Math, maxed.).

This repository exists only to publish the pages that the App Store, Google Play, and
the in-app paywall are required to link to. The app source lives in a separate private
repository.

| Page | Purpose |
|---|---|
| `index.html` | Landing page linking to everything below |
| `privacy.html` | Privacy policy — linked from the paywall and both store listings |
| `terms.html` | Terms of use, including auto-renewing subscription terms |
| `support.html` | Support contact, subscription help, bug/error reporting |
| `app-version.json` | Oldest supported (`minimum`) and newest (`latest`) app version per platform. Below `minimum` the app shows a required-update screen; below `latest` it offers the update once. Raise `minimum` only after that version is live in both stores. |

## Published at

GitHub Pages serves the repository root on the `main` branch.

The app reads this base URL from `EXPO_PUBLIC_LEGAL_URL` and appends `/privacy.html`,
`/terms.html`, and `/support.html`. **Keep those filenames stable** — changing them
breaks the links Apple and Google review against.

## Editing

Plain static HTML with one shared stylesheet. No build step, no dependencies.
Update the "Effective date" line whenever the substance of a policy changes.
