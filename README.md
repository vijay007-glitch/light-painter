# Light Painter

Paint a photomask on a 64 × 64 grid and watch the resist contour print through a partially coherent EUV or ArF imaging model. Six puzzles in optical proximity correction, plus a sandbox with a Bossung plot and depth-of-focus readout.

- Live: https://vijay007-glitch.github.io/light-painter/
- Write-up: https://vijay007-glitch.github.io/posts/light-painter/

## Run it

It is one self-contained page, so open `index.html` in a browser. Or serve the folder:

```
python -m http.server 8000
```

The page loads web fonts from Google Fonts, so it needs a network connection for the intended typefaces.

## Develop

The page is built from `src/` by `build.py`. `dist/` is git-ignored.

```
node tests/core.test.js
python build.py
python tests/browser_test.py
copy dist\index.html index.html
```

`tests/browser_test.py` needs `pip install playwright` and `python -m playwright install chromium`.
