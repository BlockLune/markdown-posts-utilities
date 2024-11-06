# Markdown Posts Utilities

I use markdown to write my blog posts, and here are some of the scripts I've used to migrate my blogs, etc.

## `img-downloader.py`

This script download images in Markdown files and update the links.

## Reference

- [mufidu/download_imgs.py](https://gist.github.com/mufidu/f7b795f844f1ee4dc78e55123d5a398b)

### Usage

```text
usage: python img-downloader.py [-h] [--only-basename-link] [-o OUTPUT_DIR] dir [dir ...]

Download images in Markdown files and update links

positional arguments:
  dir                   directory of markdown files

options:
  -h, --help            show this help message and exit
  --only-basename-link  by default, link will be updated to `OUTPUT_DIR/IMG_NAME`. If this flag is set, link will be updated to
                        `IMG_NAME` only
  -o OUTPUT_DIR, --output-dir OUTPUT_DIR
                        directory to save images
```

- If you don't specify the `OUTPUT_DIR`, the script will create a dir based on the name of the markdown file.
- If you want to use this script to update all the image links in your [Hexo](https://hexo.io) posts, run:

```bash
python MdImgDownloader /path-to-your-hexo-project/source/_posts --only-basename-link
```

## `s3-uploader.py`

This script uploads images to a s3-compatible service, written in the help of `gpt-4o`.

## `tagenerator.py`

This script uses the power of LLMs to generate tags for blog posts.
