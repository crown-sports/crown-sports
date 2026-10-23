# crown

我写一些能在本地用起来的工具：把读过的资料留下来，把工作放进实际可用的时间，查清服务为什么出错。

I build local tools for studying, planning work, and investigating service failures.

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

## 上游贡献 / Upstream contribution

- [nanobot #5496 — 已合并 / Merged](https://github.com/HKUDS/nanobot/pull/5496)：让恢复和收尾阶段、不调用工具的模型请求也受超时限制，避免会话一直等待。Apply the configured timeout to no-tools recovery and finalization requests so a stalled provider does not hold the session indefinitely.
