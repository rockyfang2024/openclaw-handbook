# 第五章：创建 Skill

**目标：打造属于你自己的 Hermes 能力扩展**

***

## 1. Skill 是什么？

Skill = Agent 的能力扩展包。

类比：手机 App。Hermes 是手机，Skill 就是各种 App（天气、邮件、日历...）。

内置 Skill 示例：

| Skill | 用途 |
| ----- | ---- |
| `xthink` | 记录思考想法 |
| `xfupan` | 复盘记录 |
| `xbook` | 书架/读书记录 |
| `xlog` | 每日完成记录 |
| `xdaoli` | 道理金句摘录 |
| `xinvest` | 投资逻辑记录 |
| `xmei` | 生活美学记录 |
| `xzili` | 自我管理/目标追踪 |
| `xtodo` | 待做清单/愿望 |

***

## 2. 使用内置 Skill

直接在对话中触发，例如：

- `xthink 每分钟都要完成自我迭代`
- `xfupan 今天完成了xxx`
- `xbook 苹果之道 大卫·波格`

Agent 会自动将内容保存到对应文件。

***

## 3. 创建自定义 Skill

在 `~/.hermes{N}/skills/` 目录下创建 Skill 文件：

```markdown
# SKILL.md

## 触发词
`每日计划` + 计划内容

## 行为
将计划按日期保存到 ~/notes/plans/{date}.md
```

***

## ✅ 本章小结

* ✅ 理解了 Skill 是什么
* ✅ 学会了使用内置 Skill
* ✅ 了解了如何创建自定义 Skill

***

## ➡️ 下一步

[第六章：多 Agent 协作](06-配置多Agent-HERMES.md)
