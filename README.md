# Codex Slider downloads

Customize Codex’s Default Slider with 3–7 model and reasoning presets.

**[Download 0.6.1](https://github.com/jiediking/codex-slider-downloads/releases/tag/v0.6.1)** · [DMG](https://github.com/jiediking/codex-slider-downloads/releases/download/v0.6.1/Codex-Slider-0.6.1-macOS-arm64.dmg) · [Checksums](https://github.com/jiediking/codex-slider-downloads/releases/download/v0.6.1/SHA256SUMS.txt)

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

Open Slider, choose 3–7 unique model and reasoning pairs, drag to reorder, then choose **Save & launch Codex**. Read the local debugging explanation on first use. If Codex is running, save your work and quit it normally when prompted. After configuration read-back, Slider stays open so you can check its actual effect in Codex and then close Slider manually. Launch through Slider for custom presets; Codex’s regular icon uses its standard slider.

## Compatibility checks

For a build outside the [signed list](https://raw.githubusercontent.com/jiediking/codex-slider-downloads/main/compatibility-feed.json), Slider can verify the official installation and try the existing adapter during your next custom launch. Configuration read-back alone does not prove that the slider adopted the presets.

**0.6.1 fixes false success reporting.** After presets are written and read back, the result remains **Slider effect not confirmed**. The window stays open. Check the actual preset count, models, reasoning levels and order in Codex, then close Slider manually. Old 0.6.0 success records are ignored.

**Check compatibility** rechecks installation eligibility and published signed data; it does not start Codex or certify the actual slider effect. Confirmed interface/schema mismatches can ask for a new adapter. Loading, absent configuration and timeouts allow retry. Independent consumer verification is still to be implemented.

After installing, open `/Applications/Codex Slider.app` and confirm **v0.6.1** in its header. To report a problem, run this read-only command; it does not start Codex or change presets:

```sh
"/Applications/Codex Slider.app/Contents/MacOS/CodexSlider" --diagnose
```

## Preview status

Unofficial; not affiliated with OpenAI. Locally signed and not Apple-notarized; a trusted download may require [Open Anyway](https://support.apple.com/en-us/102445). Codex 25241 passed local compatibility checks; live native-slider UI and inference remain unverified. Model access depends on your Codex account.

Application source remains private. This repository contains download instructions, the installer and signed compatibility data. Releases contain the app, installer and checksums; no Node runtime or developer files are bundled. Future versions use the same installation command.
