# Publish folder — agent framework visual

This folder is ready to drop into a GitHub repo and serve via GitHub Pages.

**Contents**

- `index.html` — the passphrase-protected interactive visual (AES-256-GCM encrypted content; nothing readable without the passphrase, including in page source)
- `.nojekyll` — stops GitHub trying to process the file through Jekyll
- `README.md` — this file

**Passphrase:** `overmatter-runaround-6006` — send separately from the link, never in the same message.

---

## Steps (about three minutes, all in the browser)

1. **New repo** at github.com/new — name it something neutral like `agent-framework-view`. **Public.** *(GitHub Pages on a private repo needs a paid plan; public is fine here because the content is encrypted.)*
2. **Upload** the contents of this folder — drag `index.html`, `.nojekyll` and `README.md` onto the repo page, commit.
3. **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main`, folder: `/ (root)` → Save.
4. Wait ~60 seconds. Your URL is `https://<your-username>.github.io/agent-framework-view/`
5. Open it, unlock with the passphrase, check it works before sharing.

## If you'd rather not have a public repo

- **GitHub Pages private** requires GitHub Pro/Team/Enterprise. If your account has it, make the repo private and Pages still works.
- **Cloudflare Pages / Netlify** — same drag-and-drop, and both offer password protection at the *hosting* layer on their paid tiers, which is stronger than file-level encryption because the content never leaves the server unlocked.
- **Just send the file** — `index.html` works offline. Open it in any browser from Teams or a download. No hosting needed.

## Updating it

Replace `index.html` and commit; Pages redeploys in about a minute. To regenerate after editing the source visual (`../agent-framework-architecture.html`), ask Claude to rebuild the protected version — the encryption is applied at build time, and the passphrase can be changed then.

## What this protects against, and what it doesn't

**Does:** the URL alone is useless. Search engines are told not to index it. Anyone finding the repo sees ciphertext.

**Doesn't:** once someone unlocks it, they can share what they saw. There's no expiry, no revocation, and no record of who opened it. If those matter, this belongs behind proper access control instead — an internal server or a hosting-layer password.

## Handling

WoodWing internal. Contains material derived from an internal product deck and anonymised customer conversations. Don't put the URL anywhere indexable, and don't paste the passphrase into the same channel as the link.
