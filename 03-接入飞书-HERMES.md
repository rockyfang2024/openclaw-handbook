# 第三章：接入飞书

**目标：在飞书中与 Hermes Agent 对话，随时随地唤醒 AI**

***

## 1. 在飞书开放平台创建应用

1. 打开 [飞书开放平台](https://open.feishu.cn/app)
2. 点击「创建企业自建应用」
3. 填写应用名称（如「Hermes私人助理」）
4. 获取 **AppID** 和 **App Secret**

![创建飞书应用](.gitbook/assets/06-feishu-app-create.jpg)

***

## 2. 配置权限

进入「权限管理」，开通以下权限：

- `im:chat:readonly` / `im:chat` / `im:chat:read` — 读取聊天信息
- `im:message:send_as_bot` — 发送消息
- `application:application:self_manage` — 应用管理

![配置飞书权限](.gitbook/assets/06-feishu-permission-import.jpg)

***

## 3. 配置事件订阅

进入「事件订阅」，选择 **使用长连接接收事件**（WebSocket 模式）：

![事件订阅配置](.gitbook/assets/06-feishu-event-longconn.jpg)

添加事件：

- `im.message.receive_v1` — 接收消息

***

## 4. 配置 .env 文件

在 `~/.hermes{N}/.env` 中配置：

```bash
FEISHU_APP_ID=cli_xxxxxxxx
FEISHU_APP_SECRET=xxxxxxxx
FEISHU_CONNECTION_MODE=websocket
```

***

## 5. 启动并配对

启动 Agent：

```bash
cd ~/.hermes{N}
HERMES_HOME=~/.hermes{N} python -m hermes_cli.main gateway run
```

在飞书给 bot 发一条消息，获取配对码，然后在服务器执行：

```bash
hermes pairing approve feishu <配对码>
```

配对成功后即可开始对话。

***

## ✅ 本章小结

* ✅ 在飞书开放平台创建应用
* ✅ 配置权限和事件订阅
* ✅ 配置 .env 文件
* ✅ 启动 Agent 并完成配对

***

## ➡️ 下一步

[第四章：创建 Agent 实例](04-创建Agent-HERMES.md)
