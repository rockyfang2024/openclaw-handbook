# 6.2 创建多个 Agent

**在 OpenClaw 中运行多个 Agent**

---

## 📝 创建第二个 Agent

```bash
openclaw agent create \
  --name "顾问" \
  --id agent-consultant \
  --model minimax
```

成功后会输出：
```
✅ Agent 创建成功！
📝 Agent ID: agent-consultant
📝 Agent 名称: 顾问
```

---

## 📁 每个 Agent 的目录

创建后会在 `~/.openclaw/agents/` 下生成独立目录：

```
~/.openclaw/agents/
├── agent-001/           # 第一个 Agent
│   ├── SOUL.md
│   └── memory/
└── agent-consultant/    # 第二个 Agent
    ├── SOUL.md
    └── memory/
```

---

## ⚙️ 配置不同角色

每个 Agent 有独立的 `SOUL.md`，定义其职责：

```bash
nano ~/.openclaw/agents/agent-consultant/SOUL.md
```

填入角色定义：
```markdown
# 角色：CEO 顾问

你是用户的战略顾问，帮助用户：
- 分析问题本质
- 提供决策建议
- 引导深度思考
```

---

## ➡️ 下一步

[6.3 Agent 角色定义](./03-Agent角色定义.md)
