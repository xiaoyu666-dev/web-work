# Web 课程作业技能

按课程知识点完成 HTML、CSS、JavaScript 作业的中文 Codex Skill。

每次提供作业要求和课程链接，技能先读取资料、确认可使用的知识点，再实现和检查代码，最后在对话中交付可直接复制的答案、代码说明与知识点依据。

## 功能

- 以本次课程材料确定技术范围，不自动引入框架或超纲语法。
- 保留老师要求的结构、文件名和写法。
- 默认不添加源码注释，说明直接写在对话中；老师明确要求注释时按要求处理。
- CSS 使用多行排版，每条声明单独一行，缩进 4 个空格。
- 直接输出完整代码块，不以下载链接或省略片段代替代码。
- 文字题以可直接复制的中文段落作答，默认不用表格。
- 只交付题目要求的提交文件，不自动附加说明文档、压缩包或预览图。
- 链接打不开或要求与课程范围冲突时，说明缺口，请用户补充资料，不编造已读内容。

## 安装

### 使用 Skill Installer

将下面这段话直接发送给 Codex：

```text
请使用 $skill-installer，从 https://github.com/xiaoyu666-dev/web-work 安装 skills/web-course-homework 目录中的技能。
```

### 手动安装

从本仓库复制完整的 `skills/web-course-homework` 文件夹到项目中的 `.agents/skills/`，形成：

```text
你的项目/
└── .agents/
    └── skills/
        └── web-course-homework/
            ├── SKILL.md
            └── agents/
                └── openai.yaml
```

需要对个人所有项目生效时，可放到 `~/.agents/skills/web-course-homework/`。安装后若未显示，重新启动 Codex；不同宿主版本的技能目录可能不同，以宿主说明为准。

安装及目录依据：[OpenAI 官方技能文档](https://learn.chatgpt.com/docs/build-skills)。

## 使用

安装后，在 Codex 中发送：

```text
请使用 $web-course-homework 完成本次网页设计作业。

课程知识点链接：在这里粘贴课程链接。

作业要求：在这里粘贴完整题目、评分标准和提交格式。

素材：提供老师给出的原始代码、文件或参考图。
```

技能适用于受到课程范围限制的网页作业，不用于无课程限制的普通网站开发。它不会自动发布网站或替用户提交到教学平台。

## 交付示例

如果题目只要求提交 `notice.css`，回复会先给出完整 CSS 代码块，再用中文说明关键代码及对应课程知识点。需要文件时只提供该 CSS 文件，其他验证材料不作为作业附件。

如果题目还要求回答 GET 与 POST 的区别，会同时提供可直接复制的文字答案，不要求用户再次索要。

## 仓库结构

```text
skills/web-course-homework/SKILL.md
skills/web-course-homework/agents/openai.yaml
README.md
LICENSE
```

这是一个仅包含工作流指令的技能，没有运行脚本、第三方依赖或内置课程内容。读取课程链接需要宿主具备浏览能力，运行检查需要相应的本地工具。

## 修改

工作流规则在 `skills/web-course-homework/SKILL.md`，界面名称与默认提示在 `skills/web-course-homework/agents/openai.yaml`。修改后可通过你本地 Skill Creator 提供的校验工具检查格式。

## 许可

采用 [MIT License](LICENSE)，允许使用、修改和分发。课程资料不包含在本仓库中，相关资料的权利属于其原权利人。
