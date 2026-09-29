# Welcome to [Slidev](https://github.com/slidevjs/slidev)!

## Development

Install [mise](https://mise.jdx.dev/getting-started.html) and, from this repository:

```bash
mise trust
mise install
mise run setup
mise run dev
```

`mise.toml` pins Node 24.21.0 and pnpm 10.34.4 (the same version as
`packageManager` in `package.json`). `setup` runs `pnpm install --frozen-lockfile`.
Then visit <http://localhost:3030>.

| Command | Action |
| --- | --- |
| `mise run setup` | Install dependencies from the lockfile |
| `mise run dev` | Slidev dev server (`--open --remote`) |
| `mise run check` | Build to validate the slides |
| `mise run build` | Generate `dist/` |
| `mise run export` | Export to PDF (optional, see below) |

There is no separate lint or test suite; `check` is currently the build. CI
runs the same tools and the same check.

PDF export needs Playwright's Chromium, which is not a project dependency:
install it on demand with `mise exec -- pnpm add -D playwright-chromium` before
running `mise run export`.

In a new checkout or worktree, run `mise trust` and `mise run setup`. To run a
second dev server at the same time, give it another port:
`mise run dev -- --port 3031`.

Edit the [slides.md](./slides.md) to see the changes.

Learn more about Slidev at the [documentation](https://sli.dev/).
