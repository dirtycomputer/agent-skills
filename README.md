# Agent Skills

个人技能主仓库，集中保存可复用的研究与智能体工作流程。每个技能以独立目录维护，完整保留 `SKILL.md` 及其引用的资源。

## 技能目录

| 技能 | 用途 | 入口 |
| --- | --- | --- |
| `llm-paper-screening` | 广泛检索、筛选和排序 LLM / Agent RL 研究，核查证据，并规划迁移与最小验证 | [SKILL.md](skills/llm-paper-screening/SKILL.md) |

`llm-paper-screening` 包含 [从论文筛选到最小验证](skills/llm-paper-screening/references/transfer.md)。两个文件均来自用户提供的原文，仅整理 Markdown 转义、换行与元数据格式。

## 使用与维护

1. 在本仓库维护技能主版本；每个技能的 `SKILL.md` 使用包含 `name` 和 `description` 的 YAML frontmatter。
2. 安装时使用完整技能目录，保留 `references/`、`scripts/`、`assets/` 等已有资源的相对路径。
3. 根据工具及使用范围安装到对应位置：

| 工具 | 用户级目录 | 项目级目录 |
| --- | --- | --- |
| Codex CLI | `~/.agents/skills/` | `.agents/skills/` |
| Claude Code | `~/.claude/skills/` | `.claude/skills/` |

更新本仓库后，需更新各环境已安装的技能副本。ChatGPT 个人技能需另行导入或更新；保存在 GitHub 中不等于已安装到 ChatGPT。

## 新增技能

使用 `skills/<skill-name>/SKILL.md` 作为入口，按需增加资源文件，并在上方技能目录登记。保持名称唯一，提交前检查元数据及所有相对引用路径。
