# Pseudo-classes

Pseudo-classes style a *state* of an element. They use single colon `:`.

## Interaction states

```css
a:hover { color: crimson; }
a:focus-visible { outline: 2px solid #333; outline-offset: 2px; }
a:active { color: #a00; }
button:disabled { opacity: 0.6; cursor: not-allowed; }
```

Always style `:focus-visible` when you style `:hover`. Keyboard users need it.

## Position in parent

```css
li:first-child { font-weight: bold; }
li:last-child { margin-bottom: 0; }
li:nth-child(2) { color: #555; }
tr:nth-child(even) { background: #f9f9f9; }
```

## Form states

```css
input:required { border-color: #888; }
input:valid { border-color: #1a7f37; }
input:invalid { border-color: crimson; }
input:checked + label { font-weight: 600; }
```

## Negation and grouping

```css
/* not the first */
li:not(:first-child) { margin-top: 0.5rem; }

/* any of these */
.card :is(h2, h3) { line-height: 1.2; }

/* where parent matches */
.card:has(img) { padding-top: 0; }
```

`:where()` is like `:is()` but with zero specificity, useful to keep scores low.

## Order matters: LVHA

For links, write in this order so later does not get overridden:

```css
a:link { }
a:visited { }
a:hover { }
a:active { }
```

Mnemonic: **L**o**V**e **HA**te.

## Recap

| State | Example |
|-------|---------|
| Hover/focus | `:hover`, `:focus-visible`, `:focus-within` |
| Position | `:first-child`, `:nth-child(even)` |
| Form | `:checked`, `:valid`, `:invalid`, `:disabled` |
| Group | `:is()`, `:where()`, `:not()`, `:has()` |
