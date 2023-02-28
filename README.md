# Clean Firefox Installation

Most modern browsers are up to no good, mostly for privacy reasons, but some also fail to satisfy in user experience. This document provides a rough guidance on how to install Firefox so that it is up to par with other browsers.

## Installation

### Download Firefox ESR

Download [Firefox ESR](https://www.mozilla.org/en-US/firefox/enterprise/). The ESR version is much cleaner and provides more privacy than the normal version of Firefox.

### Install Add-Ons

Install these basic add-ons from [this collection](https://addons.mozilla.org/en-US/firefox/collections/12599599/MyAddons/). The most essential add-ons are:

- [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=collection): Ad blocker
- [I still don't care about cookies](https://addons.mozilla.org/en-US/firefox/addon/istilldontcareaboutcookies/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=collection): Block annoying cookie popups. This is the open source version of "I don't care about cookies".
- [Improve YouTube! (Open-Source for YouTube)](https://addons.mozilla.org/en-US/firefox/addon/youtube-addon/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=collection): Youtube feels slow in Firefox. This add-on fixes that.

### about:config settings

Type `about:config` in URL bar and set following parameters.

| Setting | Value | Type |Note |
|:- |:-:|:-:|:- |
|browser.tabs.tabMinWidth| 0 | | Make tabs squishy. |
|full-screen-api.transition-duration.enter | 0 0 | | Remove fullscreen transitions (slow). |
|full-screen-api.transition-duration.leave | 0 0 | | Remove fullscreen transitions (slow). |
|full-screen-api.warning.timeout | 0 | | Remove fullscreen warning. |

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
