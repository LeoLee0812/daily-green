<div align="center">

# 🌱 daily-green · 每日绿格子日志

**由 Claude Code 云端定时任务每天自动提交一条打卡日志，为 GitHub 贡献图持续点亮绿格子。**

![Claude Code](https://img.shields.io/badge/Claude%20Code-云端定时任务-D97757?style=flat-square&logo=claude&logoColor=white)
![每日提交](https://img.shields.io/badge/每日提交-自动化-brightgreen?style=flat-square)
![Markdown](https://img.shields.io/badge/日志格式-Markdown-000000?style=flat-square&logo=markdown&logoColor=white)

</div>

## ✨ 简介

一个极简的每日打卡日志仓库：Claude Code 的云端定时任务（scheduled cloud agent）每天自动运行一次，往 `log.md` 追加当天的打卡记录并提交推送。仓库里没有任何脚本或工作流文件——所有自动化逻辑都跑在 Claude Code 云端，本仓库只负责承载日志内容和提交历史。

## 🚀 功能特性

- **零脚本零依赖** — 仓库里只有一个 Markdown 日志文件，没有代码、没有 CI 配置
- **云端全自动** — 定时任务由 Claude Code 云端执行，不占用本地任何资源
- **贡献图友好** — 提交以本人验证邮箱署名，每天稳定为贡献图增加一格绿
- **历史可追溯** — 每天一行日志 + 一条 commit，打卡记录一目了然

## ⚙️ 工作原理

```
Claude Code 云端定时任务（每天触发一次）
        │
        ▼
  往 log.md 追加一行「YYYY-MM-DD 自动打卡」
        │
        ▼
  git commit -m "chore: YYYY-MM-DD 每日打卡" → git push
        │
        └─▶ GitHub 贡献图 +1 格绿  ✅
```

与 [daily-checkin](https://github.com/LeoLee0812/daily-checkin)（GitHub Actions 方案）互为姊妹项目：一个走 GitHub 原生 Actions，一个走 Claude Code 云端定时任务，两条链路各自独立打卡。

## ⚡ 快速开始

想看打卡记录，直接打开 [`log.md`](./log.md)；想看每日提交历史，查看仓库的 [Commits](../../commits) 页面即可。

> 注意：本仓库每天会有机器人定时提交。如果你 fork 后想本地改动再推回，记得先 `git pull --rebase`。

## 📁 项目结构

| 文件 | 作用 |
|------|------|
| `log.md` | 每日打卡日志，云端定时任务每天追加一行 |
| `README.md` | 本说明文件 |

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=LeoLee0812/daily-green&type=Date)](https://www.star-history.com/#LeoLee0812/daily-green&Date)
