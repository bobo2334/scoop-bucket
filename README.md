# My scoop bucket

## What is this

This is a bucket for [scoop](https://github.com/lukesampson/scoop).

## What is scoop

Scoop is command-line installer for Windows, just like `apt-get` or `homebrew`.

## Usage

To add this bucket to scoop, run:

```bash
scoop bucket add bobo2334 https://github.com/bobo2334/scoop-bucket.git
```

## Auto-update manifest

```bash
.\bin\checkver -a * -d .\bucket -u
```

## Parameters of checkver.ps1

- `App` (`-a APP`)
Manifest name to search.
Placeholders (*) are supported.
- `Dir` (`-d DIR`)
Where to search for manifest(s).
- `Update` (`-u`)
Update given manifest.
- `ForceUpdate` (`-f`)
Check manifest(s) and update, even if there is no new version.
- `SkipUpdated` (`-s`)
Check given manifest(s), and list only outdated manifest(s).
- `Version` (`-v VER`)
Check given manifest(s) using a given version VER.
Usually used with -u to update to a certain version.
