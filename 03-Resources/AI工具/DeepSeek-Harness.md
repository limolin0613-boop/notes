# DeepSeek Harness

## 是什么

DeepSeek Harness（`dsh`）是 DeepSeek AI 开发的开源 Agent Harness，核心理念是“万物皆插件”（Everything is a Plugin）。

它基于 Cordis 架构，设计思路见论文《A Programming Paradigm for Spatiotemporal Composability》。桌面、功能、Agent 能力都可以做成插件，插件生态是这个项目的重点。

- 仓库：[deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness)
- 语言：TypeScript
- Star：282,266
- Fork：34,953
- 许可证：MIT
- 创建：2026-08-13
- 状态：Developer Preview，快速迭代中，会有不兼容的改动
- 文档：https://deepseek-harness.github.io/deepseek-harness/
- 最新预发布：v0.2.2-rc.3（2026-11-13）

## 怎么跑

### 用 npm 跑（最简单）

先装 Node.js，然后运行：

```bash
npx @deepseek-ai/dsh web
```

默认在 `http://127.0.0.1:3080` 启动 Web UI，本地运行会自动在浏览器打开。SSH 启动时只打印地址，加 `--no-open` 可以不自动打开浏览器。

### 从源码跑

```bash
git clone https://github.com/deepseek-ai/deepseek-harness.git
cd deepseek-harness
pnpm install
pnpm run build
pnpm dsh web
```

`pnpm run build` 准备构建产物，`pnpm dsh web` 直接用构建好的产物启动，不再重新构建。

开发模式：`pnpm run dev:web`，改代码自动重建；`make help` 可以看 Web 和桌面端的 Make 目标。

## 相关生态

- 插件精选列表：[awesome-dsh-plugin/awesome-dsh-plugin](https://github.com/awesome-dsh-plugin/awesome-dsh-plugin)（24,887 星）
- 桌面端：[anywhere-labs/dsh-desktop](https://github.com/anywhere-labs/dsh-desktop)（36,160 星），为 DSH 插件生态做的现代化桌面端；另有 [dataelement/dsh-desktop](https://github.com/dataelement/dsh-desktop)
- 手机端：[ccch1mneyyy/dsh-Go](https://github.com/ccch1mneyyy/dsh-Go)（24,698 星），手机本机运行，也能遥控电脑
- 插件市场：[dsh-market/dsh-market](https://github.com/dsh-market/dsh-market)（12,637 星），可视化插件市场，浏览、搜索、一键安装
- 多合一助手：[farion1231/cc-switch](https://github.com/farion1231/cc-switch)（154,909 星），支持 Claude Code、Codex、OpenCode、DeepSeek Harness 等

## 注意事项

- 还是开发者预览版，接口和行为可能随时变，不适合直接当生产工具依赖。
- 运行前先看仓库里的安全说明（SAFETY.md）。
- 反馈和 Bug 走 GitHub Discussions；自己写插件想被发现，给仓库打上 `dsh-plugin` 这个 topic。
- 贡献先看 CONTRIBUTING.md，Agent 开发先看 AGENTS.md。

## 来源

GitHub 趋势 / 搜索：deepseek harness，2026-11-17 查询，仓库页抓取时间 2026-11-16 18:30 UTC。
