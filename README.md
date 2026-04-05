# 文渊 (WenYuan)

> 专为文科研究者设计的 AI 学术助手——基于 Obsidian + Claude Code

**「文渊」** 取自"文以载道，渊博知识"——古代皇家藏书楼「文渊阁」正是知识汇聚之地。我们希望文渊成为你的**个人学术知识库**：把课堂笔记、论文、灵感、文献全部放进来，AI 帮你梳理、连接、积累，越用越有价值。

> **愿景：** 受 Andrej Karpathy 的"LLM 个人知识库"理念启发——不把笔记分散在各种 App 里，而是全扔进一个文件夹，让 AI 帮你整理成个人学术维基。文渊就是这个理念的文科学术版本。

文渊是一个开箱即用的 Obsidian 知识库模板，配合 AI 编码助手（Claude Code），为文科博士和研究者提供从灵感捕捉到论文写作的全流程学术生产力系统。

---

## 能做什么？

| 场景 | 命令 | 说明 |
|------|------|------|
| 每日规划 | `/start-my-day` | 回顾昨日、规划今日、连接活跃项目 |
| 精读文献 | `/read` | 苏格拉底式引导精读，生成结构化笔记 |
| 概念溯源 | `/explore <概念>` | 深度梳理定义、演变、代表人物 |
| 推进项目 | `/kickoff` | 把想法变成结构化的研究项目 |
| 写作辅助 | `/write` | 段落润色、论证逻辑、学术用语 |
| 学术调研 | `/research <主题>` | 对一个主题进行系统性深度调研 |
| 头脑风暴 | `/brainstorm` | 梳理模糊想法，找到研究方向 |
| 笔记整理 | `/organize` | 把零散笔记归类到正确位置 |
| 快速问答 | `/ask <问题>` | 学术概念快速解答 |
| 学术动态 | `/academic-feed` | 推送教职招聘、新论文、会议信息 |
| 归档 | `/archive` | 清理已完成项目，保持系统整洁 |

---

## 开始之前

文渊需要两个前提工具。如果你还不熟悉它们，请先学习：

### 1. Obsidian — 你的知识库

Obsidian 是一款免费的本地笔记软件，你的所有学术资料都存在自己电脑上。

