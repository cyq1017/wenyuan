---
name: json-canvas
description: JSON Canvas — 创建可视化画布文件，用于思维导图和概念关系图
---

# JSON Canvas 画布文件

Obsidian 使用 `.canvas` 文件创建可视化画布，支持思维导图、概念关系图等。

## 文件格式

`.canvas` 文件使用 JSON 格式：

```json
{
  "nodes": [
    {
      "id": "node1",
      "type": "text",
      "x": 0,
      "y": 0,
      "width": 250,
      "height": 100,
      "text": "# 核心概念\n\n这是一个文本节点"
    },
    {
      "id": "node2",
      "type": "file",
      "x": 300,
      "y": 0,
      "width": 250,
      "height": 100,
      "file": "40_概念/文化资本.md"
    },
    {
      "id": "node3",
      "type": "link",
      "x": 0,
      "y": 200,
      "width": 250,
      "height": 100,
      "url": "https://example.com"
    }
  ],
  "edges": [
    {
      "id": "edge1",
      "fromNode": "node1",
      "toNode": "node2",
      "fromSide": "right",
      "toSide": "left",
      "label": "相关概念"
    }
  ]
}
```

## 节点类型

| 类型 | 说明 | 必需字段 |
|------|------|----------|
| `text` | 文本节点 | `text` |
| `file` | 文件引用 | `file` |
| `link` | 外部链接 | `url` |
| `group` | 分组框 | `label` |

## 节点属性

- `id`: 唯一标识符
- `x`, `y`: 位置坐标
- `width`, `height`: 尺寸
- `color`: 颜色（"1"~"6" 或十六进制）

## 边（连接线）属性

- `fromNode`, `toNode`: 连接的节点 ID
- `fromSide`, `toSide`: 连接方向（`top`, `right`, `bottom`, `left`）
- `label`: 连接线标签
- `fromEnd`, `toEnd`: 箭头样式（`none`, `arrow`）

## 使用场景
- 为论文项目创建概念关系图
- 梳理文献之间的引用关系
- 用思维导图规划论文结构
- 可视化学术理论流派图
