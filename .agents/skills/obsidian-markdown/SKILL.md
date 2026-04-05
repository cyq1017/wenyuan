---
name: obsidian-markdown
description: Obsidian Markdown — Obsidian 风格 Markdown 语法指南，包含 wikilinks、callouts、嵌入等
---

# Obsidian Markdown 语法指南

在文渊系统中创建和编辑笔记时，遵循以下 Obsidian Markdown 语法。

## Wikilinks（内部链接）

```markdown
[[笔记名]]                    # 基本链接
[[笔记名|显示文本]]            # 自定义显示文本
[[笔记名#章节名]]              # 链接到特定章节
[[笔记名#章节名|显示文本]]      # 链接到特定章节并自定义显示
![[笔记名]]                   # 嵌入整个笔记
![[笔记名#章节名]]             # 嵌入指定章节
![[图片.png]]                 # 嵌入图片
![[图片.png|300]]             # 嵌入图片并指定宽度
```

**使用原则**：大量使用 wikilinks 建立知识连接。每当提到一个概念、文献或论文项目时，都应该创建链接。

## Callouts（提示框）

```markdown
> [!note] 标题
> 笔记内容

> [!tip] 小贴士
> 提示内容

> [!warning] 注意
> 警告内容

> [!quote] 引用
> 引用内容

> [!question] 问题
> 还未解决的问题

> [!example] 示例
> 示例内容
```

可折叠 callout：
```markdown
> [!note]- 点击展开
> 折叠的内容

> [!note]+ 默认展开
> 展开的内容
```

## 标签

```markdown
#标签名
#学科/子领域
```

## 任务列表

```markdown
- [ ] 未完成任务
- [x] 已完成任务
- [/] 进行中（自定义状态，需要插件支持）
```

## Frontmatter（元数据）

```yaml
---
type: literature
title: "论文标题"
status: active
tags: [标签1, 标签2]
area: "[[领域名]]"
---
```

**重要规则**：`---` 结束标记后不要留空行，否则空行会显示在正文中。

## 脚注

```markdown
这是一段正文[^1]。

[^1]: 这是脚注内容。
```

## 数学公式

```markdown
行内公式：$E = mc^2$
块级公式：
$$
\int_0^\infty f(x) dx
$$
```

## 表格

```markdown
| 列1 | 列2 | 列3 |
|-----|-----|-----|
| 内容 | 内容 | 内容 |
```
