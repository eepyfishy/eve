# Capabilities and implementation status

All capabilities below are planned for eve. This repository currently contains
documentation only; no eve application or end-to-end demo is included. Features
implemented in eef alone do not prove an eve integration works.

| Capability | Public objective | Public verification |
| --- | --- | --- |
| Assistant interaction | Interpret requests and return useful responses | Planned |
| Tool/capability requests | Call approved eef capabilities | Planned |
| Multi-node task execution | Request work on a different node | Planned |
| Permission-aware operations | Reject tasks without the required authority | Planned |
| Model flexibility | Support interchangeable model backends | Planned |
| Voice and media workflows | Accept audio/video-related input through integrations | Planned |
| Cross-interface continuity | Maintain a coherent assistant identity across interfaces | Planned |
| Multi-instance tasks | Handle unrelated tasks concurrently | Proposed |
| Group resource cooperation | Access contributed, narrowly approved resources | Planned / depends on eef |
| Direct peer transfers | Move approved data between peers | Planned / depends on eef networking |

## How to update this page

For each confirmed feature, record:

- **Version/commit:** the relevant public revision.
- **Evidence:** link to a test, demonstration, or release notes.
- **Conditions:** operating system, hardware, network setup, and permissions used.
- **Limitations:** known caveats and unsupported cases.

Do not infer implementation merely because a capability appears in architectural documentation.
