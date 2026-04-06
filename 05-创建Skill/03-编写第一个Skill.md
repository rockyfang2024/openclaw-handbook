# 5.3 编写你的第一个 Skill

**动手开发一个天气查询 Skill**

---

## 📝 步骤一：创建 Skill 目录

```bash
mkdir -p ~/.openclaw/skills/weather/scripts
```

---

## 📝 步骤二：编写 SKILL.md

```bash
nano ~/.openclaw/skills/weather/SKILL.md
```

填入：

```markdown
# 天气查询 Skill

## 描述
查询任意城市的实时天气

## 触发词
- "天气"
- "查天气"
- "今天多少度"

## 执行脚本
scripts/weather.py
```

---

## 📝 步骤三：编写天气脚本

```bash
nano ~/.openclaw/skills/weather/scripts/weather.py
```

填入：

```python
#!/usr/bin/env python3
import sys
import urllib.request
import json

def get_weather(city):
    # 这里使用 wttr.in 免费 API
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

保存。

---

## 📝 步骤四：赋予执行权限

```bash
chmod +x ~/.openclaw/skills/weather/scripts/weather.py
```

---

## 🧪 测试

```bash
python3 ~/.openclaw/skills/weather/scripts/weather.py 北京
```

输出：`北京今天天气：Sunny，温度 22°C`

---

## ➡️ 下一步

[5.4 实战天气 Skill](./04-实战天气Skill.md)
