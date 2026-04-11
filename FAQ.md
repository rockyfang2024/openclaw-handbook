# FAQ 常见问题

**遇到问题？先来这里看看**

---

## Q1：OpenClaw 支持哪些模型？

支持 MiniMax、DeepSeek、Claude、GPT-4 等主流大模型。国内推荐使用 **MiniMax**，中文效果好、价格实惠、响应快。

---

## Q2：服务器配置太低怎么办？

推荐 **2核2G** 起，如果运行多个 Agent，建议 **4核4G** 或更高。腾讯云轻量应用服务器性价比高，可随时升级配置。

---

## Q3：定时任务没有触发怎么办？

1. 检查 cron 表达式是否正确
2. 使用**本地 cron + Python** 方案，比龙虾内置定时任务更稳定
3. 查看日志：`openclaw gateway logs | grep cron`

---

## Q4：飞书机器人没有响应？

按顺序排查：
1. 检查 OpenClaw 配置页面 → 通道 → 飞书是否已授权
2. 确认飞书应用已发布（版本管理 → 发布）
3. 检查 OpenClaw 运行状态：`openclaw gateway status`

---

## Q5：如何让多个 Agent 协作？

在飞书开放平台创建多个应用 → 每个应用对应一个 Agent → 通过不同飞书群或私聊区分。参考第六章配置流程。

---

## Q6：API Key 泄露了怎么办？

立即到 MiniMax 平台重新生成 API Key，并更新 OpenClaw 配置。同时检查账号是否有异常调用记录。

---

## Q7：如何升级 OpenClaw 版本？

```bash
openclaw upgrade
openclaw gateway restart
```

---

## Q8：还有其他问题？

欢迎扫码联系作者获取支持：

> 💡 **支持付费手把手教学 & 应用定制配置服务**，扫码联系作者。微信号：rockyfang2024
