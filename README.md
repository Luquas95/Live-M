# Live-M

Lightweight CLI system monitor — lightweight replacement for htop + psensors.

[![Platform](https://img.shields.io/badge/platform-Linux-blue)](https://linux.org)
[![Python](https://img.shields.io/badge/language-python_3.8+-green)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/license-MIT-lightgrey)](https://opensource.org/license/MIT)
[![Stars](https://img.shields.io/github/stars/Luquas95/Live-M?style=social)](https://github.com/Luquas95/Live-M)

## What it shows

- **CPU** — per-core usage bars with color coding + load average
- **RAM & SWAP** — usage bars with GiB values
- **Disks** — usage bars for all real mountpoints
- **Temperatures** — CPU, PCH, Wi-Fi chip and others as bars
- **Wi-Fi** — live download/upload speed in the header

All panels update live. No process list — that's why it's lighter than htop.

## Requirements

- Linux (Debian / Ubuntu / Mint)
- Python 3.8+
- python3-psutil

## Installation

```bash
sudo dpkg -i livem_2.0.deb
```

## Usage

```bash
livem
```

| Key | Action |
|-----|--------|
| `q` / `Ctrl+C` | Quit |
| `+` | Increase refresh interval |
| `-` | Decrease refresh interval |

Optional flags:

```bash
livem --interval 2    # refresh every 2 seconds
livem --no-color      # disable colors
livem --version
livem --help
```

## Why not htop?

htop iterates over all processes in `/proc/[pid]/` on every refresh. Live-M skips processes entirely — CPU usage stays under 0.5%.
