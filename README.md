# Convert PDF files to PNG files, one per page

I created this since this implementation with Rust is about 2x times faster than what I used previously: https://github.com/Dima-369/pdf2png-mac

On an M1 Macbook, this takes about 700 ms to convert a 5 MB PDF file with 12 pages - just a number, depends on PDF and hardware spec. Tested on macOS 14.0.

Download the `libpdfium.dylib` file from https://github.com/bblanchon/pdfium-binaries and add it next to the compiled `pdf2png` binary or specify `--library-directory`.

# Compile

```bash
cargo build --release
```

Then the executable will be under `target/release/pdf2png`.

# Notes

- converting to PNGs is faster than JPEGs, so PNGs are used
