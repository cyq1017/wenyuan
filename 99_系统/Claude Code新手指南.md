# Claude Code 新手指南

> 从安装到上手的完整教程。遇到不懂的地方？直接在 Claude Code 中问它就好。

---

## 什么是 Claude Code？

Claude Code 是一个运行在终端中的 AI 助手。它可以读写你电脑上的文件、理解项目结构、通过自然语言完成复杂任务。在文渊中，它是帮你规划研究、精读文献、整理笔记、润色论文的伙伴。

---

## 安装

### 方式一：官方脚本（推荐）

**Mac / Linux：**
```bash
curl -fsSL https://claude.ai/install.sh | bash
```

**Windows（PowerShell）：**
```powershell
irm https://claude.ai/install.ps1 | iex
```

### 方式二：通过 npm

```bash
npm install -g @anthropic-ai/claude-code
```

安装完成后，在终端输入 `claude` 即可启动。首次运行会引导你登录。

---

## 使用方式

在文渊文件夹中启动后，你可以：

**用 `/` 命令触发工作流：**
```
/start-my-day    → 开始新的一天
/read            → 精读一篇文献
/brainstorm      → 头脑风暴
```

**用自然语言对话：**
- "帮我整理收件箱里的笔记"
- "什么是文化霸权？"
- "帮我润色这段论述"

遇到任何问题，直接问 Claude 就好——它就是你的使用说明。

---

## 国内使用方案

Claude Code 需要访问 Anthropic 服务。国内用户有以下几种方式：

### 方案一：API 中转平台（最简单）

使用第三方平台转发 API 请求，无需处理海外支付和网络问题。

**设置方法：**
```bash
# 以 OpenRouter 为例，添加到 ~/.zshrc（Mac）或 ~/.bashrc（Linux）
export ANTHROPIC_BASE_URL="https://openrouter.ai/api"
export ANTHROPIC_AUTH_TOKEN="你的API-Key"
export ANTHROPIC_API_KEY=""
```

重启终端后生效。

**主流平台：**

| 平台 | 特点 |
|------|------|
| [OpenRouter](https://openrouter.ai/) | 国外最大的模型聚合平台 |
| [SiliconFlow（硅基流动）](https://siliconflow.cn/) | 国内平台，延迟低 |
| [DeepSeek 开放平台](https://platform.deepseek.com/) | 性价比高 |

> 注意：选择中转平台时，优先选运营时间长、口碑好的；不要大额充值；避免在涉及敏感信息时使用非官方平台。

### 方案二：cc-switch（灵活切换模型）

[cc-switch](https://github.com/farion1231/cc-switch) 是社区开发的模型切换工具，可以让 Claude Code 一键切换到不同的 AI 模型。

```bash
# 安装
npm install -g cc-switch

# 使用
cc-switch          # 选择模型
claude             # 正常启动
```

### 方案三：直接订阅 Anthropic

如果你能解决海外支付，直接订阅是最佳体验：
- Pro 计划 $20/月 起
- 详见 [Anthropic 定价](https://www.anthropic.com/pricing)

**国内订阅注意事项：**
- 需要稳定的海外网络节点，注册和使用保持同一节点
- 推荐用 Gmail/Outlook 注册
- 支付可通过代充平台或虚拟信用卡
- **防封号**：不频繁换 IP、不共享账号、新号头几天轻度使用
- 被封可通过 support@anthropic.com 申诉

### 可用模型一览

| 类别 | 模型 | 适用场景 |
|------|------|----------|
| 国产 | DeepSeek | 性价比高，中文好 |
| 国产 | Kimi (Moonshot) | 长文本，中文好 |
| 国产 | 智谱 GLM | 学术场景不错 |
| 国产 | MiniMax | 长文本支持 |
| 国外 | Gemini | 免费额度大 |
| 国外 | GPT-4o | 综合能力强 |

---

## 更多学习资源

- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code)
- [code.claude.com](https://code.claude.com) — 官方入门页面
- 在 Claude Code 中输入 `/help` 查看所有命令
- CSDN / 掘金 / 少数派搜索 `Claude Code 教程` 有大量中文实践分享

---

## 常见问题

**Q: "command not found: claude" 怎么办？**
A: 重新运行安装脚本或 `npm install -g @anthropic-ai/claude-code`，然后重启终端。

**Q: 用了中转平台后不响应？**
A: 检查所选模型是否支持 tool calling（工具调用）。文渊的工作流依赖此功能。

**Q: 不确定怎么操作？**
A: 直接在 Claude Code 中把你的疑问说出来，它会引导你完成。这本身就是 AI 助手最大的优势。
