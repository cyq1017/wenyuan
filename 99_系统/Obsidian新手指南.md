# Obsidian 新手指南

> 面向零基础用户的 Obsidian 入门指南。学会这些就足以使用文渊。

---

## 什么是 Obsidian？

Obsidian 是一款**免费的本地笔记软件**，你的所有资料以纯文本（Markdown）格式存储在自己电脑上——没有云端，没有订阅，数据完全属于你。

**为什么选 Obsidian？**
- 数据本地化，不怕平台倒闭或数据丢失
- 双向链接，把知识连成网络
- 社区插件丰富，可以无限扩展
- 配合 AI 工具（如 Claude Code），变成智能学术助手

---

## 安装 Obsidian

1. 打开 [obsidian.md](https://obsidian.md/)
2. 点击 **Download**，选择你的系统（Mac / Windows / Linux）
3. 安装并打开

---

## 核心概念

### 仓库（Vault）
一个文件夹 = 一个仓库。文渊就是一个预配置好的仓库。

### Markdown
Obsidian 使用 Markdown 格式写笔记，语法非常简单：

```markdown
# 一级标题
## 二级标题

**加粗** 和 *斜体*

- 列表项 1
- 列表项 2

> 引用

[[链接到其他笔记]]
```

### 双向链接
这是 Obsidian 最强大的功能。输入 `[[` 就会弹出笔记列表，选择即可创建链接。

例如：在文献笔记中写 `[[文化资本]]`，就和概念卡片建立了双向链接，两边都能看到关联。

### 前置属性（Frontmatter）
文渊的笔记顶部有一段 `---` 包裹的属性区域：

```yaml
---
type: project
status: active
---
```

这些属性帮助 AI 理解和管理你的笔记（比如识别哪些项目是活跃的）。

---

## 基本操作

| 操作 | 快捷键 |
|------|--------|
| 新建笔记 | `Cmd/Ctrl + N` |
| 搜索笔记 | `Cmd/Ctrl + O` (快速切换) |
| 命令面板 | `Cmd/Ctrl + P` |
| 插入链接 | 输入 `[[` |
| 分栏查看 | 拖拽标签页到侧边 |

---

## 必装插件：Terminal

文渊 = Obsidian + Claude Code。要在 Obsidian 内使用 Claude Code，你需要安装 Terminal 插件。

### 安装步骤

1. 打开 Obsidian → **设置**（左下角齿轮图标）
2. 左侧选择 **第三方插件**
3. 关闭"安全模式"（第一次需要确认）
4. 点击 **浏览** → 搜索 `Terminal`
5. 找到 **Terminal** (by polyipseity) → 点击 **安装** → **启用**

### 使用方法

1. `Cmd/Ctrl + P` 打开命令面板
2. 搜索 `Terminal: Open terminal`
3. 终端会在 Obsidian 底部打开
4. 输入 `claude` 启动 AI 助手
5. 现在可以一边看笔记，一边和 AI 对话了

**建议：** 把终端拖到侧边栏，这样左边看笔记、右边和 AI 对话。

---

## 推荐安装的插件

以下插件**按需选装**，不装也能正常使用文渊：

| 插件 | 用途 | 优先级 |
|------|------|--------|
| **Terminal** | 在 Obsidian 内运行 Claude Code | 必装 |
| **Web Clipper** | 一键剪藏网页内容到 vault（论文、文章、资料） | 建议 |
| **Calendar** | 日历视图查看日记 | 建议 |
| **Obsidian Git** | 自动备份笔记到 GitHub | 建议 |
| **Dataview** | 把笔记变成可查询的数据库 | 进阶 |
| **Templater** | 更灵活的模板系统 | 进阶 |
| **ZotLit** | Zotero 文献管理集成 | 用 Zotero 的人 |
| **PDF++** | 在 Obsidian 内阅读 PDF | 常读 PDF 的人 |

### Web Clipper 使用说明

[Obsidian Web Clipper](https://obsidian.md/clipper) 是 Obsidian 官方出品的浏览器扩展，可以将网页内容一键保存为 Markdown 笔记到你的 vault。

**安装：**
1. 在 Chrome/Edge/Safari/Firefox 的扩展商店搜索 `Obsidian Web Clipper`
2. 安装后点击扩展图标，设置保存目标为你的文渊 vault

**学术使用场景：**
- 看到一篇有价值的在线论文/文章 → 一键剪藏到 `00_收件箱/`
- 浏览学术会议网站 → 剪藏 CFP 到 `50_资源/期刊动态/`
- 在知网/Google Scholar 找到文献 → 剪藏摘要信息到 `30_文献/`

**建议配置：**
- 默认保存路径设为 `00_收件箱/`（剪藏后再用 `/organize` 归类）
- 模板中加入 frontmatter：`type: inbox` + `status: unprocessed`

---

## 学习资源

- [Obsidian 官方中文帮助文档](https://help.obsidian.md/zh/)
- [PKMer 社区](https://pkmer.cn/) — 国内最活跃的 Obsidian 社区，有详细的插件教程
- B站搜索 `Obsidian 保姆级教程` 或 `Obsidian 新手指南`

---

## 多端同步

如果你想在手机上也能查看笔记：

| 方案 | 适用场景 | 费用 |
|------|----------|------|
| iCloud | Mac + iPhone 用户 | 免费 |
| Obsidian Sync | 跨平台、最省心 | $4/月 |
| Remotely Save 插件 + 坚果云 | 国内用户 | 免费 |

**新手建议：** 先在电脑上用起来，等熟悉后再考虑同步。

---

## 常见问题

**Q: Obsidian 要付费吗？**
A: 个人使用完全免费。只有 Obsidian Sync（同步服务）和 Publish（发布服务）是付费的，但你不一定需要它们。

**Q: 我以前的笔记能迁移过来吗？**
A: 如果是纯文本或 Markdown 格式，直接复制到文渊文件夹即可。Word 文档可以先转成 Markdown（有很多在线工具）。

**Q: 文件夹结构可以改吗？**
A: 可以，但建议先按文渊默认结构用一段时间，熟悉后再根据自己习惯调整。
