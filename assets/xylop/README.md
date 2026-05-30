# xylop — Flash, revived

The original `xylop.swf` (Macromedia Flash 4, a 6-key sound toy) running on the modern web
via **[Ruffle](https://ruffle.rs)**, an open-source Flash Player emulator compiled to
WebAssembly. No plugin, no Adobe, nothing phoning home — all files here are yours to host.

## Contents

```
xylop/
├── index.html          the player page
├── xylop.swf           the original movie (unchanged)
├── ruffle/             Ruffle 0.2.0 self-hosted runtime (MIT / Apache-2.0)
├── sounds/             the 12 note samples, carved out as .mp3 (11025 Hz mono)
└── images/             the 6 hand-drawn key faces, recovered as .png
```

## Running it

Ruffle loads its `.wasm` by `fetch`, which browsers block over `file://`. So **serve it**,
don't double-click it. From inside this folder:

```
python3 -m http.server 8000
```

then open <http://localhost:8000/>. (Firefox is more lenient with `file://` if you must.)

## Putting it on displacementactivities.org (Jekyll)

Drop the whole `xylop/` folder somewhere in the repo (e.g. `assets/xylop/`) and either
link to `assets/xylop/index.html`, or embed it in a page with an iframe:

```html
<iframe src="/assets/xylop/" width="475" height="210"
        style="border:0;background:#000" title="xylop"></iframe>
```

GitHub Pages serves `.wasm` with the correct MIME type automatically, so no server config
is needed. If you ever self-host on a server that doesn't, add `application/wasm` for `.wasm`.

## Notes

- The `sounds/` and `images/` folders aren't needed to *run* the piece — Ruffle reads
  everything from `xylop.swf` directly. They're extracted for your own use (raw material,
  or a future plugin-free rebuild in Web Audio + SVG/PNG, if you ever want to drop the
  emulator entirely).
- To update Ruffle later: `npm pack @ruffle-rs/ruffle`, unpack, and replace the `ruffle/`
  contents (the `.wasm` filenames are content-hashed and referenced from `ruffle.js`, so
  swap the whole folder as a set).
