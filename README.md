# Wendao Persona Skills

问道（Wendao）名人导师的 **女娲蒸馏 Skill** 独立仓库。与 [wendao](https://github.com/ChaosJu/wendao) 应用代码分离，仅存放 `SKILL.md` 与调研 sidecar。

BFF 通过环境变量 `OPENCLAW_SKILLS_DIR` 指向本仓库克隆目录，按 `personas.json` 中的 `skillDir` 加载对应 `SKILL.md`。

## 目录结构

```text
wendao-skills/                    # OPENCLAW_SKILLS_DIR 指向此处
  li-xiaolai-perspective/
    SKILL.md                      # 运行时注入 system prompt
    references/research/          # 调研 sidecar，不注入 prompt
```

## 部署

```bash
git clone https://github.com/ChaosJu/wendao-skills.git /root/.openclaw/workspace/skills
# 或任意路径，在 wendao server/.env 中设置：
# OPENCLAW_SKILLS_DIR=/path/to/wendao-skills
```

## 与 wendao 的配合

新增一位导师需要两处改动：

| 仓库 | 改动 |
|------|------|
| **wendao-skills**（本仓库） | 添加 `{skillDir}/SKILL.md` |
| **wendao** | `server/src/data/personas.json`、`miniprogram/utils/persona-profiles.js` |

## 已收录

| skillDir | 人物 | 说明 |
|----------|------|------|
| `li-xiaolai-perspective` | 李笑来 | [女娲 · nuwa-skill](https://github.com/alchaincyf/nuwa-skill) 蒸馏，9 本著作 + 媒体调研 |

## License

Private — 个人项目
