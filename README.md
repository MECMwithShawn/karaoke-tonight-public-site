# Karaoke Tonight Public Site Bundle

This folder is the copyable static bundle for the public App Store URLs.

## Files

- `index.html` routes to the public pages.
- `privacy.html` is the hostable Privacy Policy page and must match `../PRIVACY_POLICY_PUBLIC.html`.
- `support.html` is the hostable Support page and must match `../SUPPORT_PUBLIC.html`.

## Hosting

Upload the contents of this folder to a static HTTPS host controlled by the app owner.

Recommended URL mapping:

- `/privacy.html` or `/privacy` -> App Store Privacy Policy URL.
- `/support.html` or `/support` -> App Store Support URL.

After publishing, verify the live URLs:

```bash
PRIVACY_POLICY_URL=https://example.com/privacy.html npm run verify:privacy-url -- --require-url
SUPPORT_URL=https://example.com/support.html npm run verify:support-url -- --require-url
```

Then replace `PRIVACY_POLICY_URL_TBD` and `SUPPORT_URL_TBD` in `docs/APP_STORE_METADATA.md`.

Do not deploy from this folder until `npm run verify:public-site` passes.

Regenerate copied pages after privacy/support source edits:

```bash
npm run build:public-site
npm run verify:public-site
```
