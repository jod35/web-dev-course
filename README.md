# Web Development at MHSM

Course notes and exercises for the web development program at Makerere High School Migadde. The site covers HTML and CSS, with a JavaScript track still to be written.

## Local development

The site is built with [Zensical](https://zensical.org/). The project uses `uv`:

```bash
uv sync
uv run zensical serve
```

Open the local address printed by the command. To build the static site:

```bash
uv run zensical build --clean
```

The output is written to `site/`.

## Content

- `docs/index.md` is the home page.
- `docs/00-index.md` is the HTML course index.
- `docs/css/index.md` is the CSS course index.
- `zensical.toml` controls navigation, theme features, and Markdown extensions.
- `docs/stylesheets/extra.css` contains a few small readability fixes. The rest of the design comes from the Zensical theme.

## Editing

Keep one `<h1>` per page, use heading levels to show structure rather than size, and include a short practice task where it helps. Code examples should be complete enough for a student to type and run.
