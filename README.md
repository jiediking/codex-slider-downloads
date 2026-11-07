# Codex Slider downloads

Customize Codex’s Default Slider with 3–7 model and reasoning presets.

**[Download 0.5.0](https://github.com/jiediking/codex-slider-downloads/releases/tag/v0.5.0)** · [DMG](https://github.com/jiediking/codex-slider-downloads/releases/download/v0.5.0/Codex-Slider-0.5.0-macOS-arm64.dmg) · [Checksums](https://github.com/jiediking/codex-slider-downloads/releases/download/v0.5.0/SHA256SUMS.txt)

## Requirements

- Apple Silicon Mac, macOS 15 or later.
- Codex desktop installed and signed in with ChatGPT.
- Native arm64 Node.js 22.x (22.22.3+), 24.x or 26.x. [Get Node.js 22](https://nodejs.org/en/download/archive/v22.23.3).

## Install or update

Close Codex Slider, then copy this line into Terminal:

```sh
/bin/bash -o pipefail -c '/usr/bin/curl -fsSL https://raw.githubusercontent.com/jiediking/codex-slider-downloads/main/install.sh | /bin/bash'
```

No GitHub account, GitHub CLI, Python or npm setup is needed. The installer checks the package checksum, app signature, version and Node before installing to `/Applications/Codex Slider.app`. It keeps saved presets and asks through macOS if administrator permission is needed.

Alternatively, open the DMG and drag Codex Slider to Applications.

## Use

Open Slider, choose 3–7 unique model and reasoning pairs, drag to reorder, then choose **Save & launch Codex**. On first use, read the local debugging explanation. If Codex is running, save your work and quit it normally when prompted. Slider closes after successful application. Open Codex through Slider for custom presets; its regular icon uses the standard slider.

## Preview status

This is an unofficial preview, not affiliated with OpenAI. The app is locally signed and not Apple-notarized; a trusted download may require [Open Anyway](https://support.apple.com/en-us/102445). Codex 25241 passed local compatibility checks; live slider UI and inference remain unverified. Model access depends on your Codex account.

Application source remains private during validation. This repository contains download instructions, the installer and signed compatibility data; release attachments contain the app, installer and checksums. No Node runtime is bundled. Future versions use the same installation command.

## Signed compatibility updates

[The signed compatibility list](https://raw.githubusercontent.com/jiediking/codex-slider-downloads/main/compatibility-feed.json) is public and requires no account. Existing Slider 0.5.0 users can enable this source once:

```sh
"/Applications/Codex Slider.app/Contents/MacOS/CodexSlider" --set-compatibility-url https://raw.githubusercontent.com/jiediking/codex-slider-downloads/main/compatibility-feed.json
```

Then choose **Check compatibility again**. An unchanged adapter needs only a reviewed signed-list update; an actual adapter change requires a new Slider version. Enabling the source does not declare unreviewed Codex builds compatible.
