# Security and trust

Security is a design constraint, not a guarantee. Neither a working demo nor encrypted networking proves that an assistant is safe to grant unrestricted access to a host.

## Core principles

1. **Deny by default:** a device does not expose a sensitive capability merely because it joined an eef network.
2. **Local authority:** the resource owner retains ultimate control over what runs on their device.
3. **Least privilege:** grant only the resource, operation, duration, and limits needed for a task.
4. **Separate identity and authorization:** verifying a remote node's identity is not permission for it to use every tool.
5. **Treat input as untrusted:** prompts, documents, chat messages, and remote tool output may contain malicious instructions.
6. **Isolate execution:** process separation alone should not be described as a sandbox; untrusted code needs meaningful OS-level isolation.
7. **Make decisions visible:** sensitive actions should have clear approval, denial, and audit behavior.
8. **Revocation and recovery:** compromised credentials or devices must be removable without depending on indefinite trust.

## Threats to consider

- Prompt injection attempting to cause unauthorized actions.
- A compromised or malicious remote participant requesting capabilities beyond its grant.
- Eavesdropping, tampering, or replay on network links.
- Resource exhaustion through excessive workload requests.
- Leakage of logs, credentials, model prompts, private files, or personal context.
- Compromise or malfunction of the coordinating component.

## Current security status

eve has no application or security validation published in this repository yet.
The principles above are requirements for implementation. Consult the selected
eef version for its actual protections and limitations, and verify the complete
eve integration before making deployment claims.

## Responsible reporting

Until a dedicated security reporting process is published, avoid posting exploit details, credentials, or sensitive logs in public issues. Repository maintainers should add a private disclosure contact before inviting security reports.
