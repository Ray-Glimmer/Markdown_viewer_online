# Markdown 渲染工具

一个本地打开即用的单文件 Markdown 渲染、格式化和导出工具。

## 使用

双击或用浏览器打开 `Markdown 渲染工具.html`。首次打开需要联网加载以下 CDN 依赖：

- marked
- DOMPurify
- highlight.js
- Mermaid

## 主要功能

- 左侧编辑 Markdown，右侧即时预览
- 宽容模式：自动修复常见残缺语法
- 智能换行：拆分行内标题、列表、分隔线等结构
- 绘图能力：`mermaid` 代码块可渲染流程图、框架图、时序图等
- 自动识别粘贴进来的裸 Mermaid 图表源码，并在格式化/宽容渲染时补成可渲染代码块
- 搜索源码和预览内容
- 打开/拖放 `.md` 文件
- 复制 Markdown、复制 HTML、导出完整 HTML
- 自动保存内容、开关和分栏宽度到浏览器 `localStorage`

## 快捷键

| 按键 | 作用 |
|------|------|
| Ctrl+S | 立即保存到本地 |
| Ctrl+O | 打开 Markdown 文件 |
| Ctrl+E | 导出 HTML |
| Ctrl+F | 聚焦源码搜索 |
| Ctrl+Shift+F | 格式化源码 |

## 开发与验证

这是单文件工具，没有构建步骤。改动后至少验证：

1. 浏览器打开 `Markdown 渲染工具.html`
2. 默认示例能渲染
3. 残缺 Markdown 能在宽容模式下显示修复提示
4. 裸 Mermaid 图表源码能在格式化后自动补成 `mermaid` 代码块
5. 搜索、格式化、复制、导出按钮可用

更多行为说明见 `docs/markdown-renderer.md`。
