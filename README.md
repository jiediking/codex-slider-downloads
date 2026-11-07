# Codex Slider downloads

Customize Codex’s Default Slider with 3–7 model and reasoning presets.

**[Download 0.6.2](https://github.com/jiediking/codex-slider-downloads/releases/tag/v0.6.2)** · [DMG](https://github.com/jiediking/codex-slider-downloads/releases/download/v0.6.2/Codex-Slider-0.6.2-macOS-arm64.dmg) · [Checksums](https://github.com/jiediking/codex-slider-downloads/releases/download/v0.6.2/SHA256SUMS.txt)

## Requirements

- Apple Silicon Mac, macOS 15 or later.
- Codex desktop installed and signed in with ChatGPT.
- Native arm64 Node.js 22.x (22.22.3+), 24.x or 26.x. [Get Node.js 22](https://nodejs.org/en/download/archive/v22.23.3).

## Install or update

Quit every copy of Codex Slider, then copy this line into Terminal:

```sh
/bin/bash -o pipefail -c '/usr/bin/curl -fsSL https://raw.githubusercontent.com/jiediking/codex-slider-downloads/main/install.sh | /bin/bash'
```

No GitHub account or GitHub CLI is needed. The installer verifies the package, signature and Node before installing to `/Applications/Codex Slider.app`. Presets are kept. macOS asks if administrator permission is needed. Alternatively, open the DMG and drag Slider to Applications. Open Slider and confirm **v0.6.2** in its header.

## Use

1. Open Slider and choose 3–7 unique model/reasoning pairs. Drag to reorder.
2. Choose **Save & launch Codex** and read the local debugging explanation on first use. If Codex is running, save your work and quit it normally when prompted.
3. Open Codex’s **Default slider menu**. Slider independently checks the rendered stops and current selection. **Your slider is ready** confirms a match.
4. Close Slider when finished. Launch through Slider for custom presets; Codex’s regular icon uses its standard slider.

## Compatibility

Codex updates do not normally need a new entry in the [signed list](https://raw.githubusercontent.com/jiediking/codex-slider-downloads/main/compatibility-feed.json). For an unlisted official installation, Slider tries its existing adapter and independently compares the actual rendered slider with your presets.

**Slider effect not confirmed** means there is not enough evidence yet. Keep the Default menu open and use **Check now**. Loading, unavailable models, a closed menu or missing observation evidence stays unconfirmed. A confirmed configuration mismatch or a stable, fully available slider that differs from the presets asks for an adapter update.

**Check compatibility** rechecks the installation and signed data and retries a pending check in Slider’s current launch session. A saved result is historical; every new custom launch checks again. Read-back alone and old 0.6.0 success records cannot certify the slider.

## Testing a Codex upgrade locally

Keep your installed 0.6.0 until its test is complete; you may download the 0.6.2 DMG without installing it. After updating Codex, launch through 0.6.0 and check the actual count, models, reasoning levels, order and first/middle/last choices. Its success message alone is insufficient because 0.6.0 could misreport read-back as full success.

Then quit Codex and Slider, install 0.6.2 with the command above, and repeat on the same new Codex with the same presets. Check both the real slider and **Your slider is ready**. Test 0.6.2 even if 0.6.0 worked, so the new independent verification is covered. No new target build is being added to the signed list for this comparison.

For a read-only installation report, run:

```sh
"/Applications/Codex Slider.app/Contents/MacOS/CodexSlider" --diagnose
```

This static report does not start Codex. Its `consumerVerified: false` is not a live-session verdict. The actual launch record is `~/Library/Application Support/Codex Slider/last-launch.json`; 0.6.2 records `consumer-verified` only after independent evidence matches.

## Preview status

Unofficial; not affiliated with OpenAI. Locally signed and not Apple-notarized; a trusted download may require [Open Anyway](https://support.apple.com/en-us/102445). Model access depends on your Codex account. Non-interrupting checks passed; the local real Codex upgrade comparison is pending.

Application source remains private. This repository contains download instructions, the installer and signed compatibility data. Releases contain the app, installer and checksums; no Node runtime or developer files are bundled. Future versions use the same installation command.
