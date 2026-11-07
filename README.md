# Codex Slider downloads

Customize Codex’s Default Slider with 3–7 model and reasoning presets.

**[Download 0.6.0](https://github.com/jiediking/codex-slider-downloads/releases/tag/v0.6.0)** · [DMG](https://github.com/jiediking/codex-slider-downloads/releases/download/v0.6.0/Codex-Slider-0.6.0-macOS-arm64.dmg) · [Checksums](https://github.com/jiediking/codex-slider-downloads/releases/download/v0.6.0/SHA256SUMS.txt)

## Requirements

- Apple Silicon Mac, macOS 15 or later.
- Codex desktop installed and signed in with ChatGPT.
- Native arm64 Node.js 22.x (22.22.3+), 24.x or 26.x. [Get Node.js 22](https://nodejs.org/en/download/archive/v22.23.3).

## Install or update

Quit every copy of Codex Slider, then copy this line into Terminal:

```sh
/bin/bash -o pipefail -c '/usr/bin/curl -fsSL https://raw.githubusercontent.com/jiediking/codex-slider-downloads/main/install.sh | /bin/bash'
```

No GitHub account, GitHub CLI, Python or npm setup is needed. The installer verifies the package checksum, app identity, signature, version and Node before installing to `/Applications/Codex Slider.app`. Saved presets are kept. macOS asks if administrator permission is needed.

Alternatively, open the DMG and drag Slider to Applications.

## Use

Open Slider, choose 3–7 unique model and reasoning pairs, drag to reorder, then choose **Save & launch Codex**. Read the local debugging explanation on first use. If Codex is running, save your work and quit it normally when prompted. Slider closes after successful application. Launch through Slider for custom presets; Codex’s regular icon uses its standard slider.

## Compatibility updates

**A normal Codex update no longer needs a manually added version entry.** Slider can verify an unlisted official installation locally. Your next custom launch checks the existing adapter, applies presets and reads them back before remembering success for that exact installation. This local check needs no online compatibility entry.

**Check compatibility** rechecks the installation and any published [signed data](https://raw.githubusercontent.com/jiediking/codex-slider-downloads/main/compatibility-feed.json), without changing presets or starting Codex. “Official Codex verified · adapter check on launch” means it is ready for the next step: launch Codex through Slider to complete the runtime check.

A confirmed interface or preset-schema mismatch asks for a new Slider adapter. Loading, missing configuration, ambiguous clients and timeouts ask you to retry. A changed installation invalidates the local result automatically. Every custom launch probes again. Signed data still provides reviewed compatibility information and known adapter requirements.

After installing, open `/Applications/Codex Slider.app` and check that its header says **v0.6.0**. To report a problem, run this read-only command; it does not start Codex or change presets:

```sh
"/Applications/Codex Slider.app/Contents/MacOS/CodexSlider" --diagnose
```

## Preview status

Unofficial; not affiliated with OpenAI. Locally signed and not Apple-notarized; a trusted download may require [Open Anyway](https://support.apple.com/en-us/102445). Codex 25241 passed local compatibility checks; live native-slider UI and inference remain unverified. Model access depends on your Codex account.

Application source remains private. This repository contains download instructions, the installer and signed compatibility data. Releases contain the app, installer and checksums; no Node runtime or developer files are bundled. Future versions use the same installation command.
