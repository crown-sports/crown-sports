# crown

我做可复现的 Python 与 AI 工具：检查训练数据、定位 Agent 故障，把问题变成有回归测试的修复。

I build practical Python and AI tools, with reproducible examples and regression tests. My projects also cover floor-plan geometry and local learning workflows.

## 已合并的上游修复 / Merged upstream fixes

| Project | What changed | Evidence |
| --- | --- | --- |
| **Repowise** | Correct complexity scores for flat ternary dispatch across **seven languages**, while preserving real nesting and refreshing cached analysis. 修正七种语言的复杂度误报。 | [#4709 · merged](https://github.com/repowise-dev/repowise/pull/4709) |
| **Repowise** | Parse empty and no-definition CSD files without crashing; retain resource line ranges. 修复空输入解析崩溃。 | [#4492 · merged](https://github.com/repowise-dev/repowise/pull/4492) |
| **nanobot** | Apply the configured timeout to no-tools recovery and finalization requests so a stalled provider cannot hold a session indefinitely. 补齐模型请求超时保护。 | [#5496 · merged](https://github.com/HKUDS/nanobot/pull/5496) |

[Read the failure → fix → regression case studies / 查看修复案例](docs/upstream-work.md) · [Other open PRs / 待审贡献](https://github.com/pulls?q=is%3Apr+is%3Aopen+author%3Acrown-sports+-user%3Acrown-sports)

## 可直接试用的工具 / Tools to try

| If you need to… | Try | Scope |
| --- | --- | --- |
| Debug broken tool-call histories | [toolreply · v0.2.0 preview](https://github.com/crown-sports/toolreply/releases/tag/v0.2.0) | Offline CLI and [Marketplace Action](https://github.com/marketplace/actions/toolreply) for missing, duplicate and misplaced tool replies. Tested on Linux, Windows and macOS. |
| Check a calendar export or migration | [CalWitness live reports](https://crown-sports.github.io/calwitness/) | Compare recurring occurrences, moved exceptions and durations in two local ICS files over an explicit window. Unsupported input is reported as incomplete. |
| Check image-text data before fine-tuning | [VLM Data Doctor live reports](https://crown-sports.github.io/vlm-data-doctor/) | Inspect actual synthetic sample reports without installing. The local CLI checks exact overlap and document splits, not answer quality. |
| Decide whether a smaller vision model meets a quality budget | [VLM Precision Lab · v0.4.0](https://github.com/crown-sports/vlm-precision-lab/releases/tag/v0.4.0) | A recorded 3,792-request receipt study with reproducible CPU checks. Memory fell, but both model variants failed the quality gate. |
| Turn a wall mask into editable paths | [WallGraph](https://github.com/crown-sports/wallgraph#try-it) | PNG/SVG/JSON in original image coordinates. Bring a binary mask; no pretrained detector is bundled. |
| Compare room regions before and after an edit | [PlanRegions live demo](https://crown-sports.github.io/planregions/) | Region merges, splits and pixel flow, with saved local examples. |

[All projects, examples and limitations / 全部项目与使用范围](docs/projects.md)

## [Obsidian Study Flow](https://github.com/crown-sports/obsidian-study-flow) · 从原文到复习卡

在 PDF 中选一段原文，写下自己的理解，再做成卡片。复习时可以回到原来的页码和选区，摘录与卡片保存在本地 Markdown。

Turn a PDF passage and your own explanation into review cards. Keep the source link so you can check the original passage later.

![从 PDF 摘录整理理解与卡片 / Notes and cards made from a PDF excerpt](https://raw.githubusercontent.com/crown-sports/obsidian-study-flow/v0.2.1/docs/images/v0.2/03-inbox-card.png)

[试用示例库 / Try the example vault](https://github.com/crown-sports/obsidian-study-flow/releases/tag/v0.2.1) · 需要 Obsidian、PDF++ 和 Spaced Repetition。

## [DayWeave](https://github.com/crown-sports/dayweave) · 先看时间够不够

填写任务时长、截止时间和已有日程，再安排剩余工作。任务放不下时，查看缺多少时间、哪些事项需要调整；结果可导出为日历文件。

Schedule the work that remains around existing appointments. See time shortfalls and proposed changes, then export an `.ics` calendar file.

![只安排未完成的工作 / Scheduling the remaining work](https://raw.githubusercontent.com/crown-sports/dayweave/v0.2.2/docs/assets/remaining-work.png)

[运行本地示例 / Run the local demo](https://github.com/crown-sports/dayweave#open-it) · 早期版本，当前界面为中文。Preview; the current interface is in Chinese.

## [OpsResolve](https://github.com/crown-sports/opsresolve) · 修完配置，再检查业务请求

示例里的商店返回 503，健康检查却正常。查看网关与数据库配置中的两处问题，确认具体修改，再验证业务请求是否恢复。检查过程和结果写进事件报告。

The demo storefront returns 503 while health checks pass. Inspect two configuration faults, review the edits, and verify recovery with business requests.

![本地商店示例恢复后通过 10 次检查 / Ten recovery checks in the local storefront demo](https://raw.githubusercontent.com/crown-sports/opsresolve/v0.2.1/docs/assets/workbench.jpg)

[运行故障与恢复示例 / Try the failure-and-recovery demo](https://github.com/crown-sports/opsresolve#try-the-recovery-demo) · 截图为本地演示数据。Screenshot uses local demo data.

## Working together

Small reproducible bug reports, documentation fixes and real first-use feedback are welcome in each project's issue tracker. Please use synthetic examples when a report involves private documents or logs.

Thanks to [Harshit Nagila for the English Study Flow quickstart](https://github.com/crown-sports/obsidian-study-flow/pull/4), now merged with the original contribution preserved.

欢迎通过各项目的 Issue 提供复现步骤或试用反馈。项目中的生成示例、实验结果和平台验证范围都在对应文档中说明。
