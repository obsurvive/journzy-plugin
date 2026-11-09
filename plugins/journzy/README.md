# Journzy

Journzy is a writing app for novelists. This plugin connects your AI assistant to your Journzy
account so that it can read the books you choose and help you with them: find continuity slips,
recall a character's details, check the timeline, prepare a revision pass, and explain the
results of Journzy's writing checks.

**It is read-only.** The assistant can read your books and give you notes. It cannot change your
text, your story bible or your settings. Only you change the text, in Journzy.

## What is inside

- **The Journzy connector**: one remote MCP server at `https://write.journzy.com/mcp`. You sign
  in with your Journzy account on Journzy's own page, and you choose which projects this app can
  read. Nothing is open until you choose.
- **Five skills** that teach the assistant how to help an author:
  - `journzy-getting-started`: list your projects and books, and find your way around an outline.
  - `journzy-continuity-question`: check whether a detail changed, where something first
    appears, and whether dates and events agree.
  - `journzy-story-bible-brief`: a short brief on a character, place, thread or world entry,
    with sources, and without spoilers past a chapter you name.
  - `journzy-revision-notes`: editorial notes and a revision checklist for a scene, a chapter or
    a book, from the text, Journzy's open notes and your own comments.
  - `journzy-style-check`: run Journzy's writing checks on a scene and explain them.

## Install

In Claude Code:

```bash
/plugin marketplace add obsurvive/journzy-plugin
/plugin install journzy@journzy
```

In the Claude apps, find Journzy in the plugin directory and add it; then connect Journzy
on the plugin's Connectors tab.

## How to use it

1. Install the plugin, then connect Journzy when your assistant asks you to (or from its list of
   connectors).
2. Sign in on the Journzy page that opens, tick the projects this app may read, and approve.
3. Ask in your own words, in English or Spanish. For example:
   - "List my Journzy books and show me the outline of the first one."
   - "Did Diego's eye colour change anywhere in my book?"
   - "Give me notes on the lighthouse scene in chapter 5, without rewriting it."

To change which projects the app can read, or to disconnect it, open Journzy, Settings,
Connected apps.

## What data it sends and fetches

- The plugin itself runs no code on your computer and stores nothing. It contains only text
  instructions (the skills) and the address of the Journzy connector.
- When the assistant calls a Journzy tool, Journzy sends it the parts of your opened projects
  that the tool returns: outline, scene text, search results, story bible entries, check
  results, Journzy's notes and your own comments. That text goes to the AI service you use, and
  that service's terms apply to it. Journzy's no-training promise covers Journzy only.
- Journzy keeps an audit record of which items each connected app read (ids, never text), so you
  can see it in Connected apps. Journzy's privacy policy: https://journzy.com/en/privacy.
- The connector never fetches other websites and never sends your data to anyone else.

## Support

Write to the address on https://journzy.com/en/about; a person on the team will reply.
Journzy: https://journzy.com/en. Privacy: https://journzy.com/en/privacy. Terms:
https://journzy.com/en/terms.

## Licence

Copyright 2026 Obsurvive, Inc. Licensed under the Apache License, Version 2.0 (see `LICENSE`).
