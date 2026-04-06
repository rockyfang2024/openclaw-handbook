# 1.2 安装 OpenClaw

**预计耗时：2 分钟**

---

## 🚀 快速安装（一条命令）

```bash
npm install -g openclaw
```

或者用 pnpm（更快）：

```bash
pnpm add -g openclaw
```

---

## ⚙️ 初始化配置

安装完成后，执行初始化命令：

```bash
openclaw init
```

这个命令会：
1. 创建配置文件 `~/.openclaw/`
2. 生成默认的 `workspace` 目录
3. 提示你进行首次配置

---

## ▶️ 启动 OpenClaw

```bash
openclaw gateway start
```

看到类似输出即表示启动成功：

```
🚀 OpenClaw Gateway is running
📍 http://localhost:18789
```

---

## 🌐 访问控制台

打开浏览器，访问：

```
http://localhost:18789
```

你将看到 OpenClaw 的管理界面。

> 💡 **提示：** 首次使用需要配置 API Key，具体见下一节。

---

## 🔧 常用命令

| 命令 | 作用 |
|------|------|
| `openclaw gateway start` | 启动服务 |
| `openclaw gateway stop` | 停止服务 |
| `openclaw gateway status` | 查看状态 |
| `openclaw -v` | 查看版本 |

---

## ❓ 常见问题

**Q：启动报 `port already in use`？**
→ 端口 18789 被占用，执行：
```bash
openclaw gateway stop
openclaw gateway start
```

**Q：提示需要 API Key？**
→ 需要配置你的 AI 模型 API Key，见 [1.3 第一个 Agent](./03-第一个Agent.md)。

---

## ➡️ 下一步

[1.3 配置 API Key 并创建第一个 Agent](./03-第一个Agent.md)
