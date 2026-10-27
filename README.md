# Vocal Practice Player — GitHub Pages

Public support and terms website for Vocal Practice Player. This repository is stored in the `pages/` folder, alongside the separate iOS app project in `../vocal-practice-player/`.

## Contents

- `index.html` — home page.
- `terms/index.html` — app information, subscription terms, and a link to Apple’s Standard EULA.
- `support/index.html` — support contact and frequently asked questions.
- `assets/styles.css` — shared responsive styles, with no external fonts, scripts, or analytics.
- `assets/app-icon.png` — the app’s actual iOS icon, used in the header and as the website icon.
- `.nojekyll` — serves the site as static files without Jekyll processing.

Support email: [maksim.karonchyk@gmail.com](mailto:maksim.karonchyk@gmail.com).

## GitHub Pages deployment

Repository: [un3solka/vocal-practice-player](https://github.com/un3solka/vocal-practice-player).

The website files are at this repository’s root. In GitHub **Settings → Pages**, choose **Deploy from a branch**, select the branch containing these files, and use **/ (root)** as the publishing folder. Push website updates to that branch and wait for the Pages deployment to finish.

Website URLs:

- [Home](https://un3solka.github.io/vocal-practice-player/)
- [Terms of Use](https://un3solka.github.io/vocal-practice-player/terms/)
- [Support](https://un3solka.github.io/vocal-practice-player/support/)

Verify the public URLs without signing in after deployment. Use the support page URL as the **Support URL** in App Store Connect. The terms page links to Apple’s Standard EULA; it does not replace that agreement.

The app’s website URLs are defined in `AppLinks` in the separate app project’s `VocalPracticePlayer/UI/StudioViews.swift`. Keep those URLs aligned with the website when changing repository ownership or adding a custom domain.

The privacy policy remains an in-app draft in the app project’s `legal/` folder. Its publication requirements are listed in `legal/RELEASE-CHECKLIST.md` in that project.

## Updating the icon

Copy `VocalPracticePlayer/Assets.xcassets/AppIcon.appiconset/AppIcon.png` from the app project to `assets/app-icon.png` whenever the app icon changes. All website pages share this asset.

## Local preview

From this repository’s root:

```sh
python3 -m http.server 8080
```

Open [localhost:8080](http://localhost:8080/). The links inside the iOS app use the published HTTPS website.
