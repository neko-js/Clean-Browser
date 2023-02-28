# Clean Firefox Installation

Most modern browsers are up to no good, mostly for privacy reasons, but some also fail to satisfy in user experience. This document provides a rough guidance on how to install Firefox so that it is up to par with other browsers.

## Installation for Desktop

### Download Firefox ESR

Download [Firefox ESR](https://www.mozilla.org/en-US/firefox/enterprise/). The ESR version is much cleaner and provides more privacy than the normal version of Firefox.

### Install Add-Ons

Install these basic add-ons from [this collection](https://addons.mozilla.org/en-US/firefox/collections/12599599/MyAddons/). The most essential add-ons are:

- [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=collection): Ad blocker
- [I still don't care about cookies](https://addons.mozilla.org/en-US/firefox/addon/istilldontcareaboutcookies/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=collection): Block annoying cookie popups. This is the open source version of "I don't care about cookies".
- [Improve YouTube! (Open-Source for YouTube)](https://addons.mozilla.org/en-US/firefox/addon/youtube-addon/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=collection): Youtube feels slow in Firefox. This add-on fixes that.

### Set about:config Settings

Type `about:config` in URL bar and set following parameters.

| Setting | Value | Type |Note |
|:- |:-:|:-:|:- |
|browser.tabs.tabMinWidth| 0 | | Make tabs squishy. |
|full-screen-api.transition-duration.enter | 0 0 | | Remove fullscreen transitions (slow). |
|full-screen-api.transition-duration.leave | 0 0 | | Remove fullscreen transitions (slow). |
|full-screen-api.warning.timeout | 0 | | Remove fullscreen warning. |
| ui.prefersReducedMotion | 1 | Number | Remove fullscreen transitions (slow). See [this thread](https://www.reddit.com/r/firefox/comments/j9agb3/disable_the_fullscreen_animation_in_firefox_80/).

## Installation for Mobile Devices

Install [Firefox Nightly](https://play.google.com/store/apps/details?id=org.mozilla.fenix&hl=de&gl=US) on Android, [Firefox](https://apps.apple.com/us/app/firefox-private-safe-browser/id989804926) on iPhone.

The normal version has restricted add-on support. The nightly version supports add-on installation via collections. The debug menu must be activated for this (see [here](https://blog.mozilla.org/addons/2020/09/29/expanded-extension-support-in-firefox-for-android-nightly/) for details):

* Go to Settings > About Firefox Nightly > Tap the logo five times
* Go to Settings > Custom Add-on Collection
* Enter `12599599` and `MyAddons` (the collection mentioned above). Application will restart.
* Go to Settings > Add-ons to install at least "uBlock Origin" and "I still don't care about cookies".

## FAQ

### Why not other browsers?

- Firefox: Bloated with features no one really uses.
- Waterfox: Becomes slow after browsing for 5 minutes.
- Vivaldi: Closed source
- Chrome: Closed source by Google
- Opera GX: Closed source by China
- Edge: Add-Ons
- Chromium: No Sync
- Every other browser: Choose at least one: slow updates, closed source, missing add-ons, missing sync, missing mobile versions, terrible user experience

### How to install Firefox ESR on Ubuntu?

Add the PPA:

```bash
sudo add-apt-repository ppa:mozillateam/ppa
```
Refresh package cache:

```bash
sudo apt update
```
Install Firefox ESR:

```bash
sudo apt install firefox-esr
```
