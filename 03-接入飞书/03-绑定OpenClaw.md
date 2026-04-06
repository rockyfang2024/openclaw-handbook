# 3.3 绑定 OpenClaw

**把飞书应用和 OpenClaw 对接起来**

---

## 📝 配置 Webhook 事件

在飞书开放平台：

1. 进入应用 → 事件与回调 → 请求地址配置
2. 填写事件订阅 URL：
   ```
   https://你的服务器IP:18789/feishu/webhook
   ```
3. 点击保存

---

## ⚙️ 配置 OpenClaw 飞书插件

在服务器上编辑配置：

```bash
nano ~/.openclaw/config.yaml
```

添加飞书配置：

```yaml
plugins:
  feishu:
    enabled: true
    app_id: "cli_xxxxxxxxxxxxxx"
    app_secret: "xxxxxxxxxxxxxxxxxxxxxxxx"
    bot_name: "我的AI助手"
```

---

## 🌐 配置公网访问（重要）

飞书需要回调 URL 是公网可访问的，有两种方案：

**方案 A：配置公网 IP + 防火墙（推荐）**

确保服务器端口 18789 对外开放：

```bash
# 在服务器上测试端口是否通
curl -v http://你的服务器IP:18789/health
```

**方案 B：使用 ngrok 内网穿透（测试用）**

```bash
# 安装 ngrok
npm install -g ngrok
ngrok http 18789
```

会得到一个公网地址，填入飞书的回调 URL。

---

## ➡️ 下一步

[3.4 测试对话](./04-测试对话.md)
