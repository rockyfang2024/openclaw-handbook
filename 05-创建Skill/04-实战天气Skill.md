# 5.4 实战天气 Skill

**完整走通 Skill 开发流程**

---

## ✅ 完整验证

1. 重启 OpenClaw：
```bash
openclaw gateway restart
```

2. 对 Bot 说：「北京天气」

3. Bot 应该回复：「北京今天天气：xxx，温度 xx°C」

---

## 🛠️ Skill 调试技巧

**查看 Skill 加载状态：**
```bash
openclaw skills list
```

**查看日志：**
```bash
openclaw gateway logs | grep weather
```

**重新加载 Skill：**
```bash
openclaw skills reload weather
```

---

## 💡 进阶：传入更多参数

修改 SKILL.md，支持更多表达：

```markdown
## 触发词
- "天气"
- "天气 {城市}"
- "查 {城市} 天气"
```

---

## 🎉 本章小结

恭喜，你已经：
- ✅ 理解了 Skill 原理
- ✅ 掌握了 Skill 目录结构
- ✅ 开发了第一个天气 Skill

---

## ➡️ 下一步

[第六章：配置多 Agent](../06-配置多Agent/) — 搭建多角色 Agent 矩阵
