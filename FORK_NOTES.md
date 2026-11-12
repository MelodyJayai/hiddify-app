# Fork notes

This repository is a fork of [hiddify/hiddify-app](https://github.com/hiddify/hiddify-app). All credit for the
application goes to the Hiddify authors and contributors. The fork is kept public and in sync with upstream, as
the upstream license asks, and stays under the same license (see `LICENSE.md`), including its non-commercial
and share-alike terms.

## Purpose

Private interoperability testing of newer proxy transports (VLESS + XHTTP + REALITY, VLESS Encryption) against
our own Xray-core servers, on Android first. Builds are for our own test devices: they are not published to any
app store and no GitHub release is made from this fork.

## Changes relative to upstream

| Date | Change |
|---|---|
| 2026-11-12 | Added `.github/workflows/fork-android.yml`: a manually started GitHub Actions workflow that builds the Android APKs, signs them with this fork's own key and keeps them as a workflow artifact. No application code is changed. |
| 2026-11-12 | Added this file and a pointer to it at the top of `README.md`. |

Application code, name, package id and UI are unchanged from upstream at this point. Any later change to the
application or to the core (`hiddify-core`, forked at `MelodyJayai/hiddify-core`) will be listed in the table above.

## Builds

Every build of this fork is produced by GitHub Actions (`Actions` -> `Fork - Android APK` -> `Run workflow`).
The APKs are signed with a key that is different from the upstream one, so a fork build cannot be installed
over an official Hiddify install (and the other way round) without uninstalling first.
