# viodf
A shell script to comfortably edit XML content of Open Document Format (ODF) files (.odt, .odp, .ods etc.).

Unpacks the ODF file, lets user select file(s) to edit, shows changes and re-packs the ODF file.

Also works with Microsoft Office XML-based formats (.docx, .xlsx, .pptx etc.).

## Requirements
- [zip(1)](https://linux.die.net/man/1/zip) and [unzip(1)](https://linux.die.net/man/1/unzip) - as ODF files are ZIP files
- [dialog(1)](https://linux.die.net/man/1/dialog) - for choosing files
- [mktemp(1)](https://linux.die.net/man/1/mktemp) - to create a temporary directory
- [find(1)](https://linux.die.net/man/1/find) - to find changed files
- [git(1)](https://linux.die.net/man/1/git) or [diff(1)](https://linux.die.net/man/1/diff) - to highlight changes
- any editor - script check for `$EDITOR`, /usr/bin/editor, vim, vi or nano

### Optional
- [xmllint(1)](https://linux.die.net/man/1/xmllint) - formats XML files for being easier to navigate

### Debian-based Linux

Install dependencies with:

```
$ sudo apt-get install libxml2-utils dialog git zip unzip findutils coreutils
```

### mac OS

Required tools ship with mac OS, except for dialog(1). git(1) is part of Xcode command line tools.

Install dialog(1) with [Homebrew](https://brew.sh/), for example:

```
$ brew install dialog
```

