# Claude-like Typora Theme

> 一套安静、温暖、适合长时间阅读与写作的 Typora 主题。

## 阅读体验

Claude-like Theme 以低饱和的中性色为底，使用克制的陶土色作为视觉强调。舒展的行距与稳定的内容宽度，让中文长文和 mixed English content 都保持清晰的阅读节奏。

文字可以包含 **重点内容**、*轻量强调*、~~删除说明~~、==高亮片段==，也可以使用 `inline code` 标记命令或变量。

> [!NOTE]
> 主题同时优化了提示块、表格、代码、任务列表和文档导航。

## 功能概览

| 模块 | 设计目标 | 状态 |
| --- | --- | :---: |
| 正文与标题 | 清楚的层级和舒适的留白 | ✓ |
| 代码与表格 | 稳定、克制、易于扫描 | ✓ |
| 侧栏与目录 | 与文档区域保持统一 | ✓ |

### 今日任务

- [x] 完成明亮主题
- [x] 完成深色主题
- [x] 优化中英文混排
- [ ] 继续听取社区反馈

### 代码示例

```typescript
type Theme = "claude-light" | "claude-dark";

function activateTheme(theme: Theme): string {
  return `Typora theme activated: ${theme}`;
}

console.log(activateTheme("claude-light"));
```

## 数学与链接

行内公式 $E = mc^2$ 与独立公式都拥有清晰的排版：

$$
\int_{-\infty}^{\infty} e^{-x^2}\,dx = \sqrt{\pi}
$$

访问 [Typora](https://typora.io/) 了解更多 Markdown 写作功能。

---

愿每一次书写都专注于内容本身。
