# cmus — C\* Music Player

https://cmus.github.io/

[![Build Status](https://github.com/cmus/cmus/actions/workflows/build.yml/badge.svg)](https://github.com/cmus/cmus/actions/workflows/build.yml)

Copyright © 2004-2008 Timo Hirvonen <tihirvon@gmail.com>

Copyright © 2008-2017 Various Authors


## Configuration

    $ ./configure

By default, features are auto-detected. To list all configuration options, run
`./configure --help`. Some common autoconf-style options like `--prefix` are
also available.

After running configure you can see from the generated `config.mk` file
what features have been configured in (see the `CONFIG_*` options).

**Required:** pkg-config, ncurses (wide character support recommended), iconv, C compiler, git, GNU Make

**Optional input plugins:**

- FLAC — libflac
- MAD — libmad
- mpg123 — libmpg123
- Ogg/Vorbis — libvorbis, libogg
- Opus — opusfile
- FFmpeg — libavformat, libavcodec, libswresample, libavutil
- FAAD2 — libfaad (AAC)
- MP4 — libmp4v2, libfaad
- Musepack — libmpcdec
- WavPack — libwavpack
- libmodplug
- libmikmod
- BASS — libbass
- libcdio (CDDA)
- libayemu (VTX)

**Optional output plugins:**

- ALSA — libasound
- PulseAudio — libpulse
- JACK — libjack (optionally libsamplerate)
- sndio — libsndio
- OSS
- CoreAudio (macOS)
- libao
- aRts — libartsc
- AAudio (Android)

**Optional features:**

- MPRIS — libsystemd / libelogind / basu
- CDDB — libcddb
- libdiscid


## Building

    $ make

Or on some BSD systems you need to explicitly use GNU make:

    $ gmake


## Installation

    $ make install

Or to install to a temporary directory:

    $ make install DESTDIR=~/tmp/cmus

This is useful when creating binary packages.

Remember to replace `make` with `gmake` if needed.


## Manuals

    $ man cmus-tutorial

And

    $ man cmus


## IRC Channel

Feel free to join IRC channel #cmus on Libera.chat and share you experience,
problems and issues. Note: This is an unofficial channel and all people hanging
around there are for the love of cmus.


## Reporting Bugs

Bugs should be reported using the GitHub [issue
tracker](https://github.com/cmus/cmus/issues). When creating a new issue, a
template will be shown containing instructions on how to collect the necessary
information.

Additional debug information can be found in `~/cmus-debug.txt` if you
configured cmus with maximum debug level (`./configure DEBUG=2`). In case of a
crash the last lines may be helpful.


## Git Repository

https://github.com/cmus/cmus

    $ git clone https://github.com/cmus/cmus.git


## Hacking

cmus uses the [Linux kernel coding
style](https://www.kernel.org/doc/html/latest/process/coding-style.html). Use
hard tabs. Tabs are _always_ 8 characters wide. Keep the style consistent with
rest of the code.

Bug fixes and implementations of new features should be suggested as a
[pull request](https://github.com/cmus/cmus/pulls) directly on GitHub.

