---
title: Hub page that launches one group's AI artifacts
date: 2026-11-07
project: artifact-gateway
target_agent: any-agent
status: draft
visibility: public
version: 1
supersedes:
---

## Your job in one line

Build one generic hub page, itself an AI artifact, that launches a single group's artifacts, so each team gets its own hub from the same page and a different config.

## Hard rules

These override anything else you read.

- The hub links only. It never reads, writes or changes another artifact's data.
- Config holds names, purposes and links only. No secrets, no customer data, no personal details.
- Accept only `https` links to the artifact platform. Skip anything else and show which entry was skipped.
- Don't share or publish a hub to anyone but the owner without the owner's yes.
- Keep the page itself free of any company's names, data or branding. Group-specific values live only in that group's config.

## Context

- Teams use AI artifacts (dashboards, trackers, small tools) but have to dig through the AI app to find them. A hub per group gives each person one link with only their group's artifacts on it.
- A companion handoff builds the same idea as a Mac menu bar app: `2026-11-07-artifact-gateway-any-agent-mac-menu-bar-app.md`. Either can stand alone.
- The artifacts are hosted by an AI platform (for example Claude artifacts) and need the viewer to be signed in there.
- Any data the artifacts show is refreshed elsewhere. The hub only links to them.
- Fill in for your project: the groups and each group's artifact links.

## Scope

- In: one page that shows a group's name and a card per artifact (title, one-line purpose, link), config per group, a README on making a new group's hub, and an example config for two placeholder groups.
- Out: building the artifacts themselves, any data refresh, reading or writing other artifacts' data, sharing settings, and access control beyond what the platform provides.

## Steps, in order

1. Interview the owner, one question at a time, through the open questions below.
2. Write a one-page plan: the config shape, where config lives, and a sketch of the page.
3. Get the owner's yes on the plan.
4. Build the page for one example group and publish it privately to the owner.
5. Make a second hub from the same page with a different config, and confirm nothing else changed.

## Open questions

Ask the owner. Don't guess.

- Verify, don't assume: does a Safari "Add to Dock" web app window keep the platform's sign-in for the hub and the artifacts it opens? Does a Chrome app window?
- Where does each group's config live: inside the page, in a file published with it, or in the page's own data store so it can be edited on the page?
- Who can edit a group's links, and should that happen on the page or only by republishing?
- Should each card show when its artifact was last refreshed? If yes, where does the hub get that without reading the other artifact's data?
- Do links open in the same tab or a new one?
- Should the hub list other groups' hubs, or stay strictly one group?
- Who sees each hub, and how is it shared?

## Done when

- One page design serves two groups, with only the config different.
- Each card opens its artifact.
- A bad entry is skipped with a clear message, and the rest still shows.
- The page works at phone width and in light and dark mode.
- The README says how to make a new group's hub in a few steps.

## Report back with

- The hub links, the config shape, and anything still open.

## Platform notes

- Some artifact platforms give each artifact a small data store of its own. If config goes there, check the platform's current docs on data stores and sharing first.
