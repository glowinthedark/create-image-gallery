# create-image-gallery

Python script for creating a static HTML image gallery. 

Uses `imagemagic` for thumbnail generation and Python Pillow for EXIF data extraction.

## Requirements

- python 3.12 (required for `pathlib.Path.relative_to(.., walk_up=True)`)
- optional: imagemagick — `apt install imagemagick`
- optional: Pillow — `pip3 install pillow`
- optional: Pillow HEIF - `pip3 install pillow-heif`

```bash
imggal.py -h
usage: imggal9.py [-h] [--output-file output_file] [--videos] [--video-preload] [--thumbs-dir THUMBS_DIR] [--no-thumbnails]
                  [--ignored [ignore ...]] [--num-workers NUM_WORKERS] [--verbose]
                  [gallery_root]

Music gallery Generator

positional arguments:
  gallery_root          Gallery root, by default current folder

options:
  -h, --help            show this help message and exit
  --output-file output_file, -o output_file
                        Output filename
  --videos, -m          Include videos. !!!WARNING: increases page load time!
  --video-preload       Preload 1st frame for videos. !!!WARNING: increases page load time!
  --thumbs-dir THUMBS_DIR, -t THUMBS_DIR
                        Thumnails folder, by default ~/.thumbs
  --no-thumbnails       Use full size image and DO NOT generate image thumbnails using imagemagick
  --ignored [ignore ...], -i [ignore ...]
                        Custom ignored path segments. Accepts multiple segments, e.g. -i junk1 junk2 junk3 "[]"
  --num-workers NUM_WORKERS, -n NUM_WORKERS
                        Maximum number of parallel threads for thumbnail generation, DEFAULT: 16
  --verbose, -v         Verbose output
```
