# Hermes 教程

> Hermes — 多 Agent 协作的 AI 助手矩阵系统。

***

## 🎯 这本书适合谁？

* 想快速搭建多 Agent 协作系统 的开发者
* 想定制化 AI 能力 的技术爱好者
* 希望搭建 Agent 矩阵（私人助理、投资教练、英语导师...）的进阶用户

***

## 📖 六章学习路径

### [第一章：选购腾讯云服务器](01-选购腾讯云服务器-HERMES.md)

**目标：拥有自己的公网服务器，24小时运行 Hermes**

* 为什么需要云服务器
* 购买流程（腾讯云轻量应用服务器）
* 地域推荐新加坡，系统 Ubuntu 22.04 LTS

***

### [第二章：选购大模型](02-选购大模型-HERMES.md)

**目标：获取 AI 模型 API Key，让 Agent 具备智能**

* 主流模型对比（MiniMax / DeepSeek / Claude / GPT-4）
* 注册 MiniMax（邀请码享 9 折优惠）
* 购买 Plus-极速版 Token Plan（量大管饱，无 token 焦虑）
* 配置 Hermes 使用模型
* 验证配置

***

### [第三章：接入飞书](03-接入飞书-HERMES.md)

**目标：在飞书中与 Hermes Agent 对话，随时随地唤醒 AI**

* 在飞书开放平台创建应用
* 配置权限（事件订阅、长连接）
* 获取 AppID 和 App Secret
* 配置 .env 文件
* 配对连接

***

### [第四章：创建定时任务](04-创建定时任务-HERMES.md)

**目标：让 Hermes Agent 按时提醒你做事**

* 最简方式：跟 Agent 说「几点提醒我做什么事」

***

### [第五章：创建 Skill](05-创建Skill-HERMES.md)

**目标：打造属于你自己的 Hermes 能力扩展**

* Skill 是什么（Agent 的能力扩展包）
* 创建自定义 Skill

***

### [第六章：创建多Agent](06-创建多Agent-HERMES.md)

**目标：搭建分工明确的 Agent 矩阵**（内容待补充）

* 为什么需要多 Agent（一个团队，各司其职）
* 创建新的 Agent 实例
* 飞书开放平台配置
* 配对连接
* 定义 SOUL.md 人设

***

### [FAQ 常见问题](./FAQ.md)

遇到问题？这里有常见问题的解答。

***

## 🚀 快速上手路线

```
选购服务器 → 配置模型 → 接入飞书 → 设置提醒 → 开发Skill → 多Agent → 应用场景 → FAQ
```

***

## 📊 Hermes vs OpenClaw

| | OpenClaw | Hermes |
|--|--|--|
| 定位 | 个人 AI 助手 | Agent 矩阵系统 |
| 多 Agent | 单 Agent | 多 Agent 协作（规划中） |
| 复杂度 | 入门简单 | 配置灵活 |
| 平台 | 飞书为主 | 飞书 + 多平台 |
| 学习曲线 | 平缓 | 稍陡 |

***

## 💰 支持作者

如果这份文档对你有帮助，欢迎打赏：

| 微信 | 支付宝 |
| -- | -- |
| ![](.gitbook/assets/wechat-donate.jpg) | ![](.gitbook/assets/alipay-donate.jpg) |

> 💡 **支持付费手把手教学 & 应用定制配置服务**，扫码联系作者。微信号：rockyfang2024

***

_让 AI 助手从"听说很厉害"到"真的用起来"。_
