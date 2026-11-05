# Vision

## From an assistant to a framework-backed assistant

The initial project was a DIY assistant: a system that could respond to requests and take useful actions on its user's computer. It was not conceived as a general-purpose distributed framework.

As eve's requirements grew, a device and capability API became necessary. That API evolved into **eef**, a framework for coordinating selected capabilities across devices. eef is now a project in its own right, but eve remains the original reason for building it.

## Product goals

The public eve project aims to provide:

1. **Useful action:** perceive requests, plan steps, request approval where required, act through bounded capabilities, and communicate outcomes.
2. **Continuity across interfaces:** a coherent assistant experience whether interaction comes from desktop, chat, voice, or a future integration.
3. **Node cooperation:** use approved capabilities from local or remote eef nodes without giving an assistant unrestricted control of every host.
4. **User ownership:** let users choose their models, connected capabilities, permissions, and personalization.
5. **Extensibility:** allow additional integrations without permanently embedding every feature into the assistant core.

## Non-goals for the initial public demonstration

- A fully autonomous general intelligence.
- A finished cross-platform ecosystem.
- Fully decentralized, coordinator-independent networking.
- Automatic training or modification of models.
- Access to devices or private data without explicit authorization.

A focused demonstration is sufficient to communicate the direction of the project. No unimplemented capability should be presented as complete.

## Distinguishing the projects

**eve** is the user-facing assistant. **eef** provides a capability network that eve can use. Both matter to the overall pitch: the assistant explains *why* the infrastructure is useful, and the infrastructure explains *how* the assistant can extend beyond one computer.
