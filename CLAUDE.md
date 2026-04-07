# Prezto Fork — Branch Strategy

This is a fork of [sorin-ionescu/prezto](https://github.com/sorin-ionescu/prezto).

## Branches

- **`master`** — clean mirror of `upstream/master`. No personal changes.
- **`personal`** — personal config (runcoms) rebased on top of master. This is the active checkout.

## Updating from upstream

```bash
git fetch upstream
git checkout master && git merge upstream/master
git checkout personal && git rebase master
git submodule update --init --recursive
```

## Remotes

- `origin` — `git@github.com:TanakritBenz/prezto.git`
- `upstream` — `https://github.com/sorin-ionescu/prezto.git`

## Key files (personal config)

All personal customizations live in `runcoms/`:
- `runcoms/zshenv` — environment variables (PATH, exports). Sourced on every shell.
- `runcoms/zshrc` — interactive config (aliases, functions, completions).
- `runcoms/zpreztorc` — Prezto module config (prompt theme, syntax highlighting, etc.)
