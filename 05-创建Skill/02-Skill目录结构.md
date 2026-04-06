# 5.2 Skill 目录结构

**了解 Skill 的标准文件结构**

---

## 📁 标准目录结构

```
skill-name/              # Skill 文件夹
├── SKILL.md             # 【必须】Skill 定义文件
├── scripts/             # 脚本目录
│   ├── main.py          # 主脚本
│   └── utils.py         # 工具函数（可选）
└── README.md            # 使用说明（可选）
```

---

## 📝 SKILL.md 示例

```markdown
# 我的天气 Skill

## 描述
查询任意城市的实时天气

## 触发词
- "天气"
- "查一下天气"
- "北京今天多少度"

## 执行逻辑
1. 解析城市名
2. 调用天气 API
3. 返回格式化结果
```

---

## 🛠️ 创建自己的 Skill

```bash
mkdir -p ~/.openclaw/skills/my-first-skill
cd ~/.openclaw/skills/my-first-skill
mkdir scripts
```

---

## ➡️ 下一步

[5.3 编写你的第一个 Skill](./03-编写第一个Skill.md)
