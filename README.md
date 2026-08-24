# 阿囤囤的简历修改小助手

一个可以安装到任何支持 Skills 的 Agent 中使用的中文简历修改 Skill。

把下面这句话直接发给你的 Agent：

> 帮我安装这个skill：[https://github.com/panggungunvibe/atutun-resume-helper](https://github.com/panggungunvibe/atutun-resume-helper)

安装完成后，它可以读取你的 PDF 或 Word 简历，结合求职方向进行诊断，最终生成一份修改后的 Word 简历。

## 三步完成简历修改

### 第一步：上传自己的简历

向 Agent 上传需要修改的简历，例如：

- PDF 简历；
- Word 简历；
- 简历截图或整理好的文字内容。

然后告诉它：

```text
帮我诊断并修改这份简历
```

### 第二步：说明求职方向

求职方向越具体，简历修改得越准确。建议提供目标岗位、行业方向、目标职级，以及具体职位 JD、招聘链接或截图。

例如：

```text
我想找 B 端 SaaS 产品经理，工作经验 3 年。以下是目标岗位 JD。
```

如果暂时没有明确方向，也可以直接说：

```text
先按通用产品经理帮我诊断
```

### 第三步：获得诊断和最终版简历

Agent 会先在对话中告诉你：

1. 一份适合目标岗位的简历应该采用什么结构；
2. 你在每个结构下面目前存在什么问题；
3. 建议如何修改。

随后，它会基于诊断结果生成一份修改后的 Word 简历。Word 文件只保留最终简历正文，不会混入诊断过程和修改建议。

## 最终产出效果

![简历诊断与最终 Word 产出示例](assets/resume-output-example.png)

最终会同时得到：

- 对话中的结构化简历诊断；
- 一份可继续编辑的 `.docx` 最终简历。

简历中缺少但值得补充的信息会使用 `XXX` 占位，并通过黄色高亮或红色字体提醒。Skill 不会替你编造工作经历、项目数据或业务成果。

## 这个 Skill 会做什么

- 检查联系方式、时间、数字和文字等基本错误；
- 按目标岗位重新组织简历结构和内容顺序；
- 用跨行业招聘方也能理解的语言改写工作经历；
- 按“项目背景—本人承担的角色—项目内容—项目成果”整理项目；
- 区分个人贡献与公司、团队取得的整体结果；
- 根据现有经历判断目标岗位的匹配程度；
- 在同一任务中生成最终版 Word 简历。

## 手动安装

也可以将本仓库克隆到 Agent 的 Skills 目录。以 Codex 为例：

```bash
git clone https://github.com/panggungunvibe/atutun-resume-helper.git ~/.codex/skills/atutun-resume-helper
```

重新打开 Codex 后，上传简历并输入：

```text
$atutun-resume-helper 帮我诊断并修改这份简历
```

> 不同 Agent 的 Skill 安装目录和调用方式可能不同；Agent 需要具备读取简历文件和生成 Word 文档的能力。

## 文件结构

```text
atutun-resume-helper/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── assets/
│   └── resume-output-example.png
└── references/
    └── diagnosis-template.md
```

## 许可证

[MIT License](LICENSE)
