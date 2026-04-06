# Claude Code 新手指南

> 从安装到上手的完整教程。安装前有任何疑问？先问 ChatGPT 等 AI 对话工具。安装好文渊后，直接在 Claude Code 里问它就好。

---

## 什么是 Claude Code？

Claude Code 是一个运行在终端中的 AI 助手。它可以读写你电脑上的文件、理解项目结构、通过自然语言完成复杂任务。在文渊中，它是帮你规划研究、精读文献、整理笔记、润色论文的伙伴。

> **什么是终端？** 终端是电脑上的一个程序，你可以在里面输入文字命令来操作电脑。Mac 按 `Cmd + 空格` 搜索"终端"打开；Windows 按 `Win + R` 输入 `cmd` 打开。

---

## 安装

### 方式一：官方脚本（推荐）

打开终端，复制下面的命令粘贴进去，按回车：

**Mac / Linux：**
```bash
curl -fsSL https://claude.ai/install.sh | bash
```

**Windows（PowerShell）：**
```powershell
irm https://claude.ai/install.ps1 | iex
```

### 方式二：通过 npm

如果你已经安装了 Node.js：
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

---

## 国内使用方案

Claude Code 需要访问 Anthropic 服务。国内用户有以下几种方式，按推荐程度排序：

### 方案一：直接订阅 Anthropic（体验最好）

使用 Anthropic 官方服务，性能最强、延迟最低，Claude Code 的最佳体验。

- Pro 计划 $20/月 起 → [Anthropic 定价](https://www.anthropic.com/pricing)
- 详见 [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code)

**国内订阅注意事项：**
- 需要稳定的海外网络节点，注册和使用保持同一节点
- 推荐用 Gmail/Outlook 注册
- 支付可通过代充平台或虚拟信用卡
- **防封号**：不频繁换 IP、不共享账号、新号头几天轻度使用
- 被封可通过 support@anthropic.com 申诉

### 方案二：cc-switch 切换模型（灵活选择）

[cc-switch](https://github.com/farion1231/cc-switch) 是社区开发的模型切换工具，可以让 Claude Code 一键切换到不同的 AI 模型（包括国产模型）。

```bash
# 安装
npm install -g cc-switch

# 使用
cc-switch          # 选择模型
claude             # 正常启动
```

**可用模型和国内 Token 订阅平台：**

| 模型 | 平台 | 特点 |
|------|------|------|
| Kimi (K2) | [kimi.moonshot.cn](https://kimi.moonshot.cn/) | 国内可直接用，长文本能力强 |
| DeepSeek | [platform.deepseek.com](https://platform.deepseek.com/) | 性价比极高，中文优秀 |
| 智谱 GLM | [open.bigmodel.cn](https://open.bigmodel.cn/) | 学术场景表现好 |
| 通义千问 (Qwen) | [bailian.console.aliyun.com](https://bailian.console.aliyun.com/) | 阿里百炼，国内稳定 |
| MiniMax | [platform.minimaxi.com](https://platform.minimaxi.com/) | 长文本支持 |
| Gemini | 通过 cc-switch 或环境变量 | 免费额度大 |
| GPT | 通过 cc-switch 或环境变量 | 综合能力强 |

> Claude Code 可以用 Gemini 和 GPT 吗？**可以。** 通过 cc-switch 或配置环境变量即可切换。

### 方案三：API 中转平台（需谨慎选择）

使用第三方平台转发 API 请求，无需处理海外支付和网络问题。

**设置方法（在终端中输入以下命令）：**
```bash
# 以 OpenRouter 为例，将以下内容添加到 ~/.zshrc（Mac）或 ~/.bashrc（Linux）
echo 'export ANTHROPIC_BASE_URL="https://openrouter.ai/api"' >> ~/.zshrc
echo 'export ANTHROPIC_AUTH_TOKEN="你的API-Key"' >> ~/.zshrc
echo 'export ANTHROPIC_API_KEY=""' >> ~/.zshrc
source ~/.zshrc
```

**主流平台：**

| 平台 | 特点 |
|------|------|
| [OpenRouter](https://openrouter.ai/) | 国外最大的模型聚合平台 |
| [SiliconFlow（硅基流动）](https://siliconflow.cn/) | 国内平台，延迟低 |

> ⚠️ **注意：** 中转平台鱼龙混杂，选择时注意：优先选运营时间长、口碑好的；不要大额充值；避免在涉及敏感信息时使用非官方平台。

---

## 更多学习资源

- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code)
- [code.claude.com](https://code.claude.com) — 官方入门页面
- 在 Claude Code 中输入 `/help` 查看所有命令

**搜索关键词：**

| 平台 | 搜索词 |
|------|--------|
| B站 | `Claude Code 教程`、`Claude Code 零基础` |
| 知乎 | `Claude Code 入门`、`AI 编程助手` |
| 小红书 | `Claude Code 实战`、`AI 编程小白` |
| 微信公众号 | `Claude Code`、`AI 编码助手` |
| CSDN / 掘金 / 少数派 | `Claude Code 教程` |

---

## 常见问题

**Q: "command not found: claude" 怎么办？**
A: 重新运行安装脚本或 `npm install -g @anthropic-ai/claude-code`，然后重启终端。

**Q: 用了中转平台后不响应？**
A: 检查所选模型是否支持 tool calling（工具调用）。文渊的工作流依赖此功能。

**Q: 不确定怎么操作？**
A: 安装之前，问 ChatGPT 或其他 AI 对话工具。安装好文渊之后，直接在 Claude Code 中说出你的疑问——它就是你的使用说明。
