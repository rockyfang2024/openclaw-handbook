# 5.1 Skill 是什么

**理解 OpenClaw Skill 的核心概念**

---

## 💡 什么是 Skill？

Skill = 技能 = Agent 的能力扩展包。

类比：手机 App。OpenClaw 是手机，Skill 就是各种 App（地图、相机、天气...）。

---

## 🎯 Skill 能做什么？

| 场景 | Skill 示例 |
|------|-----------|
| 查询天气 | 获取实时天气数据 |
| 发送邮件 | 自动发送邮件 |
| 操作日历 | 创建/查询日程 |
| 数据处理 | 读取/写入数据库 |
| 第三方集成 | 接入飞书、腾讯文档 |

---

## 📁 Skill 的结构

```
~/.openclaw/skills/
└── my-skill/
    ├── SKILL.md      # Skill 的说明书
    ├── scripts/      # 脚本目录
    └── README.md     # 可选
```

---

## 🔑 核心文件：SKILL.md

每个 Skill 必须有一个 `SKILL.md`，内容包含：

1. **描述** - Skill 的用途
2. **触发词** - 什么话会触发这个 Skill
3. **执行逻辑** - 如何处理请求

---

## ➡️ 下一步

[5.2 Skill 目录结构](./02-Skill目录结构.md)
