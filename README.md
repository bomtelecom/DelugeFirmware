# Deluge USB Audio Firmware

Class-compliant USB audio interface capability for the Deluge. Send any track to its own channel in your DAW or other USB host, and send up to four channels back into the Deluge. No driver needed.


## Features

- 8 channels out, 4 channels in, 16-bit, 44.1 kHz, alongside USB MIDI
- Per track: send to any of 8 mono channels or 4 stereo pairs, and optionally take it out of the Deluge's own outputs
- Return to the song: one returning pair summed into the song mix, before the song's effects, with its own level
- Return to a track: an audio track can take a USB channel or pair as its input, and play and record it like a line input
- Delay compensation: holds the Deluge's own sound back 0–100 ms so a track sent through an external effect comes back in time

## Documentation

📖 See [USB Audio Feature Guide](docs/USB_AUDIO.md) for detailed controls and known limitations.


## Compatibility

Tested on a 7-segment Deluge with macOS (Ableton Live, Audacity) and Linux (Raspberry Pi). Not yet tested on OLED Deluges or Windows — reports welcome.

While connected as a USB audio device, the Deluge cannot host a USB MIDI controller. MIDI to and from the computer still works.

## Installation
⚠️ Experimental feature! Install at your own risk.

### For users (flash only)

1. **Back up your SD card** — copy the entire card to your computer first
2. Download `USB-Audio-1.0.bin` from [Releases](https://github.com/sticknobills/DelugeFirmware/releases/tag/USB-Audio-1.0)
3. Copy the `.bin` file to the root of your SD card (no subfolders), and delete any other `.bin` there
4. Insert the card into your Deluge and power off
5. Hold SHIFT while powering on
6. Wait approximately 1 minute for the flash to complete — do not interrupt or power off
7. Your songs and samples are unaffected by the flash

To revert: put an official Deluge firmware `.bin` back and repeat.

### For developers (build from source)

Clone this repository and follow the [upstream build instructions.](https://github.com/SynthstromAudible/DelugeFirmware/blob/main/docs/CONTRIBUTING.md)

```bash
git clone https://github.com/sticknobills/DelugeFirmware.git
cd DelugeFirmware
git checkout usb-audio-1.0
# Then follow upstream build steps
```


## About this fork

This repo is a downstream fork of [SynthstromAudible/DelugeFirmware](https://github.com/SynthstromAudible/DelugeFirmware). USB Audio is built on upstream `main` at bfd4a0b5 (2026-10-13), the development line for community release 1.3 Derbyshire, and is maintained on `usb-audio-1.0`.


## Bugs

This is an experimental feature in development by one person with a limited testing environment. [Please report any bugs!](https://github.com/sticknobills/DelugeFirmware/issues/new/choose)


## License

GPL-3.0 (from Deluge community firmware)
