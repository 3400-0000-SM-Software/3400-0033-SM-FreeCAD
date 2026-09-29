<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/simplemotion/.github/main/assets/banners/SM-White.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/simplemotion/.github/main/assets/banners/SM-Black.svg">
    <img alt="SimpleMotion" src="https://raw.githubusercontent.com/simplemotion/.github/main/assets/banners/SM-Black.svg" width="800">
  </picture>
</p>

<p align="center">
  <em>Engineered for Architecture, Entertainment, Industry and Manufacturing.</em>
</p>

# CHANGE.md

Changelog for this repo (`3400-0000-SM-Software/3400-0033-SM-FreeCAD`). It records
SimpleMotion's changes to the fork only; FreeCAD's own history is upstream's git log
and release notes.

GitHub Actions is disabled on this repo, so sm-ci mints no `-develop-NNN` tags here.
Rows carry `—` in Version and Hash until that changes.

---

## Changelog

| Version | Hash | Date | Author | Notes |
|---------|------|------|--------|-------|
| — | — | 2026-09-29 15:08 UTC | Greg Gowans | **Add the SimpleMotion default files to the FreeCAD fork.** A fork notice at the top of README.md explains that the fork is a base for building SM workbenches and add-ons, and leaves upstream's README intact below it. Adds CLAUDE.md, CHANGE.md, SECURE.md, SM-FreeCAD.toml and .sm-version from 9998-0006-SM-Skeleton. ASSIGN.md is deliberately omitted because FreeCAD is LGPL-2.1 and not SimpleMotion IP, and the sm-ci and sm-pr stubs are omitted because Actions is disabled and a public repo cannot call the internal reusable workflows. |

---

## Versioning

This repo follows the SimpleMotion enterprise versioning policy. It is kept in
one canonical place rather than copied into every repo, so an amendment lands
once instead of being reconciled across the fleet:

<https://github.com/simplemotion/.github/blob/main/ANNEXE.md>
