# ULTROZ — Cross-platform gaming prototype

A responsive gaming discovery/store prototype with a black, neon-purple and cyan design system.

## Features in this prototype
- Responsive desktop and mobile navigation
- Game discovery, search, detail pages, and a demo library
- Store product cards, categories, search, wishlist, item details, quantity controls, cart subtotal, and demo checkout
- PWA manifest, app icon, service-worker shell cache, and install prompt support
- Capacitor configuration to package the web app as an Android app

## Run the web app locally
The simplest route is to serve this folder with any local web server. For a development build:

1. Install Node.js (LTS).
2. Run `npm install`
3. Run `npm run start`
4. Open the local URL shown in the terminal.

PWA install and service-worker features require HTTPS or localhost. Opening `index.html` directly as a file will still show the UI, but install/offline support will not be active.

## Android project setup
Requires Node.js LTS and Android Studio with an Android SDK.

1. Run `npm install`
2. Run `npm run build`
3. Run `npm run android:add` once to create the native Android project.
4. Run `npm run android:sync` after changes.
5. Run `npm run android:open` to open the Android project in Android Studio.
6. In Android Studio, use Run to test on an emulator/device, or Build > Generate Signed Bundle / APK for a release build.

This bundle contains the web app and Android packaging configuration; it does **not** include a prebuilt APK or Play Store publication.

## Important limitations
- The store is a demo catalogue with sample cosmetic concepts and sample prices.
- Checkout is deliberately non-functional: no real payment provider is connected and no payment data is collected.
- Login, synced accounts, real player inventories, multiplayer, live game integrations, and backend APIs are not implemented.
- Wishlist, cart, and library state currently live in memory and reset when the app reloads.
- Before real purchases, add a secure backend, server-side price validation, order records, refund handling, and a trusted payment provider. Never put payment secrets in client-side code.
