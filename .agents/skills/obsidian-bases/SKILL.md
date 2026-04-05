---
name: obsidian-bases
description: Obsidian Bases — 创建数据库视图，使用 .base 文件进行笔记的过滤、排序和展示
---

# Obsidian Bases 数据库视图

Bases 是 Obsidian 内置的数据库功能（需要 Obsidian 1.8+），可以创建 `.base` 文件来以表格形式查看和管理笔记。

## .base 文件格式

`.base` 文件使用 JSON 格式，核心结构如下：

```json
{
  "folder": "30_文献",
  "filter": {
    "conjunction": "and",
    "conditions": [
      {
        "field": "status",
        "operator": "is",
        "value": "unread"
      }
    ]
  },
  "formulas": {
    "display_title": {
      "formula": "prop(\"title\")",
      "name": "标题",
      "type": "string"
    }
  },
  "order": [
    {
      "field": "year",
      "direction": "desc"
    }
  ],
  "columns": ["title", "author", "year", "status", "area"]
}
```

## 可用的操作符

### 过滤操作符
- `is` / `is-not` — 等于/不等于
- `contains` / `does-not-contain` — 包含/不包含
- `starts-with` / `ends-with` — 以...开头/结尾
- `is-empty` / `is-not-empty` — 为空/不为空
- `gt` / `lt` / `gte` / `lte` — 大于/小于/大于等于/小于等于

### 排序方向
- `asc` — 升序
- `desc` — 降序

## 公式语法

```
prop("属性名")              # 获取 frontmatter 属性
length(prop("tags"))        # 数组长度
if(condition, true, false)  # 条件判断
concat(str1, str2)          # 字符串拼接
now()                       # 当前时间
```

## 使用建议
- `.base` 文件放在 `99_系统/数据库/` 目录下
- 为不同的使用场景创建不同的视图（如：待读文献、活跃项目等）
- 利用 filter 快速切换视图内容
