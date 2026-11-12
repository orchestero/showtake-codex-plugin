---
name: setup-showtake
description: Set up ShowTake on this Mac so the agent can film demo videos of the user's iOS (Simulator) and Mac apps. Use right after installing the ShowTake plugin, or when the ShowTake tools (list_targets, start_take, export, doctor) are missing.
---

# Set up ShowTake

ShowTake (https://showtake.app) is a Mac app (macOS 26 or later) with a built-in MCP server. Recording and rendering
run on the user's Mac; nothing is uploaded.

1. Check whether the ShowTake tools are already available in this session (for example `doctor`). If they are,
   call `doctor`, apply any fix it returns, and stop here.
2. Check for the app: `test -x /Applications/ShowTake.app/Contents/MacOS/showtake-mcp`.
3. If it is missing, tell the user you are about to install ShowTake and ask them to confirm. Then install it with
   Homebrew (`brew install --cask orchestero/tap/showtake`) if `brew` exists. Otherwise give the user the download
   link https://showtake.app/download (a notarized DMG) and wait until they have moved it to Applications.
4. This plugin already declares the ShowTake MCP server (`mcp.json`). If the tools still do not appear (older hosts), register it by hand:
   `codex mcp add showtake -- "/Applications/ShowTake.app/Contents/MacOS/showtake-mcp"`
5. Tell the user to start a new session so the ShowTake tools load. On the first take, macOS asks once for
   Accessibility and Screen Recording access for ShowTake: the user has to click Allow in System Settings.
6. In the new session, call `doctor` and follow its fix steps until it reports no problems.

iOS apps also need Xcode with an iOS Simulator runtime; `doctor` reports exactly what is missing and how to add it.
