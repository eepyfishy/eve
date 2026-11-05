# eve

**An agentic assistant designed to work across devices, powered by [eef](https://github.com/eepyfishy/eef).**

> **Status:** Design stage. This repository contains documentation, with no eve application, installer, or verified demo yet. Features below describe the intended assistant.

## What is eve?

eve is an assistant project built around a simple idea: an assistant should be able to do more than respond to text. It should be able to understand a request, plan an appropriate action, use available tools and devices **with permission**, and report what happened.

The project began as a DIY assistant. As it became clear that eve would need a way to work with different devices and their capabilities, **eef** began as eve's API and grew into a reusable distributed framework.

Today, the intended relationship is:

- **eve** is the assistant people interact with.
- **eef** is the framework that discovers, authorizes, and coordinates capabilities.
- **eefn** means **eef node**. It is the node process that exposes enabled capabilities under the node owner's controls and lives in the eef repository.

The public edition is intended to make that experience available to others without depending on any one person's private assistant data or configuration.

## What makes the idea different?

**One assistant, more than one device.** eve is intended to offer a continuous assistant experience across interfaces while using capabilities available through eef.

**Owner-controlled capabilities.** A node owner chooses which features to enable. Sensitive actions still follow the permissions and limits supported by the selected eef version.

**Models are components, not the assistant's identity.** Language, vision, speech, and other models may support eve, but none individually defines the whole system.

**Useful beyond eve.** eef is designed to serve other applications and modules as well; eve is its original motivating use case.

## Example interaction (illustrative)

1. A user asks eve to perform a task that requires another device.
2. eve identifies an appropriate capability.
3. eef routes an authorized request to an available node.
4. The node enforces its local permissions and performs the operation.
5. eve explains the result, including failures or actions requiring approval.

This is the target experience; availability of each step depends on the current implementation and demo scope.

## Project boundaries

- The public edition is **not** a release of a personal, privately configured eve instance.
- It must not include personal memories, tokens, credentials, private prompts, device addresses, or private integrations.
- It should not claim unrestricted autonomy or guaranteed safety.
- Planned features are distinguished from tested implementations.

## Documentation

| Document | Contents |
| --- | --- |
| [Vision](docs/vision.md) | Origin, purpose, product goals |
| [Architecture](docs/architecture.md) | Relationship between eve, eef, and eefn |
| [Capabilities and status](docs/capabilities.md) | Public-facing functionality and evidence rules |
| [Demonstration plan](docs/demo.md) | A proposed two-node workflow and its acceptance criteria |
| [Security and trust](docs/security.md) | Permission model, risks, and principles |
| [Roadmap](docs/roadmap.md) | Intended development phases |
| [Public/private boundary](docs/public-private.md) | What belongs in public documentation |
| [Contributing](CONTRIBUTING.md) | How to discuss and propose improvements |

## Related projects

- [eef](https://github.com/eepyfishy/eef): the framework repository, containing both the eef coordinator and [eef node](https://github.com/eepyfishy/eef/tree/main/crates/eefn).

## Availability

There are no eve setup commands yet. For eef and eefn setup, use the [eef user guide](https://github.com/eepyfishy/eef/blob/main/docs/USER_GUIDE.md). Installing eef or eefn does not install eve.

## License

The code and documentation in this repository are available under the [MIT License](LICENSE).
