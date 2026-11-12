# ShowTake plugin for Codex and ChatGPT

Let your coding agent film polished demo videos and App Store screenshots of your iOS (Simulator) and Mac apps with
[ShowTake](https://showtake.app/?utm_source=github&utm_medium=readme&utm_campaign=codex-plugin).

This repository is a plugin marketplace for the Codex CLI, the Codex IDE extensions and the ChatGPT desktop app. The
`showtake` plugin bundles:

- the ShowTake MCP server (local, runs on your Mac: recordings never leave it),
- `setup-showtake`: installs ShowTake (after you confirm) and checks the setup with `doctor`,
- `film-app-demo`: plans the steps, films a clean take and exports App Store previews, screenshots and social cuts.

## Install

Requires macOS 26 or later. iOS apps also need Xcode with an iOS Simulator runtime.

```sh
codex plugin marketplace add orchestero/showtake-codex-plugin
```

Then open the Plugins Directory (Codex app or ChatGPT desktop), choose the **ShowTake** marketplace and install the
plugin, and start a new session. If ShowTake isn't installed yet, ask: "Set up ShowTake".

Update later with `codex plugin marketplace upgrade showtake`.

## Use

```text
Make a 20-second demo video of my iOS app's onboarding.
Export an App Store preview and screenshots of my app.
Film my Mac app adding and completing a task.
```

ShowTake is free to try (exports carry a watermark); Pro removes it. See https://showtake.app/pricing.

## License

The files in this repository (plugin manifest, skills, marketplace file) are MIT licensed. ShowTake itself is
proprietary software: see https://showtake.app/terms.
