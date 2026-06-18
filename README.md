# Awesome Claude Code 命令大全(中文 · 持续核查)

![Claude Code 命令大全 中文](https://claude.aiso.cool/api/og?type=home)

![已核查](https://img.shields.io/badge/%E5%B7%B2%E6%A0%B8%E6%9F%A5-96%2F102-brightgreen) ![通过来源核验](https://img.shields.io/badge/%E9%80%9A%E8%BF%87%E6%9D%A5%E6%BA%90%E6%A0%B8%E9%AA%8C-100%25-brightgreen) ![锚定](https://img.shields.io/badge/%E9%94%9A%E5%AE%9A-%E5%A4%9A%E7%89%88%E6%9C%AC-orange) ![最新同步](https://img.shields.io/badge/%E6%9C%80%E6%96%B0%E5%90%8C%E6%AD%A5-2026--06--18-blue) ![排队复核](https://img.shields.io/badge/%E6%8E%92%E9%98%9F%E5%A4%8D%E6%A0%B8-6-yellow)

> 本 README 每周自动从 [claude.aiso.cool](https://claude.aiso.cool) 同步,trust 数据(`96/102` · `100%`)实时反映核查状态。同步流水线见 [`.github/workflows/sync.yml`](https://github.com/xiaohei16k/awesome-claude-commands-zh/blob/main/.github/workflows/sync.yml)。

本仓库整理 Claude Code 全部 slash 命令、CLI 子命令、Hook 事件、启动参数,所有内容来自深度核查项目 [claude.aiso.cool](https://claude.aiso.cool) — 每条命令带交叉核查 verdict、官方文档来源,且统一锚定到同一个 Claude Code 版本。

当前收录 **227** 个命令,其中 **96** 个已完成 LLM 二阶段交叉核查(对照 docs.claude.com 官方源),通过率 **100%**。

---

## 目录

- [Slash 命令(104)](#slash-命令)
- [CLI 子命令(34)](#cli-子命令)
- [Hook 事件(28)](#hook-事件)
- [启动参数(61)](#启动参数)
- [本仓库 vs 网站](#本仓库-vs-网站)
- [如何贡献](#如何贡献)
- [License](#license)

## Slash 命令

<a id="slash-命令"></a>

会话中以 `/` 开头的命令,直接在 Claude Code 对话框里输入。例如 `/init`、`/clear`、`/agents`。

| 命令 | 简介 | 核查结论 | 锚定版本 | 详情 |
| --- | --- | --- | --- | --- |
| `/add-dir` | 为当前会话添加工作目录以用于文件访问 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-add-dir) |
| `/advisor` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-advisor) |
| `/agents` | 管理代理的配置和设置选项 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-agents) |
| `/approved-tools` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-approved-tools) |
| `/autofix-pr` | 启动远程会话自动修复 PR 中的 CI 失败 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-autofix-pr) |
| `/background` | 将当前会话后台运行并释放当前终端 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-background) |
| `/batch` | 并行编排大规模代码库变更和提交 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-batch) |
| `/bg` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-bg) |
| `/branch` | 在当前位置创建对话分支以保留原始会话 | ⏳ 排队复核 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-branch) |
| `/btw` | 提出快速旁问而不添加到对话 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-btw) |
| `/buddy` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-buddy) |
| `/bug` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-bug) |
| `/cd` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-cd) |
| `/chrome` | 配置 Claude 在 Chrome 浏览器中的设置 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-chrome) |
| `/claude-api` | 加载项目语言的 Claude API 参考和代理文档 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-claude-api) |
| `/clear` | 使用空上下文开始新对话并保留前一个 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-clear) |
| `/code-review` | 检查当前 diff 中的代码正确性缺陷并报告 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-code-review) |
| `/color` | 为当前会话设置提示栏的颜色主题 | 🟢 通过 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-color) |
| `/commit-push-pr` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-commit-push-pr) |
| `/compact` | 通过汇总对话内容来释放上下文空间 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-compact) |
| `/config` | 打开设置界面调整主题、模型等偏好 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-config) |
| `/context` | 可视化当前上下文使用情况和优化建议 | 🟠 重大 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-context) |
| `/copy` | 将最后的助手响应复制到剪贴板 | 🟠 重大 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-copy) |
| `/cost` | 显示使用成本和计费统计信息 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-cost) |
| `/debug` | 启用调试日志并诊断排查会话问题 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-debug) |
| `/desktop` | 在 Claude Code Desktop 应用中继续会话 | 🟠 重大 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-desktop) |
| `/diff` | 打开交互式 diff 查看器显示未提交更改 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-diff) |
| `/doctor` | 诊断并验证 Claude Code 的安装和设置 | 🟠 重大 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-doctor) |
| `/effort` | 设置模型工作难度级别从低到最高 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-effort) |
| `/env` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-env) |
| `/exit` | 退出 CLI 或从后台会话中分离 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-exit) |
| `/export` | 将当前对话导出为纯文本格式或保存文件 | 🟢 通过 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-export) |
| `/extra-usage` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-extra-usage) |
| `/fast` | 切换快速模式的开启或关闭状态 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-fast) |
| `/feedback` | 提交反馈、报告错误或分享对话 | 🟠 重大 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-feedback) |
| `/focus` | 切换焦点视图仅显示最后提示和工具摘要 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-focus) |
| `/fork` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-fork) |
| `/goal` | 设置目标使Claude持续工作直到条件满足 | 🟢 通过 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-goal) |
| `/heapdump` | 写入堆快照和内存分解以诊断高内存使用 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-heapdump) |
| `/help` | 显示帮助信息和可用的所有命令 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-help) |
| `/hooks` | 查看和管理工具事件的Hook配置 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-hooks) |
| `/ide` | 管理IDE集成并显示集成状态 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-ide) |
| `/init` | 使用CLAUDE.md指南初始化项目 | 🟢 通过 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-init) |
| `/insights` | 生成分析Claude Code会话的报告 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-insights) |
| `/install-github-app` | 为仓库设置Claude GitHub Actions应用 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-install-github-app) |
| `/keybindings` | 打开或创建快捷键配置文件 | 🟢 通过 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-keybindings) |
| `/less-permission-prompts` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-less-permission-prompts) |
| `/login` | 登录Anthropic账户并验证身份 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-login) |
| `/logout` | 登出Anthropic账户并清除会话 | 🟢 通过 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-logout) |
| `/loop` | 重复运行提示直到会话关闭 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-loop) |
| `/mcp` | 管理MCP服务器连接和OAuth认证 | 🟡 轻微 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-mcp) |
| `/memory` | 编辑memory文件并管理自动memory功能 | 🟢 通过 | v2.1.178 | [查看](https://claude.aiso.cool/commands/slash-memory) |
| `/mobile` | 显示二维码下载Claude移动应用 | 🟢 通过 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-mobile) |
| `/model` | 设置当前会话使用的AI模型 | 🟢 通过 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-model) |
| `/output-style` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-output-style) |
| `/permissions` | 管理工具权限的允许、询问和拒绝规则 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-permissions) |
| `/plan` | 直接从提示进入计划模式执行任务 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-plan) |
| `/plugin` | 管理Claude Code的插件配置 | 🟢 通过 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-plugin) |
| `/plugin install` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-plugin-install) |
| `/plugin list` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-plugin-list) |
| `/plugins` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-plugins) |
| `/poll` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-poll) |
| `/powerup` | 通过快速交互课程发现Claude Code功能 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-powerup) |
| `/proactive` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-proactive) |
| `/recap` | 生成当前会话的一行摘要 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-recap) |
| `/release-notes` | 在交互版本选择器中查看变更日志 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-release-notes) |
| `/reload-plugins` | 重新加载活跃插件应用待处理变更 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-reload-plugins) |
| `/reload-skills` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-reload-skills) |
| `/remote-control` | 使此会话可从 claude.ai 远程控制 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-remote-control) |
| `/remote-env` | 配置网络会话的默认远程环境 | 🟠 重大 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-remote-env) |
| `/rename` | 重命名当前会话并在提示栏显示 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-rename) |
| `/resume` | 通过 ID 或名称恢复会话或打开选择器 | 🟢 通过 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-resume) |
| `/review` | 在本地会话中查看和审查 pull request | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-review) |
| `/rewind` | 将对话和代码倒回到之前的点 | 🟢 通过 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-rewind) |
| `/sandbox` | 切换沙箱模式提高安全性 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-sandbox) |
| `/schedule` | 创建更新或运行在云基础设施执行的例程 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-schedule) |
| `/scroll-speed` | 交互式调整鼠标滚轮滚动速度 | 🟢 通过 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-scroll-speed) |
| `/security-review` | 分析待处理变更的安全漏洞风险 | 🟡 轻微 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-security-review) |
| `/settings` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-settings) |
| `/setup-bedrock` | 配置 Amazon Bedrock 认证和模型 | 🟢 通过 | v2.1.179 | [查看](https://claude.aiso.cool/commands/slash-setup-bedrock) |
| `/setup-vertex` | 配置 Google Vertex AI 认证和模型 | 🟡 轻微 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-setup-vertex) |
| `/simplify` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-simplify) |
| `/skills` | 列出可用 skills 和隐藏不需要的 | 🟡 轻微 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-skills) |
| `/stats` | 打开统计标签显示使用情况 | ⏳ 排队复核 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-stats) |
| `/status` | 打开设置界面显示版本模型和连接 | 🟡 轻微 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-status) |
| `/statusline` | 配置 Claude Code 的状态行显示信息 | 🟡 轻微 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-statusline) |
| `/t` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-t) |
| `/tasks` | 列出和管理后台任务及相关信息 | 🟠 重大 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-tasks) |
| `/team-onboarding` | 从使用历史生成团队入门指南 | 🟡 轻微 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-team-onboarding) |
| `/teleport` | 从网页版Claude Code拉入当前终端 | 🟡 轻微 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-teleport) |
| `/terminal-setup` | 配置Shift+Enter等终端快捷键 | 🟡 轻微 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-terminal-setup) |
| `/theme` | 更改终端配色主题和样式 | 🟠 重大 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-theme) |
| `/todos` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-todos) |
| `/tui` | 设置终端UI渲染器并重启会话 | 🟡 轻微 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-tui) |
| `/ultraplan` | 在ultraplan会话中草稿计划 | 🟢 通过 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-ultraplan) |
| `/ultrareview` | 运行深层多agent代码审查 | 🟢 通过 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-ultrareview) |
| `/undo` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-undo) |
| `/update` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-update) |
| `/upgrade` | 打开升级页面切换计划等级 | 🟡 轻微 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-upgrade) |
| `/usage` | 显示会话成本和订阅使用统计 | ⏳ 排队复核 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-usage) |
| `/usage-credits` | 配置usage credits在限制后继续工作 | 🟡 轻微 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-usage-credits) |
| `/voice` | 开启或配置语音听写模式 | ⏳ 排队复核 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-voice) |
| `/web-setup` | 连接GitHub账户以使用网页版功能 | 🟢 通过 | v2.1.181 | [查看](https://claude.aiso.cool/commands/slash-web-setup) |
| `/workflows` | — | — | — | [查看](https://claude.aiso.cool/commands/slash-workflows) |

→ [在线版 + 筛选 / 搜索](https://claude.aiso.cool/commands?kind=slash)


## CLI 子命令

<a id="cli-子命令"></a>

终端命令,以 `claude` 开头的子命令。例如 `claude mcp add`、`claude --resume`。

| 命令 | 简介 | 核查结论 | 锚定版本 | 详情 |
| --- | --- | --- | --- | --- |
| `claude agents` | 打开 Agent 视图监控并发送后台会话 | 🟠 重大 | v2.1.181 | [查看](https://claude.aiso.cool/commands/cli-agents) |
| `claude auth` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-auth) |
| `claude auth login` | 登录 Anthropic 账户 | 🟠 重大 | v2.1.181 | [查看](https://claude.aiso.cool/commands/cli-auth-login) |
| `claude auth logout` | 从 Anthropic 账户登出 | 🟡 轻微 | v2.1.181 | [查看](https://claude.aiso.cool/commands/cli-auth-logout) |
| `claude auth status` | 显示身份认证状态为 JSON | 🟠 重大 | v2.1.181 | [查看](https://claude.aiso.cool/commands/cli-auth-status) |
| `claude config` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-config) |
| `claude daemon status` | 打印后台会话主管的状态 | ⏳ 排队复核 | v2.1.181 | [查看](https://claude.aiso.cool/commands/cli-daemon-status) |
| `claude doctor` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-doctor) |
| `claude --help` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-help) |
| `claude install` | 安装或重新安装本地二进制文件 | 🟡 轻微 | v2.1.181 | [查看](https://claude.aiso.cool/commands/cli-install) |
| `claude logs` | 打印后台会话的最近输出 | 🟠 重大 | v2.1.181 | [查看](https://claude.aiso.cool/commands/cli-logs) |
| `claude mcp` | 配置 MCP 服务器 | ⏳ 排队复核 | v2.1.181 | [查看](https://claude.aiso.cool/commands/cli-mcp) |
| `claude mcp add` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-mcp-add) |
| `claude mcp add-from-claude-desktop` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-mcp-add-from-claude-desktop) |
| `claude mcp add-json` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-mcp-add-json) |
| `claude mcp get` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-mcp-get) |
| `claude mcp list` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-mcp-list) |
| `claude mcp serve` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-mcp-serve) |
| `claude plugin details` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-plugin-details) |
| `claude plugin disable` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-plugin-disable) |
| `claude plugin enable` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-plugin-enable) |
| `claude plugin init` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-plugin-init) |
| `claude plugin install` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-plugin-install) |
| `claude plugin marketplace remove` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-plugin-marketplace-remove) |
| `claude plugin prune` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-plugin-prune) |
| `claude plugin tag` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-plugin-tag) |
| `claude plugin update` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-plugin-update) |
| `claude plugin validate` | — | — | — | [查看](https://claude.aiso.cool/commands/cli-plugin-validate) |
| `claude project purge` | 删除项目的所有本地 Claude Code 状态 | — | — | [查看](https://claude.aiso.cool/commands/cli-project-purge) |
| `claude remote-control` | 启动 Remote Control 服务器 | — | — | [查看](https://claude.aiso.cool/commands/cli-remote-control) |
| `claude respawn` | 重启后台会话 | — | — | [查看](https://claude.aiso.cool/commands/cli-respawn) |
| `claude rm` | 从列表中移除后台会话 | — | — | [查看](https://claude.aiso.cool/commands/cli-rm) |
| `claude ultrareview` | 非交互式运行代码审查，输出发现结果到标准输出 | — | — | [查看](https://claude.aiso.cool/commands/cli-ultrareview) |
| `claude update` | 更新到最新版本 | — | — | [查看](https://claude.aiso.cool/commands/cli-update) |

→ [在线版 + 筛选 / 搜索](https://claude.aiso.cool/commands?kind=cli)


## Hook 事件

<a id="hook-事件"></a>

事件钩子,可在 `settings.json` 的 `hooks` 字段配置,Claude Code 在对应时机调用你定义的脚本。例如 `PreToolUse`、`Stop`。

| 命令 | 简介 | 核查结论 | 锚定版本 | 详情 |
| --- | --- | --- | --- | --- |
| `ConfigChange` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-configchange) |
| `CwdChanged` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-cwdchanged) |
| `Elicitation` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-elicitation) |
| `ElicitationResult` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-elicitationresult) |
| `FileChanged` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-filechanged) |
| `InstructionsLoaded` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-instructionsloaded) |
| `MessageDisplay` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-messagedisplay) |
| `Notification` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-notification) |
| `PermissionDenied` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-permissiondenied) |
| `PermissionRequest` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-permissionrequest) |
| `PostCompact` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-postcompact) |
| `PostToolUse` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-posttooluse) |
| `PostToolUseFailure` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-posttoolusefailure) |
| `PreCompact` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-precompact) |
| `PreToolUse` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-pretooluse) |
| `SessionEnd` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-sessionend) |
| `SessionStart` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-sessionstart) |
| `Setup` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-setup) |
| `Stop` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-stop) |
| `StopFailure` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-stopfailure) |
| `SubagentStart` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-subagentstart) |
| `SubagentStop` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-subagentstop) |
| `TaskCompleted` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-taskcompleted) |
| `TaskCreated` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-taskcreated) |
| `TeammateIdle` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-teammateidle) |
| `UserPromptSubmit` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-userpromptsubmit) |
| `WorktreeCreate` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-worktreecreate) |
| `WorktreeRemove` | — | — | — | [查看](https://claude.aiso.cool/commands/hook-worktreeremove) |

→ [在线版 + 筛选 / 搜索](https://claude.aiso.cool/commands?kind=hook)


## 启动参数

<a id="启动参数"></a>

Claude Code CLI 启动参数,跟在 `claude` 后面或写入配置文件。例如 `--model`、`--add-dir`。

| 命令 | 简介 | 核查结论 | 锚定版本 | 详情 |
| --- | --- | --- | --- | --- |
| `--add-dir` | 为 Claude 添加额外的工作目录以读写文件 | — | — | [查看](https://claude.aiso.cool/commands/flag-add-dir) |
| `--agent` | 为当前会话指定一个 agent（覆盖默认设置） | — | — | [查看](https://claude.aiso.cool/commands/flag-agent) |
| `--agents` | 通过 JSON 动态定义自定义子 agent | — | — | [查看](https://claude.aiso.cool/commands/flag-agents) |
| `--all` | — | — | — | [查看](https://claude.aiso.cool/commands/flag-all) |
| `--append-system-prompt` | 在默认系统提示的末尾追加自定义文本 | — | — | [查看](https://claude.aiso.cool/commands/flag-append-system-prompt) |
| `--bare` | 最小化模式，跳过自动发现以加快脚本调用启动 | — | — | [查看](https://claude.aiso.cool/commands/flag-bare) |
| `--bg` | 在后台启动会话并立即返回，打印会话 ID 和管理命令 | — | — | [查看](https://claude.aiso.cool/commands/flag-bg) |
| `-c` | 继续当前目录中最近的会话 | — | — | [查看](https://claude.aiso.cool/commands/flag-c) |
| `--channels` | 指定 MCP 服务器通道，Claude 应在此会话中监听通知 | — | — | [查看](https://claude.aiso.cool/commands/flag-channels) |
| `--chrome` | 启用 Chrome 浏览器集成以进行网络自动化和测试 | — | — | [查看](https://claude.aiso.cool/commands/flag-chrome) |
| `--client-id` | — | — | — | [查看](https://claude.aiso.cool/commands/flag-client-id) |
| `--client-secret` | — | — | — | [查看](https://claude.aiso.cool/commands/flag-client-secret) |
| `-cn` | — | — | — | [查看](https://claude.aiso.cool/commands/flag-cn) |
| `--console` | — | — | — | [查看](https://claude.aiso.cool/commands/flag-console) |
| `--continue` | 加载当前目录中最近的对话（包括添加此目录的会话） | — | — | [查看](https://claude.aiso.cool/commands/flag-continue) |
| `--dangerously-skip-permissions` | 跳过权限提示，等同于 --permission-mode bypassPermissions | — | — | [查看](https://claude.aiso.cool/commands/flag-dangerously-skip-permissions) |
| `--debug` | 启用调试模式并可选择性过滤类别 | — | — | [查看](https://claude.aiso.cool/commands/flag-debug) |
| `--disable-slash-commands` | 禁用此会话的所有 Skill 和命令 | — | — | [查看](https://claude.aiso.cool/commands/flag-disable-slash-commands) |
| `--disabled` | — | — | — | [查看](https://claude.aiso.cool/commands/flag-disabled) |
| `--disallowedTools` | 拒绝规则，从模型上下文中移除 Tool 或拒绝特定匹配 | — | — | [查看](https://claude.aiso.cool/commands/flag-disallowedtools) |
| `--effort` | 为当前会话设置处理难度级别（low/medium/high/xhigh/max） | — | — | [查看](https://claude.aiso.cool/commands/flag-effort) |
| `--enabled` | — | — | — | [查看](https://claude.aiso.cool/commands/flag-enabled) |
| `--exclude-dynamic-system-prompt-sections` | 将每台机器的系统提示部分移至第一条用户消息，改善缓存重用 | — | — | [查看](https://claude.aiso.cool/commands/flag-exclude-dynamic-system-prompt-sections) |
| `--exec` | — | — | — | [查看](https://claude.aiso.cool/commands/flag-exec) |
| `--fallback-model` | 当默认模型过载时自动故障转移到指定模型 | — | — | [查看](https://claude.aiso.cool/commands/flag-fallback-model) |
| `--from-pr` | 恢复与特定拉取请求相关的会话 | — | — | [查看](https://claude.aiso.cool/commands/flag-from-pr) |
| `--help` | — | — | — | [查看](https://claude.aiso.cool/commands/flag-help) |
| `--ide` | 启动时自动连接到可用IDE | — | — | [查看](https://claude.aiso.cool/commands/flag-ide) |
| `--include-partial-messages` | 在输出中包含部分流事件 | — | — | [查看](https://claude.aiso.cool/commands/flag-include-partial-messages) |
| `--init` | 在会话前运行Setup hooks（仅打印模式） | — | — | [查看](https://claude.aiso.cool/commands/flag-init) |
| `--init-only` | 运行Setup和SessionStart hooks后退出 | — | — | [查看](https://claude.aiso.cool/commands/flag-init-only) |
| `--json` | — | — | — | [查看](https://claude.aiso.cool/commands/flag-json) |
| `--json-schema` | 获取与JSON Schema匹配的验证JSON输出 | — | — | [查看](https://claude.aiso.cool/commands/flag-json-schema) |
| `--maintenance` | 在会话前运行维护Setup hooks（仅打印模式） | — | — | [查看](https://claude.aiso.cool/commands/flag-maintenance) |
| `--max-budget-usd` | 设置API调用的最大花费金额限制 | — | — | [查看](https://claude.aiso.cool/commands/flag-max-budget-usd) |
| `--mcp-config` | 从JSON文件或字符串加载MCP服务器 | — | — | [查看](https://claude.aiso.cool/commands/flag-mcp-config) |
| `--mcp-debug` | — | — | — | [查看](https://claude.aiso.cool/commands/flag-mcp-debug) |
| `--model` | 为当前会话设置模型 | — | — | [查看](https://claude.aiso.cool/commands/flag-model) |
| `-n` | — | — | — | [查看](https://claude.aiso.cool/commands/flag-n) |
| `--name` | 设置会话显示名称 | — | — | [查看](https://claude.aiso.cool/commands/flag-name) |
| `--output-format` | 为打印模式指定输出格式 | — | — | [查看](https://claude.aiso.cool/commands/flag-output-format) |
| `-p` | 通过 SDK 查询然后退出 | — | — | [查看](https://claude.aiso.cool/commands/flag-p) |
| `--permission-mode` | 以指定的权限模式开始会话 | — | — | [查看](https://claude.aiso.cool/commands/flag-permission-mode) |
| `--plugin-dir` | 从目录或ZIP存档加载插件 | — | — | [查看](https://claude.aiso.cool/commands/flag-plugin-dir) |
| `--plugin-url` | 从URL获取插件ZIP存档 | — | — | [查看](https://claude.aiso.cool/commands/flag-plugin-url) |
| `--print` | 打印响应而不使用交互模式 | — | — | [查看](https://claude.aiso.cool/commands/flag-print) |
| `--remote-control` | 启动启用Remote Control的交互式会话 | — | — | [查看](https://claude.aiso.cool/commands/flag-remote-control) |
| `--remote-control-session-name-prefix` | 设置Remote Control会话名称前缀 | — | — | [查看](https://claude.aiso.cool/commands/flag-remote-control-session-name-prefix) |
| `--replay-user-messages` | 重新发出stdin中的用户消息到stdout进行确认 | — | — | [查看](https://claude.aiso.cool/commands/flag-replay-user-messages) |
| `--resume` | 恢复特定会话或显示交互式会话选择器 | — | — | [查看](https://claude.aiso.cool/commands/flag-resume) |
| `--safe-mode` | — | — | — | [查看](https://claude.aiso.cool/commands/flag-safe-mode) |
| `--session-id` | 为对话使用特定的会话ID | — | — | [查看](https://claude.aiso.cool/commands/flag-session-id) |
| `--setting-sources` | 指定要加载的设置源列表 | — | — | [查看](https://claude.aiso.cool/commands/flag-setting-sources) |
| `--settings` | 指定设置JSON文件或内联JSON字符串 | — | — | [查看](https://claude.aiso.cool/commands/flag-settings) |
| `--strict-mcp-config` | 仅使用指定的MCP服务器配置忽略其他配置 | — | — | [查看](https://claude.aiso.cool/commands/flag-strict-mcp-config) |
| `--system-prompt` | 用自定义文本替换整个系统提示 | — | — | [查看](https://claude.aiso.cool/commands/flag-system-prompt) |
| `--system-prompt-file` | 从文件加载系统提示替换默认值 | — | — | [查看](https://claude.aiso.cool/commands/flag-system-prompt-file) |
| `--teleport` | 在本地终端中恢复web会话 | — | — | [查看](https://claude.aiso.cool/commands/flag-teleport) |
| `--tools` | 限制Claude可以使用的内置工具 | — | — | [查看](https://claude.aiso.cool/commands/flag-tools) |
| `-w` | — | — | — | [查看](https://claude.aiso.cool/commands/flag-w) |
| `--worktree` | 在隔离的git worktree中启动Claude | — | — | [查看](https://claude.aiso.cool/commands/flag-worktree) |

→ [在线版 + 筛选 / 搜索](https://claude.aiso.cool/commands?kind=flag)

## 本仓库 vs 网站

| 场景 | 用 GitHub README | 用 [claude.aiso.cool](https://claude.aiso.cool) |
| --- | --- | --- |
| 速查 / 离线浏览 | ✅ 一屏全部命令 | — |
| git clone 本地版本控制 | ✅ `git pull` 即可 | — |
| 站内搜索 / 按 verdict 筛选 | — | ✅ `/commands?q=…&verdict=…` |
| 看 verdict 来源核查细节(具体哪个 claim 不被支持、severity、原文链接) | — | ✅ 每条命令独立详情页 |
| 看深度使用指南(用例 / tips / 陷阱) | — | ✅ `/commands/<slug>` 长文 |
| 看 changelog / 跨版本变更 | — | ✅ `/changelog` |
| RSS 订阅命令变更 | — | ✅ `/feed.xml` |

简言之:**这里是入口,网站是真相**。表格里点 `查看` 都会跳回 [claude.aiso.cool](https://claude.aiso.cool) 对应的核查详情页。

## 相关页面

- [一屏速查 / Cheatsheet](https://claude.aiso.cool/cheatsheet) — 全量命令单页 + verdict + 锚定版本,适合打印 / 离屏速查
- [15 个核查通过的常用命令](https://claude.aiso.cool/blog/15-verified-commands) — 精选 verdict=clean 的常用命令导读
- [按 trust 排序](https://claude.aiso.cool/commands?sort=trust) — 优先查看 verdict=clean / 锚定最新版本的命令
- [按 verdict 筛选](https://claude.aiso.cool/commands?verdict=verified) — 只看已核查通过的
- [变更日志 / Changelog](https://claude.aiso.cool/changelog) — 命令跨版本变化时间线
- [Atom 订阅](https://claude.aiso.cool/feed.xml) — 命令变更 / 核查更新 feed

## 如何贡献

发现某条命令的 verdict / purpose / 锚定版本有误?直接到 [主项目仓库](https://github.com/xiaohei16k/followup) 开 issue,或在 [claude.aiso.cool](https://claude.aiso.cool) 对应详情页底部点 "Report"。本仓库的 README 由脚本自动从主项目数据再生,直接 PR 这里的 .md 不会生效。

## License

[MIT](LICENSE) — 命令名、purpose 摘要、verdict 数据均可自由转载,请保留对 [claude.aiso.cool](https://claude.aiso.cool) 的署名链接。

---

<sub>Last generated 2026-06-18 · Aligned to multiple versions · Powered by [claude.aiso.cool](https://claude.aiso.cool)</sub>
