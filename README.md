# bandcamp-dl
Download your collection from Bandcamp.

## Installation
```sh
pipx install git+https://github.com/ReK42/bandcamp-dl.git
```

## Usage
```sh
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
#### Windows
```Powershell
git clone https://github.com/ReK42/bandcamp-dl.git
cd .\bandcamp-dl
python -m venv .env
.\.env\Scripts\Activate.ps1
pip install -e .[tests]
```

#### Linux
```bash
git clone https://github.com/ReK42/bandcamp-dl.git
cd bandcamp-dl
python -m venv .env
source .env/bin/activate
pip install -e .[tests]
```
