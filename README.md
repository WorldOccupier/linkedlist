# linkedlist

A personal links page that looks and feels like Neovim. Dark theme, relative line numbers, a cursorline, a statusline with modes, and a command line — all keyboard-driven.

It's a single `index.html` with no build step and no dependencies (apart from the JetBrains Mono web font).

## Keys

| Key | Action |
|---|---|
| `g` | Open GitHub in a new tab |
| `x` | Open X in a new tab |
| `j` / `k` (or arrows) | Move the selection down / up |
| `G` | Jump to the last link |
| `Enter` / `o` | Open the selected link |
| `/` | Filter links as you type |
| `:` | Command mode |
| `Esc` | Back to normal mode / clear the filter |

### Commands

| Command | Action |
|---|---|
| `:open <name>` | Open a link by name (also `:o`, `:e`, `:tabnew`) |
| `:qa` | Open every link |
| `:<n>` | Jump to link *n* |
| `:colo` | Toggle an alternate colour scheme |
| `:q` | Try it |

## Adding links

Edit the `LINKS` array near the top of the `<script>` in `index.html`:

```js
{ key:"g", name:"GitHub", url:"https://github.com/WorldOccupier", icon:"", c:"var(--fg)" },
```

- `key`: single-character shortcut. `j`, `k`, `q`, `:`, `/`, `?` and space are reserved, so those become uppercase.
- `icon`: any glyph or emoji.
- `c`: accent colour, either a theme variable (`--blue`, `--green`, `--red`, …) or any CSS colour.

## Running locally

```sh
python3 -m http.server 8787 --bind 0.0.0.0
```

Then open `http://localhost:8787`, or `http://<your-ip>:8787` from another device on the same network. Opening `index.html` directly in a browser also works.
