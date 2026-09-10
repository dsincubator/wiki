## OKF Rules
- `contentRules.okf.enabled: true` in `.ok/config.yml` — `type` required except `index.md`/`log.md` which MUST NOT have frontmatter.
- `index.md` in any folder = frontmatter-free, entries are `[link](path) — description` bullets (see `index.md:3`).
- Use `exec("cat <path>.md")` / `exec("ls -A <dir>")` / `search({query})` for reads — never native `Read/Grep` on in-scope `.md`.

## Indexes on GitHub
- Browsable via `index.md` at root + `transcripts/index.md` (auto-generated). Other folders use live `exec("ls -A")` — no static `index.md` per subfolder by design (`okf.generate.index: false`). If GitHub browsing requires one, create `<folder>/index.md` frontmatter-free with link table (see `transcripts/index.md`).

## Useful Commands
- `ok start` + `ok open index` — preview
- `ok audit` / `ok lint` — validation
- `ok seed --pack <okf|knowledge-base> --dry-run` — inspect packs
