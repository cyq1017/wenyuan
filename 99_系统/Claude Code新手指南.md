# Claude Code 新手指南

> 从安装到使用的完整教程，包括换模型、国内订阅和防封号指南。

---

## 什么是 Claude Code？

Claude Code 是 Anthropic 公司开发的 **AI 编码助手**，运行在终端（命令行）中。它可以：
- 读取和编写你电脑上的文件
- 通过自然语言对话完成复杂任务
- 理解你的项目结构并给出建议

在文渊中，Claude Code 是你的 **AI 学术研究伙伴**——它能帮你规划研究、精读文献、整理笔记、润色论文。

---

## 安装 Claude Code

### 前提：安装 Node.js

Claude Code 需要 Node.js 运行环境。

**Mac 用户：**
1. 打开终端（在 Spotlight 中搜索"终端"或"Terminal"）
2. 安装 Homebrew（如果没有的话）：
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
3. 安装 Node.js：
```bash
brew install node
```

**Windows 用户：**
1. 下载 [Node.js 官网](https://nodejs.org/) 的 LTS 版本
2. 双击安装，一路 Next

### 安装 Claude Code

在终端中运行：
```bash
npm install -g @anthropic-ai/claude-code
```

### 首次启动

```bash
claude
```

首次运行会要求你登录 Anthropic 账号或输入 API Key。

---

## 费用说明

Claude Code **没有免费档**。你需要以下方式之一来使用：

| 方案 | 费用 | 说明 |
|------|------|------|
| Pro 订阅 | $20/月 | 入门级，够用 |
| Max 5x | $100/月 | 重度用户 |
| API 按量计费 | 按 token 收费 | 轻度使用可能更便宜 |

**学生优惠：** Anthropic 没有直接的学生折扣，但部分大学有教育合作计划。可以询问你的学校 IT 部门。

---

## 国内用户：如何订阅 Anthropic

> 由于 Anthropic 未对中国大陆开放服务，以下是社区实践经验汇总。请注意合规使用。

### 注册准备

1. **网络环境**
   - 需要稳定的海外网络节点（推荐美国）
   - 注册、支付、日常使用尽量固定同一节点

2. **邮箱**
   - 推荐 Gmail 或 Outlook
   - 避免使用 QQ、163 等国内邮箱

3. **手机验证**
   - 需要海外手机号接收验证码
   - 可通过 SMS-Activate 等接码平台获取

### 支付方式

**方式一：代充值/合租平台**
- 最稳妥的方式，无需处理海外支付
- 搜索"Claude Pro 代充"可找到相关服务

**方式二：虚拟信用卡（谨慎）**
- 许多虚拟卡平台已被加入黑名单
- 如果使用，确保卡内余额充足（多出 $1-2）
- 账单地址需与 IP 地区一致

### 防封号指南

Claude 对异常行为非常敏感。遵守以下规则：

- **固定网络节点** — 不要频繁切换 IP，换节点容易触发风控
- **不共享账号** — 一人一号，避免多设备同时登录
- **内容合规** — 不发送违规内容
- **新号养号** — 注册后前几天不要高频大量使用，让系统判定为正常用户
- **避免自动化** — 不要用脚本发送批量请求
- **在 CLAUDE.md 中** — 可以添加使用环境说明，引导 AI 正常响应

**如果被封号：**
1. 确认是暂停（Suspended）还是封禁（Banned）
2. 通过 support@anthropic.com 发起申诉
3. 说明正常使用场景（学术研究），态度诚恳

---

## 替代方案：使用其他模型（推荐）

如果你不想/不能订阅 Anthropic，可以让 Claude Code 连接到其他 AI 模型。这是**最推荐的方案**——完全合规，费用更低。

### 方法一：通过 OpenRouter

[OpenRouter](https://openrouter.ai/) 是一个 AI 模型聚合平台，支持国内外多种模型。

**设置步骤：**

1. 注册 OpenRouter 账号（支持多种支付方式）
2. 获取你的 API Key
3. 在终端中配置环境变量：

**Mac 用户**（打开终端输入）：
```bash
echo 'export ANTHROPIC_BASE_URL="https://openrouter.ai/api"' >> ~/.zshrc
echo 'export ANTHROPIC_AUTH_TOKEN="你的OpenRouter-API-Key"' >> ~/.zshrc
echo 'export ANTHROPIC_API_KEY=""' >> ~/.zshrc
source ~/.zshrc
```

**Windows 用户**（在 PowerShell 中）：
```powershell
[Environment]::SetEnvironmentVariable("ANTHROPIC_BASE_URL", "https://openrouter.ai/api", "User")
[Environment]::SetEnvironmentVariable("ANTHROPIC_AUTH_TOKEN", "你的OpenRouter-API-Key", "User")
[Environment]::SetEnvironmentVariable("ANTHROPIC_API_KEY", "", "User")
```

4. 重启终端，运行 `claude` 即可

### 方法二：使用 claude-code-router (ccr)

[claude-code-router](https://github.com/search?q=claude-code-router) 是社区开发的路由工具，可以更灵活地切换模型。

搜索 `cc-switch` 或 `claude-code-router` 获取最新使用方法。

### 支持的模型

| 类别 | 模型 | 说明 |
|------|------|------|
| 国产 | Kimi (Moonshot) | 中文能力强 |
| 国产 | DeepSeek | 性价比高 |
| 国产 | MiniMax | 长文本支持好 |
| 国产 | 智谱 GLM | 学术能力不错 |
| 国外 | Gemini | Google 出品，免费额度大 |
| 国外 | GPT-4o | OpenAI 出品 |

**注意：** 不同模型对 tool calling（工具调用）的支持程度不同。文渊的 skill 系统依赖此功能，建议优先选择支持良好的模型（如 DeepSeek、Gemini、GPT-4o）。

---

## 基本使用

### 启动 Claude Code

```bash
cd 你的文渊文件夹路径
claude
```

### 使用 Slash 命令

在 Claude Code 中输入 `/` 会看到所有可用命令：

```
/start-my-day     每日规划
/read              精读文献
/explore <概念>    概念溯源
/kickoff           想法→项目
/write             写作辅助
/research <主题>   学术调研
/brainstorm        头脑风暴
/organize          笔记整理
/ask <问题>        快速问答
/academic-feed     学术动态
/archive           归档清理
```

### 使用自然语言

你也可以不用命令，直接用自然语言和 Claude 对话：
- "帮我整理一下收件箱里的笔记"
- "我想了解一下叙事学这个概念"
- "帮我看看今天有什么教职招聘"

Claude 会自动识别你的意图并使用对应的 skill。

---

## 在 Obsidian 中使用

安装 Obsidian 的 Terminal 插件后（见 [[Obsidian新手指南]]），你可以：

1. 在 Obsidian 内打开终端（`Cmd/Ctrl + P` → `Terminal: Open terminal`）
2. 终端会自动定位到文渊文件夹
3. 运行 `claude` 启动 AI 助手
4. 一边查看笔记，一边和 AI 对话

这就是文渊的完整使用体验：**Obsidian + Claude Code = 一体化学术工作站**。

---

## 常见问题

**Q: "command not found: claude" 怎么办？**
A: 确保你已经安装了 Node.js 和 Claude Code（`npm install -g @anthropic-ai/claude-code`）。如果安装了还报错，可能需要重启终端。

**Q: 用了 OpenRouter 后 Claude Code 卡住不响应？**
A: 检查你选择的模型是否支持 tool calling。如果不支持，Claude Code 无法正常执行 skill。

**Q: API 用量怎么控制？**
A: OpenRouter 可以在后台设置用量上限。建议先设一个较低的限额，熟悉后再调整。

**Q: 我的对话内容会被 AI 公司看到吗？**
A: AI 服务商会处理你发送的内容来生成回复。不要在对话中发送敏感个人信息。你的笔记存在本地，只有在和 AI 对话时相关部分才会发送。
