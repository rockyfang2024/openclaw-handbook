# 第五章：创建 Skill

**目标：开发你的第一个自定义 Skill**

---

## 1. Skill 是什么？

Skill = Agent 的能力扩展包。

类比：手机 App。OpenClaw 是手机，Skill 就是各种 App（天气、邮件、日历...）。

---

## 2. Skill 目录结构

```
~/.openclaw/skills/my-skill/
├── SKILL.md          # Skill 定义文件（必须）
└── scripts/
    └── main.py       # 实际执行的脚本
```

---

## 3. 实战：天气查询 Skill

**第一步：创建目录**
```bash
mkdir -p ~/.openclaw/skills/weather/scripts
```

**第二步：编写 SKILL.md**
```bash
nano ~/.openclaw/skills/weather/SKILL.md
```

```markdown
# 天气查询 Skill

## 描述
查询任意城市的实时天气

## 触发词
- "天气"
- "查天气"
- "{城市}天气"

## 执行脚本
scripts/weather.py
```

**第三步：编写脚本**
```bash
nano ~/.openclaw/skills/weather/scripts/weather.py
```

```python
#!/usr/bin/env python3
import sys
import urllib.request
import json

def get_weather(city):
    url = f"https://wttr.in/{city}?format=j1"
    try:
        with urllib.request.urlopen(url) as response:
            data = json.loads(response.read().decode())
            current = data['current_condition'][0]
            temp = current['temp_C']
            desc = current['weatherDesc'][0]['value']
            return f"{city}今天天气：{desc}，温度 {temp}°C"
    except Exception as e:
        return f"查询失败：{str(e)}"

if __name__ == "__main__":
    city = sys.argv[1] if len(sys.argv) > 1 else "北京"
    print(get_weather(city))
```

**第四步：赋予权限**
```bash
chmod +x ~/.openclaw/skills/weather/scripts/weather.py
```

---

## 4. 验证 Skill

```bash
# 重启 OpenClaw
openclaw gateway restart

# 查看 Skill 是否加载
openclaw skills list

# 测试脚本
python3 ~/.openclaw/skills/weather/scripts/weather.py 北京
```

对 Bot 说「北京天气」，应该回复天气信息。

---

## 5. 调试技巧

| 命令 | 作用 |
|------|------|
| `openclaw skills list` | 查看已加载的 Skill |
| `openclaw skills reload <name>` | 重新加载 Skill |
| `openclaw gateway logs \| grep <skill>` | 查看 Skill 日志 |

---

## ✅ 本章小结

- ✅ 理解了 Skill 原理
- ✅ 掌握了 Skill 目录结构
- ✅ 开发了天气查询 Skill

---

## ➡️ 下一步

[第六章：配置多 Agent](./06-配置多Agent/)
