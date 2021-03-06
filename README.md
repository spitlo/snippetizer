# Snippetizer

Snippetizer uses `ffmpeg` and `ffprobe` to create snippets from audio files.

Snippets default to a 30 second bit from the middle of the song, and are faded in and out.

## Installation

- Copy the `snippetizer` file to  `~/bin`; or
- Clone the repo and create a symlink to `snippetizer` in `~/bin`

## Usage

```bash
snippetizer audio_file.wav
```

## Arguments

```text
[start|middle|end]    What part of the file you want to snippet.
                      Defaults to 'middle'.
[<any integer>]       Snippet length in seconds.
                      Defaults to '30'.
[-o/--ogg]            Use ogg as output format instead of mp3.
[-n/--nofade]         Don’t fade in and out.
```

## Batching example

Create 30 second snippets of all flac and wav files in current directory:

```bash
find . -maxdepth 1 \( -iname '*.wav' -o -iname '*.flac' \) -execdir snippetizer {} \;
```

## Todo

- [x] Add argument for using ogg instead of mp3 as output format
