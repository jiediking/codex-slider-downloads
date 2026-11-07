# Codex Slider

Arrange **3–7 model and reasoning presets**, then launch Codex with your custom slider.

**[Download 0.6.4](https://github.com/jiediking/codex-slider-downloads/releases/tag/v0.6.4)** · [DMG](https://github.com/jiediking/codex-slider-downloads/releases/download/v0.6.4/Codex-Slider-0.6.4-macOS-arm64.dmg) · [Checksums](https://github.com/jiediking/codex-slider-downloads/releases/download/v0.6.4/SHA256SUMS.txt)

## Requirements

- Apple Silicon Mac, macOS 15 or later.
- Codex desktop installed and signed in with ChatGPT.
- Native arm64 Node.js 22.x (22.22.3+), 24.x or 26.x. [Get Node.js 22](https://nodejs.org/en/download/archive/v22.23.3).

No API key, GitHub login, GitHub CLI, Python, Xcode or npm setup is needed.

## Install or update

Quit every copy of **Codex Slider**, then copy this line into Terminal:

```sh
/bin/bash -o pipefail -c '/usr/bin/curl -fsSL https://raw.githubusercontent.com/jiediking/codex-slider-downloads/main/install.sh | /bin/bash'
```

The installer verifies the package, signature and Node, installs `/Applications/Codex Slider.app`, and selects it in Finder. Open Slider and confirm **v0.6.4**. Saved presets are kept. If needed, macOS asks for administrator permission. You can also open the DMG and drag Slider to Applications.

## Use

1. Choose 3–7 unique model/reasoning pairs. Drag to reorder.
2. Choose **Save & launch Codex**. Read the local debugging explanation on first use. If Codex is running, save your work and quit it normally when prompted.
3. Continue in Codex. Slider checks your presets and current selection automatically, **even with the Default model menu closed**. After **Your slider is ready**, the entire Slider app exits in about one second. Codex keeps running with your presets.

While checking, the screen offers **Go to Codex** and **Edit presets**; use the window × to close Slider. Pending or failed checks keep it open. A read error offers **Check again**. Editing cancels the automatic exit.

Launch through Slider for custom presets. Codex’s regular icon uses its standard slider. A renderer reload may require another launch through Slider.

## Compatibility and help

Codex updates do not normally need a new [signed-list](https://raw.githubusercontent.com/jiediking/codex-slider-downloads/main/compatibility-feed.json) entry. Slider verifies an official installation, tries the existing adapter, and independently checks Codex’s committed picker presets and visible current selection. An open menu also checks its rendered stops.

Loading, unavailable models or missing evidence stays unconfirmed. If checking stalls, open Codex’s Default model menu. **Check compatibility** in the editor rechecks the installation and retries the current session. Only confirmed configuration incompatibility or a stable, fully available picker mismatch asks for an adapter update. Every custom launch checks again; old records and configuration read-back alone cannot trigger success or exit.

Presets are saved in `~/Library/Application Support/Codex Slider/settings.json`. The latest launch evidence is `last-launch.json` in the same folder. A read-only installation report is available with:

```sh
"/Applications/Codex Slider.app/Contents/MacOS/CodexSlider" --diagnose
```

The static report does not start Codex; its `consumerVerified: false` is not a live-session verdict.

Unofficial; not affiliated with OpenAI. Model access depends on your Codex account. This preview is locally signed and not Apple-notarized; a trusted download may require [Open Anyway](https://support.apple.com/en-us/102445). Slider sends no inference requests and installs no files inside Codex.

Application source remains private. This repository contains download instructions, the installer and signed compatibility data. Releases contain the app, installer and checksums. Node is not bundled. Use the same command for future updates.
