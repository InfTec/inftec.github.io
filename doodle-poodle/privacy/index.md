---
title: Doodle-Poodle Privacy Policy
description: Privacy policy for the Doodle-Poodle kids' drawing-and-guessing game by InfTec GmbH.
---

<!--
  This file is a clean derivative of docs/privacy-policy.md from
  the (private) doodle-poodle app repository. The drafting notes
  and hosting checklist are stripped. Keep this in sync with the
  source on every revision.
-->

**Effective date:** 2026-05-10
**Last updated:** 2026-05-10

---

## Who we are

Doodle-Poodle is a kids' drawing-and-guessing game published by
**InfTec GmbH** ("we", "us"), registered in **Switzerland**.

Contact for privacy questions: **info@inftec.ch**.

## Plain-language summary

- We do **not** collect any personal information from you or your child.
- We do **not** track behaviour, identity, or location.
- Drawings the child makes never leave the device — they are recognised
  by a small machine-learning model that runs locally on the phone or
  tablet.
- The only things stored on the device are the child's earned reward
  count ("bones"), their chosen language, and a flag for whether the
  Pro upgrade is active. Uninstalling the app deletes all of it.
- Family-safe ads (when enabled) and one-time purchases are handled by
  Google or Apple under their own privacy terms.

If you want the formal version, read on.

---

## What information the app processes

### Information stored on the device only

The app keeps a small amount of state on the device so the game works
between sessions. None of it is transmitted, none of it identifies the
child, and uninstalling the app removes it all.

| Stored on device | Purpose | Where it lives |
|---|---|---|
| Earned-reward ("bones") count | Show the child their progress | Application documents directory (single JSON file) |
| Language preference (`en` / `de`) | Render the UI in the chosen language | Operating-system shared preferences |
| Pro-upgrade flag | Unlock the full category list | Operating-system shared preferences |
| Round-finish counter | Pace the periodic Pro upgrade prompt | Operating-system shared preferences |

The recognised drawings themselves exist only in memory while the
child is drawing and are discarded between rounds.

### Information processed locally and discarded

While the child draws, the strokes are converted to a small image
tensor and run through a machine-learning model bundled inside the app.
The model never leaves the device, the inputs never leave the device,
and the prediction is immediately consumed by the UI to show the
top-three guesses. Nothing about the drawing or the prediction is
saved or transmitted.

### Information we do not collect

We do not collect, transmit, or sell:

- Names, email addresses, phone numbers, or any other contact details
- Account or login credentials (the app has no account system)
- Photos, contacts, location, microphone, or camera data
- Advertising identifiers or device identifiers
- Crash reports or analytics events
- Behavioural profiles of any kind

The app holds the `INTERNET` permission solely to allow the
embedded Google AdMob and Google Play Billing SDKs to reach
their respective Google endpoints. Drawings, audio recordings,
recognition results, settings, and any other content created by
the child never leave the device.

## Third-party services

The app embeds two Google SDKs. Both are required to deliver the
features they support; both are configured to minimise data
exposure.

### Google AdMob (banner ads, family-safe inventory only)

Banner ads are served by Google AdMob using the family-safe ad
inventory. The integration is configured per Google's Designed
for Families requirements:

- `tagForChildDirectedTreatment` set to `yes` — Google treats the
  request as for a child-directed app and serves only family-safe
  inventory.
- `tagForUnderAgeOfConsent` set to `yes`.
- Maximum ad content rating set to `G`.
- Non-personalised ads only — Google does not use the request to
  build a behavioural profile.
- No interstitial or rewarded ads in interrupting positions; ads
  appear only on the home and settings screens, and never block
  gameplay.
- The Pro upgrade removes ads entirely.

AdMob's own privacy practices are documented at
[`policies.google.com/privacy`](https://policies.google.com/privacy)
and [`support.google.com/admob/answer/6128543`](https://support.google.com/admob/answer/6128543).

### Apple App Store / Google Play (in-app purchases)

Doodle-Poodle offers a single, optional, one-time Pro upgrade.
The purchase itself is processed by Apple or Google, not by us. We
receive only the result of the transaction (purchased / not
purchased) so we can unlock the Pro features on the device. We do
not see the buyer's name, email address, or payment details.

The purchase entry point is gated by a parental-gate dialog (a
small math problem) so it cannot be triggered accidentally by a
child.

Apple's privacy practices are documented at
[`apple.com/privacy`](https://www.apple.com/privacy/). Google's are
at [`policies.google.com/privacy`](https://policies.google.com/privacy).

### No analytics, no crash reporting, no third-party tracking

Doodle-Poodle does not use Firebase, Amplitude, Mixpanel, Sentry,
Crashlytics, or any other analytics or crash-reporting SDK. There
are no third-party trackers, fingerprinting libraries, or
advertising attribution SDKs.

## Children's privacy (COPPA, GDPR-K)

Doodle-Poodle is designed for children. We comply with:

- **COPPA** (US Children's Online Privacy Protection Act) — we
  collect no personal information from anyone under 13, so no
  parental consent is required.
- **GDPR-K** (EU General Data Protection Regulation, Article 8) —
  the same applies: we collect no personal data from any user,
  irrespective of age.
- **Apple Kids Category** and **Google Play Designed for Families**
  programme requirements — no third-party analytics, no
  behavioural advertising, parental gate in front of any purchase
  or external link.

If you believe your child has somehow shared personal information
with us (we do not know how this would happen given the design, but
we want to be safe), please contact us at the email address above
and we will delete anything we have, although we expect to find
nothing.

## How long we keep information

We do not store any personal information, so there is nothing to
retain. The on-device state listed above is kept until you delete
the app or clear its storage.

## Your rights

Because we do not collect personal data, the data-subject rights
under GDPR (access, rectification, erasure, portability, objection)
are practically inapplicable: there is nothing to access, rectify,
erase, or port. You may, however, contact us at any time at the
email above with questions about this policy or our practices.

If you wish to delete the app's on-device state without uninstalling,
you can do so via the operating system's app-storage controls
(Settings → Apps → Doodle-Poodle → Storage → Clear data on Android;
delete and reinstall the app on iOS).

## Security

The app's local storage relies on the security model of the host
operating system (sandboxed app data, OS-level encryption when
enabled by the user). Because we transmit nothing, there is no
network attack surface for the data we process.

## Changes to this policy

If we change this policy materially — for example, when ads or
in-app purchases are first enabled — we will update the "Last
updated" date and post a clearly visible notice in the app's
Settings → About section. For any change that affects what data
leaves the device (currently nothing does), we will give at least
30 days' notice in-app before the change takes effect.

## Contact

Questions, requests, or concerns about this policy:
**info@inftec.ch**

Postal address (for formal data-protection requests):
**InfTec GmbH, Grubenstrasse 7b, 3322 Urtenen-Schönbühl, Schweiz**
