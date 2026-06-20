# CLAUDE.md — surfn-mint-x-grey

## Project overview

Standalone repo for the **Surfn-Mint-X-Grey** icon theme, split out of the `erikdubois/surfn`
monolith. See [README.md](./README.md).

## Current state

Ships one theme: `usr/share/icons/Surfn-Mint-X-Grey/`. Packaged as `surfn-mint-x-grey-icons-git` (recipe in
`~/KIRO-PKG-BUILD-ICONS/surfn-mint-x-grey/`), `depends=('surfn-icons-git')` — the base Surfn theme.

## Patterns & decisions

- Theme dir PascalCase; repo/package lowercase. `icon-theme.cache` gitignored (rebuilt by
  the pacman hook on install). Bash scripts follow the canonical Kiro template.
