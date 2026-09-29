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

# SECURE — 3400-0033-SM-FreeCAD

> Security posture, threat model, and secrets-handling notes for `3400-0000-SM-Software/3400-0033-SM-FreeCAD`.

## Threat model

- **Assets:** none of SimpleMotion's. The repo is a public fork of FreeCAD and holds upstream source plus a handful of SimpleMotion documentation files.
- **Main risk is disclosure.** The repo is public and cannot be made private, so anything committed here is published. Never commit client models, drawings, internal paths, credentials or anything from a `10-Client` project repo.
- **CI:** GitHub Actions is disabled, so upstream workflows cannot run with this org's minutes or secrets. Re-enabling it is a deliberate decision, not a default.

## Secrets handling

- All credentials follow the SimpleMotion `b64:<base64-payload>` envelope convention.
- No credential material is committed to this repo. Use the home-repo / GitHub Secrets / Keychain path instead.

## Reporting issues

- A vulnerability in **FreeCAD itself** goes to the FreeCAD project, as described in upstream's [`SECURITY.md`](SECURITY.md).
- Anything specific to **SimpleMotion's use of this fork**: email **security@simplemotion.com**.