**学习资源：**
- [Obsidian 官方中文帮助](https://help.obsidian.md/zh/)
- [PKMer 社区](https://pkmer.cn/) — 国内最活跃的 Obsidian 中文社区
- B站搜索 `Obsidian 保姆级教程` 或 `Obsidian 新手指南`

**你只需要掌握：**
- 创建和打开一个仓库（vault）
- 基本的 Markdown 语法（标题、列表、加粗）
- 双向链接 `[[笔记名]]`

### 2. Claude Code — 你的 AI 研究伙伴

Claude Code 是 Anthropic 公司开发的 AI 编码助手，运行在终端中。它可以读写你的文件，是文渊的"大脑"。

**学习资源：**
- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code)
- 安装方法：`npm install -g @anthropic-ai/claude-code`

**费用说明：**
- Claude Code 需要 Anthropic 订阅，Pro 计划 $20/月起
- 详情见 [Anthropic 定价页面](https://www.anthropic.com/pricing)

#### 用不了 Anthropic？使用其他模型

如果你无法订阅 Anthropic（没有 Visa 信用卡、费用太高等），可以通过以下方式让 Claude Code 连接到其他 AI 模型：

**方法：通过 OpenRouter 使用国内外模型**

1. 注册 [OpenRouter](https://openrouter.ai/)（支持多种支付方式）
2. 获取 API Key
3. 在终端中设置环境变量：

```bash
# 添加到 ~/.zshrc（Mac）或 ~/.bashrc（Linux）
export ANTHROPIC_BASE_URL="https://openrouter.ai/api"
export ANTHROPIC_AUTH_TOKEN="你的OpenRouter API Key"
export ANTHROPIC_API_KEY=""
```

4. 重启终端，即可使用

**支持的模型包括：**
- 国产：Kimi (Moonshot)、MiniMax、DeepSeek、智谱 GLM
- 国外：Gemini、GPT、Llama

更多配置方法可搜索 `claude-code-router` 或 `cc-switch`。

---

## 安装文渊

### 方式一：让 Claude Code 帮你装（推荐）

如果你已经安装了 Claude Code，在终端中运行：

```bash
claude
```

然后对 Claude 说：

> "帮我从 GitHub 下载 cyq1017/wenyuan 这个仓库到我的文档文件夹，然后用 Obsidian 打开它"

Claude 会自动完成下载和配置。

### 方式二：网页下载（零终端）

1. 打开 [https://github.com/cyq1017/wenyuan](https://github.com/cyq1017/wenyuan)
2. 点击绿色的 **Code** 按钮 → **Download ZIP**
3. 解压到你想要的位置（如「文档」文件夹）
4. 打开 Obsidian → 点击「打开文件夹作为仓库」→ 选择解压后的文件夹

### 方式三：命令行

```bash
# 使用 npx degit（需要 Node.js）
npx degit cyq1017/wenyuan 我的文渊

# 或使用 git clone
git clone https://github.com/cyq1017/wenyuan.git 我的文渊
```

---

## 安装完成后

1. 在 Obsidian 中打开文渊文件夹
2. 安装 Terminal 插件（在 Obsidian 内打开终端）→ 详见 [[99_系统/Obsidian新手指南]]
3. 在终端中 `cd` 到文渊文件夹，运行 `claude`
4. 输入 `/start-my-day` 开始你的第一天！

**新手必读：**
- [[99_系统/Obsidian新手指南]] — Obsidian 入门 + Terminal 插件配置
- [[99_系统/Claude Code新手指南]] — Claude Code 安装 + 换模型 + 国内订阅
- [[99_系统/快速上手教程]] — 手把手带你跑完一个完整流程（纸质笔记 OCR 归档）
- [[99_系统/文渊使用指南]] — 全部功能的详细说明 + 个性化定制

---

## 其他 AI 工具（实验性）

文渊的核心工作流为 Claude Code 设计，但也兼容其他 AI 编码助手。用自然语言描述你的需求即可：

| 工具 | 配置文件 | 链接 |
|------|----------|------|
| Gemini CLI | `GEMINI.md` | [github.com/google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli) |
| Codex CLI | `AGENTS.md` | [github.com/openai/codex](https://github.com/openai/codex) |

---

## 文件夹说明

```
文渊/
├── 00_收件箱/     灵感和想法的快速捕捉站
├── 10_日记/       每日学术日志 (YYYY-MM-DD.md)
├── 20_项目/       学术项目（论文、课题、研究计划）
├── 30_文献/       文献精读笔记与研究综述
├── 40_概念/       学术概念卡片（原子化知识单元）
├── 50_资源/       外部资源收藏
├── 90_计划/       写作计划与阶段性目标
└── 99_系统/       模板、提示词、偏好设置、归档
```

---

## 命令速查表

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

---

## 常见问题

**Q: 需要会编程吗？**
A: 不需要。你只需要能在终端中输入一行命令启动 Claude Code，之后的交互全部用自然语言。

**Q: 数据安全吗？**
A: 你的所有笔记都存在本地电脑上，不会自动上传到任何地方。AI 交互时会将相关内容发送给 AI 服务商处理。

**Q: 可以在手机上用吗？**
A: Obsidian 有移动端 App，可以随时查看和编辑笔记。但 Claude Code 需要电脑端的终端运行。

**Q: 和 Notion / 语雀有什么区别？**
A: 文渊基于 Obsidian，数据全部本地化、纯 Markdown 格式，不依赖任何云服务。你的学术资料完全掌握在自己手中。

---

## 设计理念

文渊的设计参考了 [OrbitOS](https://github.com/MarsWang42/OrbitOS) 框架，并为人文学科学术场景重新设计：

- **AI 即助手**：AI 不替代你的思考，而是引导和辅助。文献精读用苏格拉底式提问，头脑风暴用发散性对话。
- **知识即网络**：通过双向链接将概念、文献、项目连成知识网络，越用越有价值。
- **简单即力量**：纯 Markdown 文件，不依赖复杂插件，不锁定任何平台。
- **以用户为中心**：所有工作流围绕文科研究者的真实场景设计——选题、文献、写作、答辩。

---

## 开源协议

MIT License — 自由使用、修改、分发。
