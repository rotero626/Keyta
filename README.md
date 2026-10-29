# Keyta website (static, for GitHub Pages)

Plain HTML and CSS. No build step, no scripts, no cookies, no external fonts. Open `index.html` in a browser to preview.

Files: `index.html`, `server.html`, `privacy.html`, `support.html`, `terms.html`, `style.css`, `.nojekyll`.

## Before you publish

Search the folder for `TODO(Alex)` and fix every one (support email, download links, version, App Store link). The privacy and support pages are not finished without the email address.

    grep -rn "TODO(Alex)" Site/

## Publish on GitHub Pages

1. Sign in at github.com. Choose **New repository**.
2. Name it. Two good choices:
   - `keyta` (URL will be `https://rotero626.github.io/Keyta/`), or
   - `rotero626.github.io` (URL will be `https://rotero626.github.io/`, shorter).
   Set it to **Public** (free Pages needs a public repo). Create it.
3. Upload the **contents** of the `Site` folder (not the folder itself): on the new repo page choose **uploading an existing file**, drag in all the files, including `.nojekyll` (hidden files may need Finder's Cmd-Shift-. to show), and **Commit changes** to `main`. `index.html` must be at the top level of the repo.
4. Go to **Settings, Pages**. Under **Build and deployment**, set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`, and **Save**.
5. Wait a minute or two. The page shows "Your site is live at ...". Open each page and check it.
6. Optional: for a custom domain, set it under Settings, Pages, Custom domain, and tick Enforce HTTPS. Do this before submitting, because the URLs go on the App Store and cannot silently change.

Host the Keyta Server downloads separately, for example as assets on a **GitHub Release** in the same or another repo (Releases, Draft a new release, attach `KeytaServer-Windows-Setup.exe`, `KeytaServer-Windows.zip`, `KeytaServer-macOS.dmg`). Then put the release asset URLs into `server.html` (they look like `https://github.com/rotero626/keyta/releases/download/v1.0/KeytaServer-macOS.dmg`).

## URLs to use

If the repo is `keyta` (replace `rotero626`; for a `rotero626.github.io` repo drop `/keyta`):

| Where | Value |
|---|---|
| `KeytaLinks.serverDownload` | `https://rotero626.github.io/Keyta/server.html` |
| `KeytaLinks.privacyPolicy` | `https://rotero626.github.io/Keyta/privacy.html` |
| `KeytaLinks.support` | `https://rotero626.github.io/Keyta/support.html` |
| `KeytaLinks.termsOfUse` | leave as Apple's EULA (already set), or `https://rotero626.github.io/Keyta/terms.html` |
| App Store Connect: Privacy Policy URL | `https://rotero626.github.io/Keyta/privacy.html` |
| App Store Connect: Support URL | `https://rotero626.github.io/Keyta/support.html` |
| App Store Connect: Marketing URL | `https://rotero626.github.io/Keyta/` |
| App Store Connect: Terms (EULA) | leave on Apple's standard EULA; if the Description or a Terms field asks for a link, use the Apple EULA URL |
| Subscription pages (App Store Connect) | Privacy Policy URL as above |

Check that every URL returns 200 in a private browser window before submitting.
