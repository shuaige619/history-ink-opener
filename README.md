# 历史水墨开场与正文衔接

根据中国历史故事联动设计片头口播、人物特征和时代意象，调用 cinematic-director 设计历史剧片头蒙太奇或叙事序幕、水墨关键帧与转场，使用 MiniMax H3 时调用 h3-prompt-writing 编译提示词，经项目选定工作台生成并接入正文。适用于跨故事复用的历史开场；整期文稿修订与验收沿项目口播流程，生成画面不当史料。

`history-ink-opener` · 原创 Skill · 内容版本 `e9a9086358e5`

## 适用场景

根据中国历史故事联动设计片头口播、人物特征和时代意象，调用 cinematic-director 设计历史剧片头蒙太奇或叙事序幕、水墨关键帧与转场，使用 MiniMax H3 时调用 h3-prompt-writing 编译提示词，经项目选定工作台生成并接入正文。适用于跨故事复用的历史开场；整期文稿修订与验收沿项目口播流程，生成画面不当史料。

## 安装与使用

```sh
git clone https://github.com/shuaige619/history-ink-opener.git
cd history-ink-opener
```

将此目录按宿主支持的方式登记为本地 Skill，或把 [SKILL.md](SKILL.md) 交给支持 Agent Skills 的助手读取。保留 `scripts/`、`references/` 等配套目录的相对位置；下载完成不代表宿主已加载。

读取当前写作工作区的规范；导演与 H3 提示词等外部 Skill 按 references/upstream-sources.json 单独取得。媒体生成依赖用户指定的工作台。

## 输入与输出

**输入：** 历史故事、已锁口播或片头范围，以及当前项目规范和可复用素材。

**输出：** 开场叙事方案、人物与时代意象、镜头及关键帧提示词，按授权范围进一步交付片段和正文接点。

## 使用示例

```text
请使用 history-ink-opener 为提供的历史故事设计开场，先核当前项目规范与已锁文稿，交付分镜、关键帧提示词及正文衔接方案。
```

以上是调用示例，不是已完成业务运行的记录。

## 工作方式

- 先识别本次范围
- 0. 联动设计片头口播与画面
- 1. 调用 cinematic-director 设计本期镜头
- 2. 从设定板写成可生成的镜头
- 3. 调用模型提示词 Skill，再交工作台生成
- 4. 让片头进入正文
- 交付

- [assets/minimax-design-custom-skill-prompt.md](assets/minimax-design-custom-skill-prompt.md)
- [references/ai-writing-handoff.md](references/ai-writing-handoff.md)
- [references/body-handoff.md](references/body-handoff.md)
- [references/character-prompt-design.md](references/character-prompt-design.md)
- [references/character-scene-storyboard.md](references/character-scene-storyboard.md)
- [references/director-h3-handoff.md](references/director-h3-handoff.md)
- [references/minimax-design-handoff.md](references/minimax-design-handoff.md)
- [references/narration-picture-design.md](references/narration-picture-design.md)
- [references/observed-style.md](references/observed-style.md)

## 验证与限制

本次检查公开副本的文件结构、来源记录与路径可移植性；没有重新生成或验收历史片头视频。

模型输出与业务事实需要结合具体材料核对；结构和上传检查不能替代业务效果测试。

## 来源与二创说明

作者确认原创。公开副本将个人工作区绝对路径转为当前项目约定，保留外部依赖及其作者、版本与许可记录。

文件身份与发布标准版本记录在 [发布清单](skill-release.json) 中。问题反馈请附复现输入、期望结果及内容版本，并先移除私人数据。

## 许可证

以仓库随附的 LICENSE / NOTICE 为准；未附许可证的部分尚未授予额外使用许可，请联系作者。
