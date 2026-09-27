# ifs_lab

A learning project for Claude Code. It holds two things:

- A small Rust command-line program that prints "Hello World".
- **IFS Lab** (`web/fern.html`), a browser page for drawing and designing fractals. [Try it live](https://harveyrook.github.io/ifs_lab/web/fern.html).

## Rust program

```sh
cargo run
```

Other commands: `cargo build`, `cargo test`, `cargo fmt`, `cargo clippy`.

## IFS Lab

**Live page:** https://harveyrook.github.io/ifs_lab/web/fern.html

To use it offline, open `web/fern.html` in a web browser. It's a single self-contained file with no build step.

The page draws fractals made by an iterated function system (IFS): a small set of affine maps

```
x' = a·x + b·y + e
y' = c·x + d·y + f
```

each picked at random with probability `p`. Repeating this many times (the "chaos game") traces out the shape that is made of shrunken copies of itself, such as the Barnsley fern.

Features:

- Presets: Blank, Barnsley fern, Cyclosorus, Fishbone and the Sierpinski triangle.
- A dashed frame stands for the whole image. Each map is drawn as a box showing where it sends that frame.
- **Add map** creates a new box. Drag any of its three corner handles to move, scale, rotate, skew or flip it.
- The frame stays fixed while you edit. **Fit view** resizes it to the current drawing.
- A fast low-detail preview while dragging, then a full render when you let go.
- Probabilities are set from each box's area, so new maps always show up.
- Maps that don't shrink are blocked while dragging and shown in red if typed in.
- Every coefficient can also be edited in the table.
