# bandcamp-dl

[![PyPi Version](https://img.shields.io/pypi/v/bandcamp-dl.svg)](https://pypi.python.org/pypi/bandcamp-dl)
[![PyPI Status](https://img.shields.io/pypi/status/ruff)](https://pypi.python.org/pypi/bandcamp-dl)
[![Python Versions](https://img.shields.io/pypi/pyversions/bandcamp-dl.svg)](https://pypi.python.org/pypi/bandcamp-dl)
[![Last Commit](https://img.shields.io/github/last-commit/ReK42/bandcamp-dl/main?logo=github)](https://github.com/ReK42/bandcamp-dl/commits/main)
[![Build Status](https://img.shields.io/github/actions/workflow/status/ReK42/bandcamp-dl/main.yml?logo=github)](https://github.com/ReK42/bandcamp-dl/actions)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/charliermarsh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)
[![Black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![License](https://img.shields.io/github/license/ReK42/bandcamp-dl)](https://github.com/ReK42/bandcamp-dl/blob/main/LICENSE)

Download your collection from Bandcamp.

## Installation
```sh
pipx install bandcamp-dl
```

## Usage
```
usage: bandcamp_dl [-b BROWSER]
                   [-c FILE]
                   [-d DIR]
                   [-f FORMAT]
                   [-t INT]
                   [-p FLOAT]
                   [-m INT]
                   [-r FLOAT]
                   [--filename-format FORMAT]
                   [--force]
                   [-v]
                   [--debug]
                   [-h]
                   [--version]
                   USERNAME

Download your collection from Bandcamp.

To use, login to Bandcamp using one of the supported browsers. All albums in your
collection will be downloaded to the output directory, with subfolders, based on the
filename format selected.

Arguments:
  USERNAME              Bandcamp username

Options:
  -b,--browser          Browser used to login to Bandcamp, default: firefox
                        Supported browsers: brave, chrome, chromium, edge, firefox, opera
  -c,--cookie-path      Path to cookies.txt, if no browser was used
  -d,--directory        Directory to download to, default: .
  -f,--file-format      File format to download, default: mp3-v0
                        Supported formats: aac-hi, aiff-lossless, alac, flac, mp3-320, mp3-v0, vorbis, wav
  -t,--threads          Number of download threads to spawn, default: 4
  -p,--pause            Pause between successful downloads, default: 1.0
  -m,--max-retries      Maximum number of failed download attempts, default: 5
  -r,--retry-wait       Pause between retries, default: 5.0
  --filename-format     Filename format to use, default: $artist/$artist - $title
                        Supported variables: $artist, $title
  --force               Re-download and overwrite existing albums
  -v, --verbose         Show verbose information
  --debug               Show debug information
  -h, --help            Show this help message and exit
  --version             Show version information and exit
```

## Development Environment
```sh
git clone https://github.com/ReK42/bandcamp-dl.git
cd bandcamp-dl
pip install -e .[tests]
```
