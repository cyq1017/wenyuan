# 文渊 (WenYuan)

> 用 AI 构建你的学术知识库 · 基于 Obsidian + Claude Code

**「文渊」** 取自“文以载道，渊博知识”——古代皇家藏书楼「文渊阁」寓意知识汇聚之所。在 AI 时代，我们重新构想这个概念：让每位研究者都拥有一座属于自己的「文渊阁」——一个由你和 AI 共同整理、关联、积累的个人学术知识库。知识网络通过双向链接不断生长，AI 基于你的积累给出越来越精准的建议——越用越有价值。

文渊是一个 Obsidian 知识库模板，结合 AI 助手，为研究者提供从灵感捕捉到论文产出的全流程学术工作流。文渊为人文社科学术研究设计，开箱即用。你也可以根据自己的学科和习惯自由调整。

---

## 能做什么？

| 场景 | 命令 | 说明 |
|------|------|------|
| 每日规划 | `/start-my-day` | 回顾昨日、规划今日、推送学术动态 |
| 每日复盘 | `/end-my-day` | 总结成果、更新项目、归档对话、规划明日 |
| 精读文献 | `/read` | 苏格拉底式引导精读，生成结构化笔记 |
| 概念溯源 | `/explore <概念>` | 深度梳理定义、演变、代表人物 |
| 推进项目 | `/kickoff` | 把想法变成结构化的研究项目 |
| 写作辅助 | `/write` | 段落润色、论证逻辑、学术用语 |
| 学术调研 | `/research <主题>` | 对一个主题进行系统性深度调研 |
| 头脑风暴 | `/brainstorm` | 梳理模糊想法，找到研究方向 |
| 笔记整理 | `/organize` | 把零散笔记归类到正确位置 |
| 快速问答 | `/ask <问题>` | 学术概念快速解答 |
| 知识解析 | `/parse` | 课堂笔记、读书摘录等非结构化文本 → 结构化笔记 + 概念卡片 |
| 归档 | `/archive` | 清理已完成项目，保持系统整洁 |

---

## 开始之前

文渊 = Obsidian（知识库）+ Claude Code（AI 助手），两者是一个整体。

> 如果你已经熟悉这两个工具，可以跳过这一步直接安装。

### 1. Obsidian — 你的知识库
- 详细教程：安装文渊后查看 → [Obsidian新手指南](99_系统/Obsidian新手指南.md)（含 Terminal 插件、Web Clipper 等配置）
- 或参考：[Obsidian 官方中文帮助](https://help.obsidian.md/zh/) · [PKMer 社区](https://pkmer.cn/) · B站搜索 `Obsidian 保姆级教程`

### 2. Claude Code — 你的 AI 研究伙伴
- 详细教程：安装文渊后查看 → [Claude Code新手指南](99_系统/Claude%20Code新手指南.md)（含安装、换模型、国内使用方案）
- 或参考：[Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code)

---

## 安装文渊

### 方式一：让 Claude Code 帮你装（推荐）

如果你已经安装了 Claude Code，在终端中运行：

```bash
claude
```

然后对 Claude 说：

> "帮我从 GitHub 下载 cyq1017/wenyuan 这个仓库到我的文档文件夹，然后用 Obsidian 打开它"

### 方式二：网页下载（零终端）

1. 打开 [https://github.com/cyq1017/wenyuan](https://github.com/cyq1017/wenyuan)
2. 点击绿色的 **Code** 按钮 → **Download ZIP**
3. 解压到你想要的位置（如「文档」文件夹）
4. 打开 Obsidian → 点击「打开文件夹作为仓库」→ 选择解压后的文件夹

### 方式三：命令行

> 什么是命令行/终端？Mac 按 `Cmd + 空格` 搜索「终端」打开，Windows 按 `Win + R` 输入 `cmd` 打开。终端就是一个可以输入文字命令的窗口。

```bash
git clone https://github.com/cyq1017/wenyuan.git 我的文渊
```

---

## 安装完成后

1. 在 Obsidian 中打开文渊文件夹
2. 安装 Terminal 插件（在 Obsidian 内打开终端）→ 详见 [Obsidian新手指南](99_系统/Obsidian新手指南.md)
3. 在终端中 `cd` 到文渊文件夹，运行 `claude`
4. 输入 `/start-my-day` 开始你的第一天！

**新手必读：**
- [Obsidian新手指南](99_系统/Obsidian新手指南.md) — Obsidian 入门 + 必装插件
- [Claude Code新手指南](99_系统/Claude%20Code新手指南.md) — 安装 + 国内使用 + 换模型
- [快速上手教程](99_系统/快速上手教程.md) — 手把手体验完整工作流
- [文渊使用指南](99_系统/文渊使用指南.md) — 全部功能 + 个性化定制

---

## 其他 AI 工具（实验性）

文渊的核心工作流围绕 Claude Code 设计，但所有的 AI 提示词和工作流指令都以纯文本（Markdown）存储，因此也兼容其他 AI 编码助手。你只需要在对应工具的终端里打开文渊文件夹，用自然语言描述需求即可。不同工具会读取各自的配置文件：

| 工具 | 配置文件 | 链接 | 说明 |
|------|----------|------|------|
| Codex CLI | `AGENTS.md` | [github.com/openai/codex](https://github.com/openai/codex) | OpenAI 官方，每月有免费额度 |
| Kimi Code | `AGENTS.md` | [github.com/nicepkg/kimi-code](https://github.com/nicepkg/kimi-code) | 国内直接用，中文表现好 |
| Gemini CLI | `GEMINI.md` | [github.com/google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli) | Google 官方 |

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
/start-my-day     每日规划 + 学术动态推送
/end-my-day       每日复盘
/read              精读文献
/explore <概念>    概念溯源
/kickoff           想法→项目
/write             写作辅助
/research <主题>   学术调研
/brainstorm        头脑风暴
/organize          笔记整理
/ask <问题>        快速问答
/parse             知识解析（非结构化文本→笔记+卡片）
/archive           归档清理
```

---

## 常见问题

**Q: 需要会编程吗？**
A: 不需要。Claude Code 虽然运行在终端里，但交互全部用自然语言。详见 [Claude Code新手指南](99_系统/Claude%20Code新手指南.md)。

**Q: 数据安全吗？**
A: 你的所有笔记都存在本地电脑上。AI 交互时会将相关内容发送给 AI 服务商处理。

**Q: 可以在手机上查看吗？**
A: Obsidian 有移动端 App，可以随时查看和编辑笔记。同步方案见 [Obsidian新手指南](99_系统/Obsidian新手指南.md)。

**Q: 只适合文科生吗？**
A: 文渊为人文社科学术研究设计，所有工作流和模板都可以根据你的学科自由调整。详见 [文渊使用指南](99_系统/文渊使用指南.md)。

**Q: 遇到问题怎么办？**
A: 安装前可以在 ChatGPT 等 AI 对话工具中提问；安装好文渊后，直接在 Claude Code 中描述你的问题即可。

---

## 设计理念

文渊的设计灵感来源于 [OrbitOS](https://github.com/MarsWang42/OrbitOS) 框架与个人知识库构建实践，并为学术研究场景重新设计：

- **AI 即助手**：AI 不替代你的思考，而是引导和辅助
- **知识即网络**：通过双向链接将概念、文献、项目连成知识网络
- **简单即力量**：纯 Markdown 文件，不依赖复杂插件，不锁定平台
- **以人为本**：所有工作流围绕研究者的真实场景设计

---

## 开源协议

MIT License — 自由使用、修改、分发。
