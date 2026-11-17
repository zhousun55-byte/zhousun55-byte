<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
  <img src="assets/header-light.svg" alt="ZHOU · AI 应用与开发工具" width="100%">
</picture>

做 AI 应用和开发工具，关注的是怎样让多个模型分工合作、互相复核，并且用测试和评测确认结果可靠。2026 年 7 月以来和 Claude Code、Codex、Kimi 一起做了 9 个项目，正在找 AI 应用开发 / AI 工具开发方向的工作。

全部作品：**[zhousun55-byte.github.io](https://zhousun55-byte.github.io)**

常用：TypeScript · Node.js · Python · MCP · Claude Code · Codex · GitHub Actions

## 代表项目

**[RelayDesk 接力台](projects/relaydesk.md)** · 多模型编程协作平台

一个模型额度用完、卡住或出错时，自动换另一个模型接着做，每一棒留下交接单和文件快照，可以复核也可以退回。

- 读取 Claude Code / Codex 的本地会话，带着对话主线交给另一个模型接手
- 强模型拆任务和复核，便宜的模型执行，额度用完自动换人
- 多个模型匿名出方案、互相投票，再由强模型汇总，结论写进任务约定
- 项目内容按不可信处理：检查命令要本机确认，拒绝越界写入，发给模型前抹掉密钥
- 约 2.5 万行 TypeScript / JavaScript，191 项自动化测试

源码私有，面试可现场演示。

**[council](https://github.com/zhousun55-byte/magpie-council)** · 多模型会审插件（MCP）

几个模型同问一个问题、匿名投票，或请另一家的模型评审代码。按故障类型自动冷却，慢的模型自动找替身。25 项测试，CI 通过，已向上游提交 [PR #646](https://github.com/magpie-community/plugins/pull/646)。

**[dsh-postman](projects/dsh-postman.md)** · DeepSeek Harness 文件投递插件

在会话里直接选文件或文件夹，图片作为附件，文本写进草稿。已被两份生态目录收录。

## 其他作品

| 项目 | 做了什么 |
| --- | --- |
| K线阅读 | TradingView 读盘指标，681 次提交；用体检脚本核对 AI 写的文档和代码是否一致 |
| 交易知识库与问答技能 | Obsidian 知识库加两个 Claude Code 技能：按问题定位相关页面作答、定期追踪来源更新 |
| Jev 中文判别基准 | 用 57 篇真实笔记测小模型的中文归类能力，去掉会泄露答案的字段，结果可复现 |
| 摄影作品集网站 | React + TypeScript + Vite，为国内访问做了资源本地化 |

这几个项目是私有的，介绍见[作品集网站](https://zhousun55-byte.github.io/#works)。

## 开源贡献

| 贡献 | 状态 |
| --- | --- |
| [magpie-community/plugins #646](https://github.com/magpie-community/plugins/pull/646)：council 多模型插件 | 评审中 |
| [awesome-dsh-plugin #1153](https://github.com/awesome-dsh-plugin/awesome-dsh-plugin/pull/1153)：收录 dsh-postman | 已合并 |
| [awesome-deepseek-harness #308](https://github.com/0xsline/awesome-deepseek-harness/pull/308)：收录 dsh-postman | 已合并 |
