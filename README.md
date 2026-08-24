# 阿囤囤的简历修改小助手

一个面向中文求职者的 Codex Skill，用于诊断、重构和改写简历。

它不会只做文字润色，而是先确认目标岗位，再按照招聘方的阅读逻辑组织证据：在对话中给出简洁诊断，并同步生成一份只包含最终简历正文的 Word 文件。

## 主要能力

- 先确认目标岗位、方向和代表性 JD；
- 检查基本错误、时间与数据口径；
- 按“合理结构—当前问题—修改方向”输出简洁诊断；
- 用外行也能理解的语言改写工作经历；
- 按“项目背景—本人承担的角色—项目内容—项目成果”整理项目；
- 不编造经历和数据，缺失事实统一使用醒目标记的 `XXX`；
- 在完整诊断任务中生成可继续编辑的 `.docx` 最终简历。

## 安装

将本仓库克隆到 Codex Skills 目录：

```bash
git clone https://github.com/panggungunvibe/atutun-resume-helper.git ~/.codex/skills/atutun-resume-helper
```

重新打开 Codex 后即可使用。

## 使用示例

上传简历后输入：

```text
$atutun-resume-helper 帮我诊断并修改这份简历
```

Skill 会先询问目标岗位和 JD。没有 JD 时，也可以要求按通用岗位进行诊断。

## 输出内容

一次完整任务包含两部分：

1. 对话中的简洁诊断；
2. 只包含最终简历正文的 Word 文件。

Word 中不会放入诊断过程、修改建议或评语。所有无法从原简历确认的事实都会保留为 `XXX`，并使用黄色高亮或红色字体提示补充。

## 文件结构

```text
atutun-resume-helper/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── diagnosis-template.md
```

## 许可证

[MIT License](LICENSE)
