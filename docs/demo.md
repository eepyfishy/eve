# Demonstration plan

This is a plan, not a published or verified demonstration. Its purpose is to show
a real request flowing from eve through eef to another node, with visible user control.

## Minimal demo hardware

- **Node A:** a computer running eefn and the future eve implementation or interface.
- **Node B:** a second computer running eefn with one intentionally enabled capability.
- **eef coordinator:** hosted on one of these computers, as supported by the chosen tested build.

## Suggested live sequence

1. **Discover:** show two connected nodes and one capability offered by node B.
2. **Request:** ask eve to use a capability verified on the selected eef build.
3. **Execute:** visibly show dispatch to node B, execution, and a result returned to eve.
4. **Deny:** disable or revoke the capability and repeat the request, demonstrating a safe failure.
5. **Restore:** explicitly re-enable approval and show a successful request if the implementation supports it.

Use only actions proven to work on the actual demonstration build. If an assistant planner is not ready, describe the prototype command mapping plainly rather than presenting it as autonomous reasoning.

## What the audience should understand

- eve is the assistant they interact with.
- eef coordinates work and routes capability requests.
- eefn performs the work on participating machines.
- Device owners control which capabilities are exposed.

## Planned versus demonstrated

Use three clear labels in the presentation:

- **Live:** demonstrated on actual hardware during the pitch.
- **Prototype:** implemented to some degree, but not reliable or complete enough for the live demo.
- **Planned:** architectural or product goals that are not available yet.

## Demo safety checklist

- Use test credentials, non-sensitive files, and disposable sample inputs.
- Keep unneeded capabilities off.
- Prepare a fallback recording of the **same authentic tested procedure** in case networking fails.
- Do not expose local tokens, private addresses, account names, or personal data on the projector.
- State failures and manual steps accurately.
