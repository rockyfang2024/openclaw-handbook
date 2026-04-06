# 1.3 第一个 Agent

**预计耗时：3 分钟**

---

## 🎯 你会学到

- 如何配置 API Key
- 如何创建一个 Agent
- 如何与 Agent 对话

---

## 第一步：获取 API Key

OpenClaw 支持多种 AI 模型，这里以 **MiniMax** 为例：

1. 注册 [MiniMax Platform](https://platform.minimaxi.com/)
2. 进入控制台 → 创建 API Key
3. 复制保存你的 API Key

> 💡 **支持的模型：** OpenAI、Claude、MiniMax、DeepSeek 等，详见 [官方文档](https://docs.openclaw.ai)。

---

## 第二步：配置 API Key

编辑配置文件：

```bash
nano ~/.openclaw/config.yaml
```

填入以下内容：

```yaml
providers:
  minimax:
    api_key: "你的API Key"
    model: "MiniMax-M2"

default_provider: minimax
```

保存退出（Ctrl+X → Y → Enter）。

---

## 第三步：创建你的第一个 Agent

在终端执行：

```bash
openclaw agent create --name "我的助手" --model minimax
```

成功后会输出类似：

```
✅ Agent 创建成功！
📝 Agent ID: agent-001
📝 Agent 名称: 我的助手
```

---

## 第四步：与 Agent 对话

启动对话：

```bash
openclaw chat --agent agent-001
```

然后直接输入你的问题：

```
你好，你是谁？
```

你的第一个 Agent 应该会回答你。

---

## 📁 目录结构

创建 Agent 后，OpenClaw 会生成以下文件：

```
~/.openclaw/workspace/
├── SOUL.md          # Agent 的角色设定
├── AGENTS.md        # 工作区说明
└── memory/          # 记忆存储目录
```

---

## 🎉 恭喜！

你已成功：
- ✅ 安装 OpenClaw
- ✅ 配置 API Key
- ✅ 创建第一个 Agent

---

## ➡️ 下一步

[第二章：平台接入](./02-平台接入/) — 把 Agent 绑定到飞书或微信
