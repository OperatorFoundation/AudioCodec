# AudioCodec

> **Maintained Fork** — This is an actively maintained fork of
> [FrankBoesing/Arduino-Teensy-Codec-lib](https://github.com/FrankBoesing/Arduino-Teensy-Codec-lib)
> by [Operator Foundation](https://codeberg.org/OperatorFoundation).
> Full credit to Frank Boesing for the original work.

Software MP3, AAC, and FLAC audio codec plugin for the Teensy Audio Library.

---

## Features

- Decodes **MP3** (up to 320 kbps), **AAC** (MP4, M4A, raw), and **FLAC** (4–24 bit) entirely in software
- Requires as little as **48 MHz** — no dedicated codec hardware needed
- Optimized for **ARM Thumb2** architecture
- Reads audio from **SD card**, **built-in Flash**, or **serial Flash** (with Teensy Audio Shield)

## Requirements

- Teensy 3.x or later
- [Teensy Audio Library](https://github.com/PaulStoffregen/Audio)

## Installation

### PlatformIO

Add to your `platformio.ini`:

```ini
lib_deps =
    https://codeberg.org/OperatorFoundation/AudioCodec
```

Pin to a specific release for reproducible builds:

```ini
lib_deps =
    https://codeberg.org/OperatorFoundation/AudioCodec#v1.0.0
```

### Arduino IDE (manual)

1. Go to the [repository](https://codeberg.org/OperatorFoundation/AudioCodec) and download the ZIP (use the **Download repository** button)
2. In the Arduino IDE, go to **Sketch → Include Library → Add .ZIP Library**
3. Select the downloaded ZIP

## Usage

See the `examples/` directory for working sketches. This library integrates as a plugin to the Teensy Audio Library — include it alongside your existing audio graph setup.

## Known Limitations

- **AAC-HE (SBR)** is not supported — insufficient RAM on Teensy 3.x hardware
- **FLAC block size** is limited to 128–1024 bytes on Teensy 3.2 and earlier
- **ID3, APE, and MP4 tag parsing** is not yet implemented

## License

The original library was authored by Frank Boesing and was published without a license file. This fork is maintained by Operator Foundation. In the absence of an explicit license, use of this library may be subject to the original author's copyright.

We have requested that the original author add an open source license to clarify terms. If you are Frank Boesing or another rights holder and wish to address licensing, please [open an issue](https://codeberg.org/OperatorFoundation/AudioCodec/issues).

## Contributing

Issues and pull requests are welcome on [Codeberg](https://codeberg.org/OperatorFoundation/AudioCodec). Please open an issue before submitting significant changes.
