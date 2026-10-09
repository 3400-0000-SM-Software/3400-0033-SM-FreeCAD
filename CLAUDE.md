# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

SimpleMotion's fork of [FreeCAD/FreeCAD](https://github.com/FreeCAD/FreeCAD), used as a base for building SimpleMotion workbenches and add-ons against FreeCAD's own source: building FreeCAD locally, reading and debugging the internals a workbench depends on, and pinning the upstream revision our add-ons are tested against.

Owner: Greg Gowans.

## Working rules

- **This is upstream's code, not ours.** FreeCAD is LGPL-2.1-or-later and belongs to its contributors. There is deliberately no `ASSIGN.md`; never add one, and never change `LICENSE` or any upstream licence header.
- **Do not adopt the SM-MCP layout here.** Upstream's tree stays where upstream puts it, so `main` can keep merging from `FreeCAD/FreeCAD`. SimpleMotion files are limited to `CLAUDE.md`, `CHANGE.md`, `SECURE.md`, `sm-repo.toml`, `SM-FreeCAD.toml`, `.sm-version` and the fork notice at the top of `README.md`, which sits between the `BEGIN`/`END SimpleMotion fork notice` comments.
- **A workbench we ship lives in its own repo**, installed through the Addon Manager, not inside this tree. Only patches that must touch FreeCAD's source belong here, each on its own branch.
- **Never open a PR against `FreeCAD/FreeCAD` from Claude.** Upstream's [`AI_POLICY.md`](AI_POLICY.md) requires a human to write and present every contribution, and it rejects clearly AI-generated code, commit messages and PR descriptions. A change meant for upstream is handed to a human to author.
- **The repo is public and cannot be made private.** Never commit client models, drawings, credentials or internal paths.
- **GitHub Actions is disabled.** Upstream's workflows must not run on this org's minutes. Do not add the sm-ci or sm-pr caller stubs: a public repo cannot call the internal reusable workflows, so they would only fail at startup.
- **Keep a checkout sparse and blobless** unless you actually need to build (`git clone --filter=blob:none`). The full tree is about 2.9 GB.
- **Do not include "Co-Authored-By" trailers in git commits.** (Enterprise rule, applies repo-wide.)
- **Keep `sm-repo.toml` ("alpha") and `SM-FreeCAD.toml` current.** `sm-repo.toml` is the authoritative structured record of what this repo holds (identity in `[alpha]`, schema in `SM-ALPHA.md`); `SM-FreeCAD.toml` keeps the fork's data, including the upstream revision it was forked from.
