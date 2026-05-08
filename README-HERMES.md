# Hermes 教程

> Hermes — 多 Agent 协作的 AI 助手矩阵系统。

***

## 📖 教程目录

### [第一章：认识 Hermes](README-HERMES.md#第一章认识-hermes)

**目标：了解 Hermes 是什么，以及它与 OpenClaw 的区别**

- Hermes 是什么
- 核心概念：Agent、SOUL、config.yaml、.env
- 多 Agent 协作架构

***

### [第二章：选购大模型](README-HERMES.md#第二章选购大模型)

**目标：获取 AI 模型 API Key**

- MiniMax M2.7 配置
- API Key 配置（MINIMAX_CN_API_KEY）
- 验证连接

***

### [第三章：接入飞书](README-HERMES.md#第三章接入飞书)

**目标：在飞书中与 Hermes Agent 对话**

- 在飞书开放平台创建应用
- 配置权限（事件订阅、长连接）
- 获取 AppID 和 App Secret
- 配置 .env 文件
- 配对连接

***

### [第四章：创建 Agent 实例](README-HERMES.md#第四章创建-agent-实例)

**目标：创建你的第一个 Hermes Agent**

- 目录结构说明（~/.hermes{N}/）
- config.yaml 核心配置
- SOUL.md 人设配置
- .env 环境变量
- 启动 Agent
- 配对与授权

***

### [第五章：多 Agent 协作](README-HERMES.md#第五章多-agent-协作)

**目标：搭建分工明确的 Agent 矩阵**

- Agent 分工设计示例
- SOUL 写作指南
- Agent 间隔离与协作

***

### [第六章：Skill 系统](README-HERMES.md#第六章skill-系统)

**目标：扩展 Agent 能力**

- Skill 是什么
- 内置 Skill（xthink、xfupan、xbook...）
- 自定义 Skill

***

### [第七章：定时任务](README-HERMES.md#第七章定时任务)

**目标：让 Agent 自动执行任务**

- Cron 配置
- 定时推送

***

---

## 🚀 快速上手

### 1. 创建 Agent 实例

```bash
mkdir -p ~/.hermes7/{bin,cache,cron,logs,memories,platforms,sessions,skills,sandboxes}
```

### 2. 配置 config.yaml

```yaml
model:
  default: MiniMax-M2.7
  provider: minimax-cn
  base_url: https://api.minimaxi.com/anthropic
```

### 3. 配置 .env

```bash
FEISHU_APP_ID=cli_xxxxxxxx
FEISHU_APP_SECRET=xxxxxxxx
MINIMAX_CN_API_KEY=sk-xxxxxxxx
```

### 4. 配置 SOUL.md

定义 Agent 的人设、行为规则、语言风格。

### 5. 启动

```bash
cd ~/.hermes7
HERMES_HOME=~/.hermes7 python -m hermes_cli.main gateway run
```

### 6. 配对

在飞书给 bot 发消息 → 获取配对码 → 运行：

```bash
hermes pairing approve feishu <CODE>
```

---

## 📁 目录结构说明

```
~/.hermes7/
├── config.yaml     # Agent 配置（模型、工具、行为）
├── .env            # 环境变量（飞书 AppID/Secret、API Key）
├── SOUL.md         # Agent 人设定义
├── bin/            # 启动脚本
├── cache/          # 缓存
├── cron/           # 定时任务
├── logs/           # 日志
├── memories/       # 记忆存储
├── platforms/      # 平台配置
├── sessions/       # 会话存储
├── skills/         # 能力扩展
└── sandboxes/      # 沙盒
```

---

## 🔗 相关资源

- [OpenClaw 教程](README-OPENCLAW.md)
- [Hermes GitHub](https://github.com/NousResearch/hermes-agent)
