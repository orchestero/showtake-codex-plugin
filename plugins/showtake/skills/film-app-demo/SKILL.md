---
name: film-app-demo
description: Film a short demo video of the user's own iOS app (in the iOS Simulator) or native Mac app with ShowTake, then export App Store App Previews, the App Store header video, social cuts (X, TikTok, Reels, Shorts, LinkedIn) or App Store screenshots. Use when the user asks for a demo, launch, promo or App Store preview video, app screenshots, or to re-shoot a saved demo for a new build or language.
---

# Film an app demo with ShowTake

This needs the ShowTake MCP tools. If they are missing, follow the `setup-showtake` skill first.

1. If anything fails or looks misconfigured, call `doctor` first and apply the fix it returns.
2. Read the MCP resource `showtake://guide` once: it is the full, current guide for these tools.
3. `list_targets`, then `prepare_ios` (project + scheme) or `prepare_macos` (app path or bundle id).
4. Explore briefly, then plan **6-8 steps, 15-30 s**, one story, a caption of at most 8 plain words per step.
5. `launch_app` with `fresh: true`, `start_take`, run exactly the planned steps, `end_take`. If the take is not
   clean, read `issues`, adjust and retake (up to 3 times) without asking.
6. `save_flow`, then `render` and `export` the presets the user asked for. Report the file paths.

Rules: one action at a time; never explore inside a take; only film the user's own apps; ask the user only for
login walls (demo-mode launch arguments or test data, never real credentials). Free exports carry a watermark at
1080p. On `license_required`, tell the user which preset needs ShowTake Pro (see https://showtake.app/pricing) and
do not retry.
