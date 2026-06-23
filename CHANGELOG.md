# Changelog

## 2026.06.23 — relicensed GPL3 + refreshed from upstream

**Install docs:** the README install section now lists the meta packages (top-level `*-icons-meta`, plus the group meta where applicable) alongside the per-variant `*-icons-git` package — replacing the outdated single `pacman -S` line.

### What Changed

Part of the Surfn Mint-X/Mint-Y per-colour rollout. Two changes to this repo:
- **Licence corrected to GPL-3.0** (was Attribution-NonCommercial-ShareAlike 4.0). The LinuxMint
  upstream `mint-x-icons` is GPL-3+ (`debian/copyright` `Files: * → GPL-3+`); the NonCommercial
  clause was wrong and inconsistent with the rest of the Surfn Mint-X family.
- **Icon data refreshed** from `linuxmint/mint-x-icons` and `index.theme` standardised to
  `Inherits=Surfn,Adwaita,gnome,hicolor`, matching the other per-colour Mint-X repos.

### Files Modified

- `LICENSE` (GPL-3 text), `README.md` (licence line), `usr/share/icons/Surfn-Mint-X-Grey/`.

## 2026.06.20 — split out of the surfn monolith

### What Changed

Initial standalone repo. The **Surfn-Mint-X-Grey** theme was carved out of the monolithic
`erikdubois/surfn` repo so it ships as its own package, `surfn-mint-x-grey-icons-git`, depending on the base
`surfn-icons-git`.

### Technical Details

- `usr/share/icons/Surfn-Mint-X-Grey/` copied verbatim from the monolith; theme dir kept PascalCase
  so `Inherits=` resolution is unaffected. Repo/package names lowercase per Arch convention.
- `icon-theme.cache` not shipped — the pacman gtk-update-icon-cache hook rebuilds it on install.

### Files Modified

- Initial scaffold + usr/share/icons/Surfn-Mint-X-Grey/
