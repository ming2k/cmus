# Changelog

## v3.0.2

### Changes

- Remove PulseAudio output plugin, keep PipeWire as the native replacement
- Add PipeWire to CI build dependencies
- Update documentation to reflect PipeWire replacing PulseAudio

## v3.0.1

### New Features

- Add PipeWire output plugin for native PipeWire audio support

## v3.0.0

### New Features

- Add mpg123 input plugin for MP3/MP2 decoding
- CUE: enable adding cue files directly, handle directories with cue files
- CUE: add replaygain and genre to track info, more precise time tracking
- CUE: support multiple FILEs and non-sequential TRACK numbers
- op/mixer_alsa: add alsamixer's volume scale and mixer control like aplay

### Improvements

- ip/ffmpeg: optimize seeking, better frame skipping logic, improve readability
- ip/ffmpeg: fix building for ffmpeg 8.0
- Standardise in using xmalloc
- README: replace distro-specific dependency tables with plain dependency list

### Bug Fixes

- Fix compiler warning about uninitialized rb_parent_color
- Fix memory leak in bass.c
- Fix stringop-truncation warning
- Fix unterminated-string-initialization warnings
- Fix compilation failure
- Fix libmp4v2 check
- Fix for missing Icecast streaming bitrate display
- Fix ptr_array_unique always removing 1st element
- CUE: fix incorrect track timing calculation, fix memory leak
- CUE: remove 'associated cue' mechanism
- ip/flac: remove debug output spam
- op/alsa: remove polling for events before pause
- Make sure to not try freeing an uninitialized pointer
