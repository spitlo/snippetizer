# Snippetizer

Snippetizer uses `ffmpeg` and `ffprobe` to create snippets from audio files.

Snippets default to 30 seconds, and are faded in and out.

## Usage

```bash
snippetizer audio_file.wav
```

## Arguments

```text
  [start|middle|end]    What part of the file you want to snippet.
                        Defaults to 'middle'.
  [<any integer>]       Snippet length in seconds.
  [-n/--nofade]         Don’t fade in and out.
```
