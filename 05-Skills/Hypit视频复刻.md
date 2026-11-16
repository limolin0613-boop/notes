# Hypit 视频复刻

## 是什么

Hypit 是一个 AI Agent 视频系统，用来复刻爆款视频。给它一个参考视频，它会把视频复刻成一个完整、可编辑的工作流，而不是只给一份分镜脚本。

可以复刻和替换的部分包括：画面、字幕、旁白、B-roll、特效，换主角、换文案、换产品、换语言、换画幅都可以，一次能出多个版本。

- 仓库：[hypit-ai/hypit](https://github.com/hypit-ai/hypit)
- 语言：TypeScript
- Star：30,148
- 最新版本：v0.3.3（2026-11-16）
- 许可证：Apache-2.0 with conditions

## 使用流程

1. 发一个视频链接或视频文件给 Muse。
2. 说一句指令，例如：“用 Hypit 复刻这个视频，形象换成猫咪”。
3. Muse 按 Hypit 流程分析原视频结构，生成 SVML 工作流，替换指定内容，渲染出新视频。

## 需要准备什么

- **参考视频**：链接要能下载，TikTok、Reels、YouTube 有的链接下不了，下载不了时改发视频文件。
- **替换要求**：想换成什么形象、换什么文案、换什么产品、什么语言、什么画幅、要几个版本，提前说清楚。
- **模型服务账号**：Hypit 本身免费开源，但换脸、生成新画面、配音等要走模型服务，按量收费。可以用 HypitHub，也可以用自己的 API。费用由模型服务方收，不是 Hypit 收。

## 安装

### 在 Muse 里

已经安装为 Muse 自定义 skill：

- 源码：`~/workspace/skill-sources/hypit/`（37M）
- Skill：`~/workspace/custom-skills/hypit/`
- 触发词：Hypit、hypit、视频复刻、克隆爆款视频

以后直接说“用 Hypit 复刻这个视频”即可。

### 在自己 Mac 上

Hypit 没有 Mac .dmg，官方安装方式是在终端运行：

```bash
npx skills add hypit-ai/hypit -g
```

要求：Node 22.15+、pnpm 10.33。首次使用时，Agent 会检查 Hypit 可执行文件并协助准备。

## 注意事项

- 第一次搭环境比较重，有社区反馈安装时要拉一堆工具和模型，大约 10G 左右，效果因视频而异，装之前先想好。
- 不要用 Hypit 冒充真人，也不要复刻没有使用权的视频。换真人脸 / 声音前，先确认对方同意和版权。
- 不要把复刻出的视频当成原作者的作品发布。
- 示例成本仅供参考：官方示例里一个 20 秒左右的短视频，模型费用约 1 美元，具体以实际使用的模型服务计费为准。

## 相关链接

- 官网：https://hypit.ai
- 快速开始：https://hypit.ai/quickstart/
