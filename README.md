# Codex Slider downloads

Customize Codex’s Default Slider with 3–7 model and reasoning presets.

**[Download 0.6.3](https://github.com/jiediking/codex-slider-downloads/releases/tag/v0.6.3)** · [DMG](https://github.com/jiediking/codex-slider-downloads/releases/download/v0.6.3/Codex-Slider-0.6.3-macOS-arm64.dmg) · [Checksums](https://github.com/jiediking/codex-slider-downloads/releases/download/v0.6.3/SHA256SUMS.txt)

## Requirements

- Apple Silicon Mac, macOS 15 or later.
- Codex desktop installed and signed in with ChatGPT.
- Native arm64 Node.js 22.x (22.22.3+), 24.x or 26.x. [Get Node.js 22](https://nodejs.org/en/download/archive/v22.23.3).

## Install or update

Quit every copy of Codex Slider, then copy this line into Terminal:

```sh
/bin/bash -o pipefail -c '/usr/bin/curl -fsSL https://raw.githubusercontent.com/jiediking/codex-slider-downloads/main/install.sh | /bin/bash'
```

No GitHub account or GitHub CLI is needed. The installer verifies the package, signature and Node before installing to `/Applications/Codex Slider.app`. Presets are kept. macOS asks if administrator permission is needed. Alternatively, open the DMG and drag Slider to Applications. Open Slider and confirm **v0.6.3** in its header.

## Use

1. Open Slider and choose 3–7 unique model/reasoning pairs. Drag to reorder.
2. Choose **Save & launch Codex** and read the local debugging explanation on first use. If Codex is running, save your work and quit it normally when prompted.
3. Open Codex’s **Default slider menu**. Slider independently checks the rendered stops and current selection. **Your slider is ready** confirms a match. Slider shows it briefly and exits automatically; Codex keeps running with the applied presets.
4. Pending or failed checks keep the window open. Editing during the success notice cancels automatic exit. A close error keeps the editor available for manual retry. Launch through Slider for custom presets; Codex’s regular icon uses its standard slider.

## Compatibility

Codex updates do not normally need a new entry in the [signed list](https://raw.githubusercontent.com/jiediking/codex-slider-downloads/main/compatibility-feed.json). For an unlisted official installation, Slider tries its existing adapter and independently compares the actual rendered slider with your presets.

**Slider effect not confirmed** means there is not enough evidence yet. Keep the Default menu open and use **Check now**. Loading, unavailable models, a closed menu or missing observation evidence stays unconfirmed. A confirmed configuration mismatch or a stable, fully available slider that differs from the presets asks for an adapter update.

**Check compatibility** rechecks the installation and signed data and retries a pending check in Slider’s current launch session. A saved result is historical; every new custom launch checks again. Read-back alone and old 0.6.0 success records cannot certify the slider.

## Check automatic exit

Launch Codex through Slider, then open the Default slider menu. A fresh independent confirmation shows **Your slider is ready** and closes Slider after about one second. Codex should stay running and retain the applied presets. An old success record or configuration read-back alone cannot trigger exit.

If the slider is still unconfirmed, incompatible or loading, the window stays open. **Edit presets** cancels the pending exit; a close error shows a message and permits a manual retry. This release changes the completion flow and does not add a Codex build to the signed list.

For a read-only installation report, run:

```sh
"/Applications/Codex Slider.app/Contents/MacOS/CodexSlider" --diagnose
```

This static report does not start Codex. Its `consumerVerified: false` is not a live-session verdict. The actual launch record is `~/Library/Application Support/Codex Slider/last-launch.json`; 0.6.3 records `consumer-verified` only after independent evidence matches.

## Preview status

Unofficial; not affiliated with OpenAI. Locally signed and not Apple-notarized; a trusted download may require [Open Anyway](https://support.apple.com/en-us/102445). Model access depends on your Codex account. Non-interrupting and isolated native-host checks passed. Controlled fixture results are distinct from a direct live Codex session test.

Application source remains private. This repository contains download instructions, the installer and signed compatibility data. Releases contain the app, installer and checksums; no Node runtime or developer files are bundled. Future versions use the same installation command.
