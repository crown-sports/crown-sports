# Project directory

[Back to profile](../README.md)

Each repository includes its own installation instructions, examples and verification limits. Releases range from early previews to stable packages; see the linked release page for the current status. Synthetic demonstrations are not production adoption or accuracy measurements.

| Project | Useful for | First step / limitation |
| --- | --- | --- |
| [toolreply](https://github.com/crown-sports/toolreply) | Finding missing, duplicated or misplaced tool replies in saved conversations | [v0.2.0 preview](https://github.com/crown-sports/toolreply/releases/tag/v0.2.0): installable CLI and [Marketplace Action](https://github.com/marketplace/actions/toolreply). Checks records; does not execute tools or certify API acceptance. |
| [VLM Data Doctor](https://github.com/crown-sports/vlm-data-doctor) | Validating image-text fine-tuning data and separating related documents | [Open the actual sample reports](https://crown-sports.github.io/vlm-data-doctor/). Exact overlap only; no label-quality judgment. |
| [VLM Precision Lab](https://github.com/crown-sports/vlm-precision-lab) | Comparing model quality, failures and service latency | [v0.4.0 receipt study and CPU checks](https://github.com/crown-sports/vlm-precision-lab/releases/tag/v0.4.0). Lower memory did not establish a passed quality gate. |
| [EvidencePack](https://github.com/crown-sports/evidencepack) | Selecting evidence within a context budget and checking quotations | Local examples; checks supplied evidence, not the truth of a generated conclusion. |
| [OpsResolve](https://github.com/crown-sports/opsresolve) | Diagnosing a service failure, reviewing configuration edits and verifying recovery | Run the local HTTP/SQLite failure-and-recovery demo. |
| [NetOps Fault Lab](https://github.com/crown-sports/netops-fault-lab) | Ranking ambiguous link faults and choosing the next diagnostic probe | Reproducible simulations with known paths; no production accuracy claim. |
| [WallGraph](https://github.com/crown-sports/wallgraph) | Extracting centerlines and connections from a binary wall mask | Generated demo needs no model; scan detection needs compatible supplied weights. |
| [PlanRegions](https://github.com/crown-sports/planregions) | Extracting room regions and explaining merges/splits after edits | [Interactive example](https://crown-sports.github.io/planregions/). No automatic room semantics. |
| [PlanMetric](https://github.com/crown-sports/planmetric) | Calibrating pixel measurements from supplied dimensions | Check scale conflicts first; not surveying accuracy. |
| [PlanPortals](https://github.com/crown-sports/planportals) | Exploring room connectivity and door-closure scenarios | Supply opening labels; no bundled door/window detector. |
| [Obsidian Study Flow](https://github.com/crown-sports/obsidian-study-flow) | Turning source passages into explanations and review cards | Download the example vault. PDF++ and Spaced Repetition are separate dependencies. |
| [Zhixing Notes](https://github.com/crown-sports/zhixing-notes) | Capturing notes, clearing an inbox and reviewing a week | Local Markdown workspace and Obsidian plugin. |
| [DayWeave](https://github.com/crown-sports/dayweave) | Scheduling remaining work around a calendar | Local single-user preview; exports ICS, does not operate a notification service. |
| [Chat Task Bridge](https://github.com/crown-sports/chat-task-bridge) | Auditing and merging CSV files with traceable results | Offline workflow verified; real WeChat/Lark account integration remains pending. |

## Contributing

The most useful first contribution is a reproducible problem from actual use: what you tried, the smallest synthetic input and what you expected. Follow the individual repository's contribution guide. Please keep personal documents, credentials and private logs out of public issues.
