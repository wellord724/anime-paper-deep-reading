# anime-paper-deep-reading

面向 Codex 的双语论文精读 skill。将论文 PDF、链接或材料整理成可追溯的中文与英文 Markdown，以及可切换语言的离线交互 HTML。

## 能力

- 解释背景、问题、贡献、方法、实验与局限，回答八个研究问题。
- 使用米白纸面、青绿重点的阅读风格，提供机制探索、分步图解与证据比较。
- 中英文切换保留阅读位置、参数与播放状态。
- 要求数学公式采用专业 LaTeX，并在 HTML 中实际渲染；数学资源须离线自包含。
- 写作强调具体机制、来源与条件，减少空泛评价和套话。

这是 agent 指令与模板包，不是独立的论文解析程序。实际能力取决于运行 agent 可用的 PDF、检索与浏览器工具。模板提供可运行的双语交互示例；生成正式报告时，agent 需要替换论文内容并按规范配置离线数学渲染。模板示例不是完整精读报告。

## 安装

将本仓库完整复制到 Codex 用户 skills 目录，文件夹名为 `anime-paper-deep-reading`。默认位置为 `~/.codex/skills/anime-paper-deep-reading`；若设置了 `CODEX_HOME`，使用其下的 `skills` 目录。

Windows PowerShell（目标目录尚不存在时）：

```powershell
git clone https://github.com/wellord724/anime-paper-deep-reading.git "$env:USERPROFILE\.codex\skills\anime-paper-deep-reading"
```

macOS / Linux（目标目录尚不存在时）：

```sh
git clone https://github.com/wellord724/anime-paper-deep-reading.git ~/.codex/skills/anime-paper-deep-reading
```

私有仓库需要有访问权限的 GitHub 账户。已有同名 skill 时，先保留本地修改，再选择更新方式。安装后重新载入 skills 或开始新的 Codex 会话。

## 使用

```text
$anime-paper-deep-reading 精读 Attention Is All You Need，生成中英文报告和离线交互页面。
```

也可以附上 PDF，或提供论文链接。默认交付：

```text
paper_report.zh.md
paper_report.en.md
paper_report.html
```

## 文件

| 文件 | 作用 |
| --- | --- |
| SKILL.md | 入口、工作原则与交付要求 |
| REFERENCE.md | 双语、视觉、交互与数学排版规范 |
| EXAMPLES.md | 使用与写作示例 |
| agents/openai.yaml | Codex 展示信息与默认提示 |
| templates/anime_report_template.html | 双语交互视觉基准 |

## English

A Codex skill for source-grounded research-paper reading. It produces Chinese and English Markdown notes plus a bilingual, offline interactive HTML report. The workflow covers methods, evidence, limitations and eight research questions, with a paper-and-teal visual style and professional LaTeX requirements.

Clone the complete repository into your Codex user skills directory and invoke `$anime-paper-deep-reading` with a paper title, link or PDF. Private-repository access requires an authorized GitHub account. This is an instruction-and-template package, not a standalone application; generation uses the host agent's tools. The interactive template is a teaching example, and the agent must adapt its content and configure offline math rendering for a full report.
