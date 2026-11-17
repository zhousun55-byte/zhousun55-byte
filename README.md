<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
  <img src="assets/header-light.svg" alt="ZHOU · AI 应用与开发工具" width="100%">
</picture>

**做让多个 AI 模型协同干活的工具。** 独立设计并实现了多模型编程协作平台「接力台」（约 2.5 万行 TypeScript / JavaScript，191 项自动化测试），并向 AI 编程工具生态贡献插件与 PR。正在寻找 **AI 应用开发 / AI 工具开发** 岗位。

<p>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/LLM%20Agents-Claude%20Code%20%7C%20Codex%20%7C%20DeepSeek-555">
  <img src="https://img.shields.io/badge/Prompt%20%26%20Eval-多模型投票%20%2F%20交叉复核-555">
</p>

## 代表项目

### 🏃 RelayDesk · 接力台 — 多模型编程协作平台

一个 AI 的额度用完、卡住或出错时，自动换另一个 AI 接着做，并留下可检查的交接、快照和复核记录。

- **换 Agent 继续**：读取 Claude Code / Codex 的本地会话，还原对话主线，带着上下文交给另一个模型接手
- **强弱模型分工**：强模型拆任务、弱模型执行、强模型复核；额度用完自动换人，失败可一键退回快照
- **群聊决策**：多个模型匿名出方案、互投（不能投自己），再由强模型当主席汇总，结论写进任务约定
- **安全设计**：项目内容一律按不可信处理——检查命令需本机确认、拒绝符号链接越界写入、发给模型前自动抹掉密钥
- **工程质量**：命令行 + 本地网页（中英双语、深色模式、窄屏适配），191 项测试覆盖调度、解析、隔离与安全反例

[设计与实现 →](projects/relaydesk.md)　·　源码私有，面试可现场演示

### 📎 dsh-postman — DeepSeek Harness 文件投递插件

在 DeepSeek Harness 会话里选文件或文件夹，图片走消息附件，文本写进草稿。已被两份生态目录收录。

[项目说明 →](projects/dsh-postman.md)　·　[源码](https://github.com/zhousun55-byte/dsh-postman)

## 开源贡献

| 贡献 | 状态 |
| --- | --- |
| [magpie-community/plugins #646](https://github.com/magpie-community/plugins/pull/646)：council 多模型插件（并行提问、匿名投票、交叉评审） | 评审中 |
| [awesome-dsh-plugin #1153](https://github.com/awesome-dsh-plugin/awesome-dsh-plugin/pull/1153)：收录 dsh-postman | ✅ 已合并 |
| [awesome-deepseek-harness #308](https://github.com/0xsline/awesome-deepseek-harness/pull/308)：收录 dsh-postman | ✅ 已合并 |

## 我在想的问题

- 换一个模型接手时，怎样只带上真正有用的上下文，并核实前一位说的「已完成」
- 弱模型怎样在强模型的复核下稳定产出，把成本降下来
- 多模型并发调用时，怎样控制费用、及时取消
