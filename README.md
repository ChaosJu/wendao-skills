# Persona Skills

[女娲 · nuwa-skill](https://github.com/alchaincyf/nuwa-skill) 蒸馏的人物思维框架 Skill 集合。

每个 Skill 包含：
- `SKILL.md` — 核心 prompt（心智模型、决策启发式、表达 DNA）
- `references/research/` — 调研 sidecar（著作精读、时间线、争议等，不注入 prompt）

## 目录结构

```text
li-xiaolai-perspective/
  SKILL.md
  references/research/
    01-writings.md
    01b-writings-more.md
    02-conversations.md
    03-expression-dna.md
    04-external-views.md
    05-decisions.md
    06-timeline.md
```

## 使用方式

### Cursor Agent Skill

将目录复制或软链到 `~/.cursor/skills/`：

```bash
cp -r li-xiaolai-perspective ~/.cursor/skills/
```

重启 Cursor 后在对话中说「用李笑来的视角」即可激活。

### 作为 System Prompt

读取 `SKILL.md` 内容注入 LLM 的 system message 即可，适用于任何兼容 OpenAI API 的服务。

## 已收录

| 目录 | 人物 | 来源 |
|------|------|------|
| `li-xiaolai-perspective` | 李笑来 | 9 本著作原文 + 30+ 条权威媒体 |
| `zone-perspective` | Zone · 交易心理学 | Douglas / Steenbarger / Elder / Kahneman 等 8 位 · 23 个调研源 |

## License

Private — 个人项目
