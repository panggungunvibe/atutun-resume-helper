# 改简历 Skill

面向中文求职者的简历诊断与改写工作流。

1、用户：提供简历，格式不限（PDF、图片或文字均可）

2、AI：

（1）确认用户情况：校招／社招、是否有目标岗位、目标JD；

（2）检查原简历是否通过修改的门槛；

（3）给出诊断结果 + 一版重构后的简历（Word格式）。

## 1. 如何安装这个 Skill

把下面这句话直接发给你的 Agent：

> 帮我安装这个skill：[https://github.com/panggungunvibe/atutun-resume-helper](https://github.com/panggungunvibe/atutun-resume-helper)

Agent 会根据自己的 Skill 安装方式完成安装。

## 2. 这个 Skill 怎么用

### 第一步：上传自己的简历

向 Agent 上传需要修改的简历，可以是：

- PDF 简历；
- Word 简历；
- 简历截图或整理好的文字内容。

然后告诉它：

```text
帮我诊断并修改这份简历
```

### 第二步：回答求职信息

Agent 会先问两个问题：

1. 你是参加校招，还是社招？
2. 你的目标岗位是什么？

求职方向越具体，简历修改得越准确。如果暂时没有明确岗位，也可以回答“通用产品经理”等大致方向。

回答后，Agent 会在下一轮询问你有没有目标 JD。如果有，可以发送职位截图、招聘链接或文字内容；如果没有，Agent 会按照通用岗位要求进行诊断。

例如可以这样回答：

```text
我是社招，想找 B 端 SaaS 产品经理，工作经验 3 年。
```

### 第三步：获得诊断和最终版简历

Agent 会先在对话中告诉你：

1. 一份适合目标岗位的简历应该采用什么结构；
2. 你在每个结构下面目前存在什么问题；
3. 建议如何修改。

随后，它会基于以上分析生成一份修改后的 `.docx` 简历。Word 文件只保留最终简历正文，不会混入诊断过程和修改建议。

如果原简历中没有任何可以提取的工作、实习或实践项目，Skill 会停止改写并要求先补充真实经历，不会生成一份只有占位内容的空壳 Word。

![简历诊断与最终 Word 产出示例](assets/resume-output-example.png)

简历中缺少但值得补充的信息会使用 `XXX` 占位，并通过黄色高亮或红色字体提醒。Skill 不会编造工作经历、项目数据或业务成果。

## 3. 文件结构

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

本项目采用 [MIT License](LICENSE)。
