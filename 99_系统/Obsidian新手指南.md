# Obsidian 新手指南

> 学会这些就足以使用文渊。更深入的学习可以参考末尾的社区资源。

---

## 什么是 Obsidian？

Obsidian 是一款**免费的本地笔记软件**，数据以纯 Markdown 文件存储在你自己电脑上。核心优势：数据属于你、双向链接构建知识网络、插件生态强大。

**安装：** [obsidian.md](https://obsidian.md/) → Download → 选择你的系统

---

## 你只需要掌握

### Markdown 基础
```markdown
# 一级标题
## 二级标题
**加粗** 和 *斜体*
- 列表项
> 引用
[[链接到其他笔记]]
```

### 双向链接
输入 `[[` 弹出笔记列表，选择即可创建链接。两边都能看到关联。

### 前置属性（Frontmatter）
文渊的笔记顶部有一块 `---` 包裹的属性区域，用来告诉 AI 这篇笔记是什么、属于哪个项目、当前状态等。你不需要每次手动写，AI 会自动添加。
```yaml
---
type: project          # 笔记类型（project/literature/concept等）
status: active         # 状态（active/completed/on-hold）
related: [[XX项目]]   # 关联到其他笔记
---
```

### 快捷键

| 操作 | 快捷键 |
|------|--------|
| 新建笔记 | `Cmd/Ctrl + N` |
| 快速搜索 | `Cmd/Ctrl + O` |
| 命令面板 | `Cmd/Ctrl + P` |
| 插入链接 | 输入 `[[` |

---

## 文渊必装插件

以下插件是文渊工作流正常运行所需要的，请在安装文渊后依次装上：

| 插件 | 用途 | 安装方法 |
|------|------|----------|
| **Terminal** (by polyipseity) | 在 Obsidian 内运行 Claude Code | 设置 → 第三方插件 → 浏览 → 搜 `Terminal` |

### Terminal 插件使用

1. `Cmd/Ctrl + P` 打开命令面板
2. 搜索 `Terminal: Open terminal`
3. 终端在底部打开，输入 `claude` 启动 AI
4. 建议把终端拖到侧边栏——左边笔记、右边 AI

---

## 推荐插件

按需选装，不装也能用文渊：

| 插件 | 用途 | 推荐度 |
|------|------|--------|
| **Web Clipper** | 一键剪藏网页到 vault | 建议 |
| **Calendar** | 日历视图查看日记 | 建议 |
| **Obsidian Git** | 自动备份到 GitHub | 建议 |
| **Editing Toolbar** | 类 Word 编辑栏，降低 Markdown 门槛 | 新手友好 |
| **Dataview** | 把笔记变成可查询的数据库 | 进阶 |
| **Templater** | 灵活的模板自动化 | 进阶 |
| **Excalidraw** | 手绘流程图、思维导图 | 进阶 |
| **ZotLit** | Zotero 文献管理集成 | 用 Zotero 的人 |
| **PDF++** | Obsidian 内阅读 PDF | 常读 PDF 的人 |

> 更多插件推荐：搜索 `Obsidian 必装插件 2026` 或访问 [PKMer 插件推荐](https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/)

### Web Clipper 使用

[Obsidian Web Clipper](https://obsidian.md/clipper) 是官方浏览器扩展，将网页一键保存为 Markdown。

- Chrome/Edge/Safari/Firefox 扩展商店搜 `Obsidian Web Clipper`
- 默认保存路径设为 `00_收件箱/`，剪藏后用 `/organize` 归类
- 典型场景：剪藏知网论文摘要、学术会议 CFP、在线文章

---

## AI Skills（给 AI 看的参考文档）

文渊内置了一些 Obsidian 技术相关的 AI 参考文档，帮助 AI 更好地使用 Obsidian 功能。这些文件位于 `.claude/skills/` 和 `.agents/skills/` 目录下：

**文渊内置：**

| Skill | 内容 |
|-------|------|
| `obsidian-markdown` | Obsidian 的 Markdown 语法指南 |
| `obsidian-bases` | Obsidian Bases（数据库视图）使用方法 |
| `json-canvas` | Obsidian Canvas（画布笔记）格式说明 |

**社区可选 Skills（与文渊工作流无关，按需安装）：**

这些是社区开发的 Obsidian 相关 AI 技能，可以增强 AI 在特定场景下的表现。它们不是 Obsidian 插件，而是给 AI 看的参考文档。

| Skill | 用途 | 安装命令 |
|-------|------|----------|
| obsidian-cli | 让 AI 用命令行管理 vault | `npx skills add kepano/obsidian-skills@obsidian-cli` |
| defuddle | 网页转干净 Markdown | `npx skills add kepano/obsidian-skills@defuddle` |
| excalidraw-diagram | AI 生成手绘图 | `npx skills add axtonliu/axton-obsidian-visual-skills@excalidraw-diagram` |
| canvas-creator | AI 创建 Canvas 画布 | `npx skills add axtonliu/axton-obsidian-visual-skills@obsidian-canvas-creator` |
| mermaid-visualizer | AI 生成流程图 | `npx skills add axtonliu/axton-obsidian-visual-skills@mermaid-visualizer` |

浏览更多：[skills.sh](https://skills.sh/) 搜索 `obsidian`

这些不是用户手动调用的命令，而是 AI 在需要时自动参考的文档。

---

## 多端同步

| 方案 | 适用场景 | 费用 |
|------|----------|------|
| iCloud | Mac + iPhone 用户 | 免费 |
| Obsidian Sync | 跨平台、最省心 | $4/月 |
| Remotely Save + 坚果云 | 国内用户 | 免费 |

**iCloud 同步设置：** 将文渊 vault 放到 iCloud 对应目录下：
```
Mac: ~/Library/Mobile Documents/iCloud~md~obsidian/Documents/文渊/
iPhone: 打开 Obsidian App → 就能看到 iCloud 中的文渊 vault
```

新手建议先在电脑上用起来，熟悉后再配置同步。

---

## 学习资源

- [Obsidian 官方中文帮助文档](https://help.obsidian.md/zh/)
- [PKMer 社区](https://pkmer.cn/) — 国内最活跃的 Obsidian 社区，有详细的插件和工作流教程
- B站搜索 `Obsidian 保姆级教程` 或 `Obsidian 新手指南`
- 少数派搜索 `Obsidian` — 高质量中文使用心得

---

## 常见问题

**Q: Obsidian 要付费吗？**
A: 个人使用完全免费。Obsidian Sync 和 Publish 是可选的付费服务。

**Q: 以前的笔记能迁移过来吗？**
A: Markdown 格式直接复制进来。Word 可以先转 Markdown（搜索 `Word 转 Markdown` 有在线工具）。复制进来后用 `/organize` 让 AI 帮你归类整理。

**Q: 文渊的文件结构可以改吗？**
A: 可以。详见 [[文渊使用指南#个性化定制]](文渊使用指南.md)。建议先跟 Claude Code 商量再改，避免打乱现有结构。
