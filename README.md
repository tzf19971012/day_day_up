# day_day_up

研究讨论、实验结论与任务进度的每日记录。

每篇日报先列当天最关键的 3～5 个点，再记录讨论细节、证据、待验证假设和任务状态。实验的“准备完成”“进程启动”“完成更新”“效果验证”分别记录。

- [2026-11-13：跨日整理云道 OpenVLA 与 U-self 权重交付](daily/2026-11-13.md)
- [2026-11-12：RGB latent 深度恢复的逻辑与验证](daily/2026-11-12.md)
- [11 月 11 日实验结果汇报](reports/2026-11-11-experiment-results.md)
- [RGB projection loss 分析](reports/2026-11-12-projection-rgb-loss.md)
- [多视角＋DiT 深度 decoder 续训至 20000 步的收益](reports/2026-11-12-wan-depth-continue20k.md)
- [反思：从 Wan RGB latent 恢复深度](reflections/2026-11-12-wan-latent-depth.md)
- [2026-11-11：研究主线、深度恢复实验与 UAV 训练](daily/2026-11-11.md)
- [日报模板](templates/daily.md)

只提交整理后的文档与必要的实验摘要，不提交原始对话、凭据、模型权重或数据缓存。记录范围以实际可读取的会话与日志为准。

## 每日执行

本机定时任务默认每天北京时间 23:00 调用 `scripts/daily_report.py`。脚本读取本机可用的 Codex 用户／最终回复记录和配置的服务器状态，按模板生成日报、创建本地提交并尝试推送 `main`。通过官方支持的 [Codex 非交互模式](https://learn.chatgpt.com/docs/non-interactive-mode) 生成整理文本。

运行依赖这台 Mac、Codex 登录、代理网络及 GitHub Git 认证。其他设备未同步的对话无法覆盖。原始输入与执行日志只保存在忽略提交的 `.local/` 中；推送失败会保留本地文档和提交，并在 `.local/status.json` 写明失败状态。

首篇日报已人工整理并成功推送到 `main`。此前的 Git 登录问题已解决。定时任务按每天北京时间 23:00 执行；2026-11-11 首次自动整理与推送已有成功回执。
