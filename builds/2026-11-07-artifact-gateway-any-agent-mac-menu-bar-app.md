---
title: Mac menu bar app that opens AI artifacts by group
date: 2026-11-07
project: artifact-gateway
target_agent: any-agent
status: draft
visibility: public
version: 1
supersedes:
---

## Your job in one line

Build a macOS menu bar app that lists AI artifact links grouped by team or area, and opens each one in its own window, all driven by a config file.

## Hard rules

These override anything else you read.

- The app opens links only. It never sends, posts or changes anything on any site.
- Never store, read or handle passwords, session cookies or tokens in the app or the config. Sign-in happens in the window, by the user.
- The config holds names and links only. No secrets.
- Open only `https` links from the config. Skip anything else and say which entry was skipped.
- No telemetry, and no network calls besides loading the configured links.
- Don't publish, sign, notarize or share a build without the owner's yes.
- Work in a private repo until the owner says otherwise.

## Context

- Teams use AI artifacts (dashboards, trackers, small tools) but have to dig through the AI app to find them. One launcher, grouped by area, keeps each person on the few artifacts their work needs.
- A companion handoff builds the same idea as a web page: `2026-11-07-artifact-gateway-any-agent-hub-page.md`. Either can stand alone.
- The artifacts are hosted by an AI platform (for example Claude artifacts) and need the user to be signed in there to view them.
- Any data the artifacts show is refreshed elsewhere. This app only opens them.
- Fill in for your project: the groups, the artifact links, and the macOS versions you must support.

## Scope

- In: a menu bar icon, a menu grouped by area, one window per artifact, a config file for groups and links, reloading the config without a rebuild, and a short README on install and config.
- Out: editing artifacts, reading or writing artifact data, user accounts, syncing config across machines, app store distribution, and Windows or Linux.

## Steps, in order

1. Interview the owner, one question at a time, through the open questions below.
2. Write a one-page plan: the window approach, the config format, and an example config with two placeholder groups.
3. Get the owner's yes on the plan.
4. Test sign-in persistence (first open question) before building anything else.
5. Build the smallest version: menu from config, click opens one window.
6. Add reload, bad-entry handling and the README.

## Open questions

Ask the owner. Don't guess.

- Verify, don't assume: does a Safari "Add to Dock" web app window keep the AI platform's sign-in? Does a Chrome app window? Test both before choosing.
- Which window approach: an embedded web view, a Safari web app window, or a Chrome app window? Depends on the sign-in test.
- Native (Swift) or cross-platform (for example Tauri or Electron)?
- Config format and location: JSON or YAML, in the home folder or next to the app?
- Should a group be able to point at a hub page instead of listing every artifact?
- Who gets the app, and how: built by each person, or a shared signed build?
- Keyboard shortcut or launch at login?

## Done when

- The menu bar icon shows the groups and links from the config file.
- Clicking a link opens that artifact in its own window, and a second link opens a second window.
- Editing the config and choosing reload updates the menu without a rebuild.
- A bad entry (missing name, non-https link) is skipped with a clear message, and the rest still loads.
- The sign-in behavior is tested and written down, with the macOS and browser versions used.
- The README covers install, config format and the example config.

## Report back with

- The repo and branch, the window approach chosen and why, the sign-in test result, and anything still open.

## Platform notes

- macOS 13 and later have a built-in menu bar API for SwiftUI apps (`MenuBarExtra`). Check the current docs.
- Some sign-in providers block sign-in inside embedded web views. Include that in the sign-in test.
