# Roadmap

This is a directional roadmap for the **public eve experience**, not a promise of dates or a replacement for the eef release roadmap.

## Phase 1 — Credible proof of concept

- Publicly explain the eve/eef/eefn relationship.
- Build a minimal eve request interface.
- Show at least one real end-to-end action on another device.
- Demonstrate a denied operation and owner approval where supported.
- Record limitations and exactly which software revision was used.

## Phase 2 — Reliable assistant foundation

- Make request and result handling predictable.
- Improve task lifecycle, error reporting, approval UX, and recovery.
- Support useful model/tool integrations without tying identity to one model.
- Document setup and configuration once there is a repeatable public build.

## Phase 3 — Better connectivity and extensibility

- Adopt stable eef capability APIs.
- Improve discovery and pairing as eef networking matures.
- Add optional interfaces and modules without hard-coding them into eve.
- Support narrowly scoped shared resources with reliable owner controls.

## Longer-term ideas

- Richer vision, audio, and automation workflows.
- Continuity across applications and devices.
- Multiple concurrent task sessions under one assistant experience.
- More flexible multi-owner resource cooperation.

Features in this section are proposals, not committed public-release milestones.

## Dependency on eef

Track framework implementation and release status in the [eef repository](https://github.com/eepyfishy/eef). eve's readiness depends on the exact eef capabilities it uses. A future eve demo or release must identify its compatible eef revision and verified workflow; this roadmap assigns no eef version numbers or release dates.
