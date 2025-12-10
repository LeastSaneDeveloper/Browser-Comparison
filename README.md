# Browser Comparison

**NOTE:** THIS PROJECT IS NOT COMPLETE YET.

## Introduction

I made this repository to provide a comparison of modern browsers, evaluating them across multiple metrics including privacy, security, performance, and compatibility with modern web standards.

With the information in this project, (hopefully) you will be able to make an informed choice. The goal is not to find a single “best” browser, the goal is to find the one which suits your threat model.

## Overview

Browsers are categorized based on their browser engine: Blink, Webkit, Gecko, and Goanna. That is, except for AI browsers, which will have its own section.

Each browser will be judged based on their privacy, security, performance, and web compatibility. In the end, my subjective rating will be given, with a 5-star system in place.

## Index

- [Introduction](#introduction)
- [Overview](#overview)
- [Index](#index)
- [Blink Browsers](#blink-browsers)
  * [Chromium](#chromium)
  * [Google Chrome](#google-chrome)

## Blink Browsers

Blink is a browser engine developed as part of the free and open-source Chromium project. Blink is by far the most-used browser engine, due to the market share dominance of Google Chrome and the fact that many other browsers are based on the Chromium code.

List of browsers discussed in this project:
- [Chromium](#chromium)
- [Google Chrome](#google-chrome)

## Chromium

Chromium is a free and open-source web browser project, primarily developed and maintained by Google. It provides the codebase for the vast majority of web browsers, such as Google Chrome, Microsoft Edge, Samsung Internet, Opera, etc.

### Privacy

Chromium [does not partition cookies](https://privacytests.org) in a normal window across different sites, which enables unique, cross-site identifiers to be linked to you. (NOTE: INCOGNITO MODE __DOES__ PARTITION COOKIES!)

Chromium also does not [remove tracking query parameters, even in Incognito Mode.](https://privacytests.org/private) Query parameters are information that is attached to an address. Tracking companies frequently add a tracking parameter to URLs in order to track you across sessions and sites.

[Known tracking scripts are also not blocked](https://privacytests.org/private) in both normal windows and Incognito windows. [By default, tracking cookies are also not blocked](https://privacytests.org) (__IN NORMAL WINDOWS ONLY. INCOGNITO MODE BLOCKS TRACKING COOKIES.__) Chromium also [does not prevent cross-session tracking](https://privacytests.org/private) in normal windows.

[Chromium leaks the most metadata when using WebRTC.](https://arxiv.org/abs/2510.16168)

Chromium provides no built-in way to spoof major fingerprinting vectors including Hardware metadata, screen resolution, Canvas, WebGL, Font, and AudioContext fingerprinting. In general, Chromium has very little privacy settings.

**VERDICT**: 1 star ⭐️

### Security

Chromium supports [site isolation](https://www.chromium.org/Home/chromium-security/site-isolation/), meaning each site runs in its own sandboxed rendering process. In general, Chromium browsers' site isolation is very mature, stable, and granular. You can read more about Chromium's security [here.](https://madaidans-insecurities.github.io/firefox-chromium.html)

In addition, [Chromium has ASLR (Address Space Layout Randomization), DEP (Data Execution Prevention), JIT hardening, SafeSEH,](https://www.chromium.org/Home/chromium-security/core-principles/) and other anti-exploit techniques.

Chromium has a feature called [Safe Browsing](https://www.chromium.org/Home/chromium-security/enamel/), which identifies malicious and phishing sites. Moreover, it automatically blocks known malware downloads and warns about potentially dangerous files.

[Chromium has robust memory safety features](https://www.chromium.org/Home/chromium-security/memory-safety#what-were-trying), as approximately [70% of all browser vulnerabilities](https://www.chromium.org/Home/chromium-security/memory-safety) are due to memory safety issues.

**VERDICT** (Subjective): 4.4 stars ⭐️⭐️⭐️⭐️

## Google Chrome

Google Chrome is a cross-platform web browser developed by Google. It is based on Chromium, which is based on Blink. As of 2025, it is the most used browser globally, with a 70% market share.

### Privacy

A [major class‑action lawsuit](https://www.macrumors.com/2020/06/03/lawsuit-google-chrome-tracking-incognito-users/) filed in 2020 accused Google of continuing to track users’ browsing activity even when they used Chrome’s Incognito mode, via tools like Google Analytics, Ad Manager, and related tracking utilities.

According to the complaint, Google’s representations (“You’ve gone Incognito,” “Now you can browse privately”) led many users to (very understandibly) expect that their web activity would not be sent to Google, but in practice [Chrome “continues to send the user’s browsing history and other data directly to Google’s servers” during Incognito sessions.](https://arstechnica.com/tech-policy/2024/01/chrome-updates-incognito-warning-to-admit-google-tracks-users-in-private-mode/)

In December 2023 Google agreed to settle the lawsuit and [committed to deleting “billions” of data records collected from users in Incognito mode.](https://time.com/6962521/google-incognito-lawsuit-data-settlement/).

As part of the settlement, Google also agreed to update the Incognito-mode startup screen (the “splash page”) to actually warn users that “data collected by websites and services they use (including Google)” might be unaffected by private browsing.

Although many browsers have moved to deprecate or block third‑party cookies (cookies set by domains other than the site you're visiting), Google has backtracked: in 2025 [Chrome announced it would not roll out a standalone prompt to phase out third‑party cookies](https://www.reuters.com/sustainability/boards-policy-regulation/google-opts-out-standalone-prompt-third-party-cookies-2025-04-22/), which implied that these tracking techniques still remain for Google Chrome users.

And it is not solely the browser. The entire business model for Chrome (and in whole, Google itself) depends on data collection and targeted advertising. Browsers that collect more user data produce more precise advertising profiles, which is [how Google makes money.](https://www.nasdaq.com/articles/how-much-does-google-make-ad-revenue)

A jury recently ordered Google to pay approximately US$425 million for [illegally collecting tens of thousands of users and devices' data](https://www.theverge.com/news/771540/google-class-action-verdict-user-privacy-tracking), even after they disabled tracking settings.

In 2025 Google settled a data‑privacy suit with the state of Texas Attorney General's Office for US$1.375 billion, because [Google secretly tracked](https://www.reuters.com/technology/texas-says-it-secures-138-billion-settlement-with-google-over-data-privacy-2025-05-09/) location history, biometric data, and Incognito-mode activity without proper user consent.

See [Chromium's Privacy section.](#chromium)

**VERDICT** (Subjective): 0 Stars

### Security

**(IMPORTANT: REMEMBER THAT GOOGLE CHROME IS A CHROMIUM-BASED BROWSER. WHEN I MENTION CHROMIUM, NOTE THAT CHROMIUM'S FEATURES ALSO EXTEND TO GOOGLE CHROME.)**

Due to Google Chrome being the most widely used browser in the world, it is affected by many [zero-day vulnerabilities.](https://en.wikipedia.org/wiki/Zero-day_vulnerability) Many bad actors specifically target it.

Google Chrome's mass-telemetry increases attack surface.

See [Chromium's Security section.](#chromium)

**VERDICT** (Subjective): 4 stars ⭐️⭐️⭐️⭐️
