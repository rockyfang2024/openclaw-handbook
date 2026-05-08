# 第四章：创建定时任务

**目标：让 Hermes Agent 按时提醒你做事**

***

## 最简单的方式

直接跟 Agent 说：**几点提醒我做什么事**，即可创建一个定时任务。

例如：每天晚上 21:00，提醒你锻炼身体。

***

## 使用 Hermes Cron

Hermes 内置 Cron 系统，支持定时任务：

```bash
# 创建定时任务
hermes cron create "0 9 * * *" "每天早上9点提醒我今日计划"
```

查看定时任务：

```bash
hermes cron list
```

***

## ✅ 本章小结

* ✅ 学会了最简方式：告诉 Agent「几点提醒我做什么」
* ✅ 了解了 Hermes Cron 定时任务

***

## ➡️ 下一步

[第五章：创建 Skill](05-创建Skill-HERMES.md)
