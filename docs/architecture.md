# Architecture overview

This describes the intended separation of responsibilities, not an assertion that all interfaces or networking modes are implemented.

```text
User / application
       |
       v
+-------------------------+
| eve                     |
| interaction, planning,   |
| context, permission UX   |
+-------------------------+
       |
       | capability request
       v
+-------------------------+
| eef coordinator         |
| discovery, policy,       |
| routing, task lifecycle  |
+-------------------------+
       |
       | authenticated, authorized requests
       v
+-------------------------+
| eef nodes               |
| local capabilities,      |
| local enforcement,       |
| execution, results       |
+-------------------------+
```

## Responsibilities

### eve

- Accepts user requests from supported interfaces.
- Determines whether a model, tool, or device capability is appropriate.
- Requests permission for sensitive actions where required.
- Tracks the task's state and communicates results, errors, and uncertainty.

### eef

- Maintains the coordination and capability-discovery layer.
- Selects a suitable executor under applicable policy.
- Routes supported requests and results.
- Provides a reusable infrastructure interface for other modules and applications.

### eefn

- Runs on participating hosts.
- Advertises only allowed capabilities.
- Enforces local authorization and resource limits.
- Executes accepted tasks and reports their outcomes.

## Example workflow

A request originating on node A may be handled by a capability on node B:

```text
request -> eve -> eef -> eefn B -> eef -> eve -> user
```

The specific messages, channels, and available capabilities vary by implementation version. Network encryption alone does not authorize a task. The receiving node must independently enforce permission boundaries.

## Networking dependency

eve should use eef's supported transport and authorization interfaces. Pairing,
reconnection, relay paths, and any direct peer transfer depend on the specific eef
version and configuration. This repository does not define an eef release schedule
or claim that those modes are available.

## Design constraints

- Avoid equating language models with the whole assistant.
- Do not require the coordinator to host heavyweight AI models.
- Do not equate membership in a network with permission to access every resource.
- Keep the capability interface understandable to non-eve applications.
