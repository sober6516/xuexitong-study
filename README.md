# 学习通作业助手

从学习通网页自动收录题目、选项和可见批改信息，整理成适合平时学习和期末突击的零基础讲义。按章解释概念，带你做例题，再逐题讲解，最后给出答案速查和考前重点。

## 两种用法

| 用法 | 能做什么 |
| --- | --- |
| 自动答题＋讲义 | 从收件箱找待做作业，读题、解答、填选、核对并暂存。适合复习的作业在本轮答完后集中生成讲义。 |
| 只收题做讲义 | 指定科目，可一起收录以前做过的作业。网页只读，答案和逐题解析写进讲义。 |

只说「用学习通技能」时，助手会给出以上两个选项，回复 **1** 或 **2** 即可。也可以在请求里直接指定用法。后续需要确定科目、是否收录历史作业或是否出讲义时，优先提供可点选的选项，也支持回复编号。

**示例**

- 「从学习通收件箱找仪器分析的待做作业，答完暂存，再给我一份零基础讲义。」
- 「只收录分子生物学和仪器分析的题。之前做过的也收录，只生成讲义。」

## 安装与使用

下载仓库里的 `SKILL.md`，放在名为 `xuexitong-study` 的目录里。

| 使用环境 | 放置位置 |
| --- | --- |
| Claude Code | 项目的 `.claude/skills/xuexitong-study/SKILL.md`，或个人目录的 `~/.claude/skills/xuexitong-study/SKILL.md` |
| GitHub Copilot | 项目的 `.github/skills/xuexitong-study/SKILL.md` |
| 其他兼容 Agent Skills 的工具 | 放入对应工具的技能目录或使用其导入功能 |
| 支持附件或自定义提示词的聊天助手 | 附上 `SKILL.md` 或粘贴其正文，说明要使用哪种模式 |

放好后，直接描述要处理的课程和用法。支持按名称调用的工具可用技能名 `xuexitong-study`。

## 运行条件

- **网页收题与填选**需要 Agent 能访问你已登录的学习通页面。只有网页读取能力时，可以收题和整理。填选需要浏览器交互工具。
- **附件整理**适用于没有浏览器工具的环境。提供题目截图、PDF、文本或其他可读材料即可。
- **Word 输出**需要宿主具备文档生成及文件交付能力。只支持文本时可以生成同结构的 Markdown 讲义。
- 只读模式不会改动学习通作答。自动答题默认暂存，正式提交需明确授权。

规范与安装文档

- [Agent Skills 规范](https://agentskills.io/specification)
- [Claude Code 技能文档](https://code.claude.com/docs/en/skills)
- [GitHub Copilot 技能文档](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/add-skills)
