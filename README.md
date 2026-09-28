# Shailu Bhai Daily Collection

This repository packages the existing **Shailu Bhai Daily Collection** HTML app as an Android APK using Capacitor.

## Important

- The existing app logic in `www/index.html` is kept as the source of truth.
- WhatsApp buttons/messages remain part of the app.
- No advertisements, ad SDKs, ad banners, or ad popups are added.
- Customer and payment data remains local to each installed device through the app's existing browser storage design.
- The APK is not a PWA and does not require PWABuilder.

## Build APK on GitHub

1. Create a GitHub repository.
2. Upload all files from this folder to the repository root.
3. Open **Actions**.
4. Run **Build Android APK** (or push a commit; the workflow also runs on pushes).
5. Open the completed workflow run.
6. Download the artifact named `ShailuBhai-DailyCollection-APK`.
7. Inside it is `ShailuBhai-DailyCollection-debug.apk`.

The APK is a debug build intended for direct installation/sharing. A signed release APK can be added later if Play Store distribution is needed.

## Functionality

The supplied HTML app is not rewritten into a different UI/framework. The Capacitor Android shell loads the same `www/index.html`, so the existing customer, payment, partial/late payment, advance/payment flows, history, reports, expenses, backup/restore, Excel, recovery/trash, settings, and WhatsApp flows remain the source functionality.

## Network-dependent features

The current source uses WhatsApp web links for WhatsApp actions and loads the SheetJS Excel library from its existing CDN URL. Therefore WhatsApp needs WhatsApp/network availability, and Excel import/export needs internet access unless the library is later bundled locally.
