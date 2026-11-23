<p align="center">
  <img src="https://i.postimg.cc/x11zwRtn/banner.png" alt="SoundDeck Mic Soundboard — Hotkey Soundboard for Discord, OBS & Voice Chat" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D6?style=flat-square&logo=windows" alt="Platform: Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Mode-Discord%20%26%20OBS%20Soundboard-2EA44F?style=flat-square" alt="Mode">
  <img src="https://img.shields.io/badge/Release-sounddeck--v1.1-5391FE?style=flat-square" alt="Release Tag">
  <img src="https://img.shields.io/badge/License-MIT-8B5CF6?style=flat-square" alt="License: MIT">
</p>

# SoundDeck Mic Soundboard — Hotkey Soundboard for Discord, OBS & Voice Chat

**Want a fast, ad-free desktop soundboard for Discord, OBS streams, or tabletop/co-op sessions without monthly subscriptions or bloated overlays? Load your local .MP3, .WAV, or .OGG clips, bind hotkeys, and route audio to your headset and virtual mic.**

SoundDeck Mic Soundboard provides dual-output audio playback on Windows: **routing sound clips simultaneously to a Virtual Audio Cable (such as VB-Cable) for Discord/in-game mic input and to your headphones for local monitoring, with independent volume sliders and global hotkeys**.

This project is aimed at **Windows 10 and Windows 11 (64-bit) gamers, Discord users, and streamers** who want a simple local soundboard using their own audio files.

## Quick Use-Case & Troubleshooting Reference

| Scenario / Issue | Cause | Solution |
| --- | --- | --- |
| Discord Nitro soundboard limits custom slots & file sizes | Built-in Discord soundboard restricts free users and shortens clips | Play unlimited local `.mp3`, `.wav`, and `.ogg` files of any length |
| Cannot hear the soundboard clip yourself while teammates hear it | Single-output players send audio only to the virtual cable | Use Dual Output: `Primary (VB-Cable)` + `Monitor (Your Headset)` |
| Clip keeps playing too long during a tense match | No global stop button when a long audio track triggers | Press the global **Stop All** hotkey (`Ctrl+Alt+S`) to silence immediately |
| Heavy Electron soundboards eat 400+ MB RAM in background | Web-wrapped audio apps waste memory while gaming | Run a lightweight native Windows audio engine (< 25 MB RAM) |

## Download for Windows

[**Download SoundDeck.zip — Latest GitHub Release (Windows x64)**](../../releases/latest/download/SoundDeck.zip)  
[View All Releases & Changelog](../../releases) · [Report an Issue](../../issues)

### Why use `SoundDeck.exe`? (Key features)

- Plays `.mp3`, `.wav`, `.ogg`, and `.flac` clips with instant zero-latency hotkey triggers.
- Supports Dual Audio Output: routes simultaneously to a Virtual Cable (Discord/OBS) and your headphones.
- Independent volume sliders and per-clip gain normalization so loud clips never clip voice chat.
- Includes a global **Stop All** hotkey and customizable grid profiles.

### Sample Output

```text
[SoundDeck] Loaded Profile: Co-op_Gaming (16 sound clips | Stop Hotkey: Ctrl+Alt+S)
[OK]   Primary Output   : CABLE Input (VB-Audio Virtual Cable) [Vol: 80%]
[OK]   Monitor Output   : HyperX Cloud III Headset [Vol: 65%]
[INFO] Memory Footprint : 21.4 MB RAM (Idle)
```

The release ZIP is named `SoundDeck.zip`; the Windows executable inside is named `SoundDeck.exe`.

1. Close SoundDeck before updating or replacing executable files.
2. Click **Download SoundDeck.zip** above.
3. Right-click the downloaded archive and choose **Extract All**.
4. Open the extracted folder and run `SoundDeck.exe`.
5. Review the options and output paths before processing files.

**Requirements:** Windows 10 or 11 (64-bit); optional VB-Audio Virtual Cable for routing clips into Discord/in-game voice chat.

### Verification & Windows SmartScreen Note

- **Offline & standard user permissions:** `SoundDeck.exe` runs locally without uploading your files and does not require disabling Windows Defender.
- **Windows SmartScreen:** Because this is an independent open-source utility without a commercial EV code-signing certificate, Windows SmartScreen may show *"Windows protected your PC"* on first launch. Click **More info → Run anyway** after verifying the release checksum on the [Releases](../../releases) page.

## Problems this project solves

### Unlimited local sound slots with zero subscriptions

Organize hundreds of `.mp3` and `.wav` clips across tabs without upload quotas.

### Clean dual-device audio routing

Hear every triggered sound in your own headset while sending clean audio into OBS or Discord via VB-Cable.

### Per-clip volume balancing

Prevent sudden ear-splitting volume spikes by setting individual clip gain levels.

### 100% local files

Your audio library stays on your drive.

## Default folders and configuration paths

SoundDeck saves soundboard profiles and hotkey mappings in `%APPDATA%\SoundDeck`:

```text
%APPDATA%\SoundDeck\profiles.json
```

Typical directory layout:

```text
SoundDeck Audio Routing:
├── Clip Trigger (Hotkey / Click)
│   ├──► Primary Output : CABLE Input (Discord / OBS Mic)
│   └──► Monitor Output : Headphones (Local Preview)
└── Global Stop Hotkey  : Ctrl + Alt + S
```

To send soundboard clips through your microphone in Discord, install free **VB-Audio Virtual Cable** and route your mic + SoundDeck through it (or select `CABLE Output` in OBS).

## Quick start guide

Follow these steps to get started:

1. **Extract `SoundDeck.zip` to a local folder and launch `SoundDeck.exe`.** No installer or account login required.
2. **Select your **Monitor Output** (Headset) and **Primary Output** (VB-Cable / Speakers).** Adjust master volume sliders.
3. **Drag `.mp3`, `.wav`, or `.ogg` files onto any soundboard button.** Right-click a button to assign a global hotkey and clip volume.
4. **Test triggering a sound and stopping it with `Ctrl+Alt+S`.** Verify audio levels in Discord or OBS.

### Data safety note

SoundDeck plays local audio files in read-only mode without altering Windows audio drivers.

## What the status summary shows

SoundDeck displays **loaded clip count, Primary and Monitor output endpoints, active hotkeys, and memory usage**.

## FAQ

**How do I make my friends in Discord hear SoundDeck?**

Install the free VB-Audio Virtual Cable driver, set SoundDeck's Primary Output to `CABLE Input`, and select `CABLE Output` as your input device (or mix with your mic in Windows Listen/VoiceMeeter).

**What audio formats does SoundDeck support?**

MP3, WAV, OGG, and FLAC.

**Does it require an internet connection or account?**

No. SoundDeck works 100% offline with your local audio files.

## Useful reading

- [VB-Audio Virtual Cable Official Page](https://vb-audio.com/Cable/)

## More Windows Desktop Utilities

- [AudioSwitch-HotkeyToggle](../AudioSwitch-HotkeyToggle) — One-key headphones, speakers & microphone switcher
- [PadDrift-ControllerPollingTest](../PadDrift-ControllerPollingTest) — Gamepad stick drift & mouse polling rate (1000-8000 Hz) tester
- [PinTop-WindowAlwaysOnTop](../PinTop-WindowAlwaysOnTop) — Pin any window Always-on-Top & adjust transparency on Windows
- [ClipVault-OfflineClipboardHistory](../ClipVault-OfflineClipboardHistory) — Offline Windows clipboard history & plain-text snippet manager

*Independent open-source desktop utility for Windows. Not affiliated with Discord Inc. or OBS Project.*
