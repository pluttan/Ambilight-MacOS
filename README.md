<div align="center">

# Ambilight macOS

**Software-driven ambient backlight for macOS via Arduino**


</div>

A Python script that captures screen edge colors on macOS and drives an RGB 5050 LED strip connected to an Arduino UNO. Configurable LED count per side, pixel sampling density, and Retina display support.

## ■ Features

- ❖ **Real-time screen capture** — samples edge pixels to drive ambient LEDs
- ❖ **Configurable layout** — set LED count per side (top, right, bottom, left) and offsets
- ❖ **Retina support** — pixel density multiplier for HiDPI displays
- ❖ **Auto-detection** — finds Arduino serial port automatically (`/dev/cu.usbserial*`)

## ■ Stack

<div align="center">

| Component | Technology |
|-----------|------------|
| Software | Python 2.7 |
| Screen capture | PyObjC (Quartz CoreGraphics, AppKit) |
| Hardware | Arduino UNO, RGB 5050 LED strip |
| Communication | Serial 115200 baud (pySerial) |

</div>

## ■ How It Works

```
1. Python reads LED layout from config.py (count per side, offsets, Retina multiplier).
2. PyObjC/Quartz captures the screen edges in real time.
3. Edge pixels are sampled and mapped to individual LED positions.
4. Color data is sent to the Arduino over a serial connection at 115200 baud.
5. Arduino firmware drives the RGB 5050 LED strip with the received colors.
```

## ■ Usage

```bash
# Edit config.py with your LED layout
python ambilight.py
```

Requires the [Arduino firmware](https://github.com/sergeich5/Ambilight-Arduino-part) flashed to an Arduino UNO.

## ■ License

MIT © [pluttan](https://github.com/pluttan)
