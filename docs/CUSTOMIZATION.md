# Customizing Claude-like Typora Theme

[中文说明](#中文说明)

Typora loads user CSS after the selected theme. Keep your changes in user CSS so future theme updates can replace `claude-light.css` and `claude-dark.css` safely.

## Where to put overrides

Open `Preferences → Appearance → Open Theme Folder`, then create one of these files:

- `base.user.css` — applies to every Typora theme;
- `claude-light.user.css` — applies only to Claude Light;
- `claude-dark.user.css` — applies only to Claude Dark.

Restart Typora after creating a new user CSS file. Most later edits can be refreshed by switching themes.

## Change the accent

Use different readable text values in light and dark mode when needed:

```css
/* claude-light.user.css */
:root {
  --accent-color: #b66a4d;
  --accent-hover-color: #91472f;
  --accent-text-color: #91472f;
  --focus-color: #91472f;
}
```

```css
/* claude-dark.user.css */
:root {
  --accent-color: #d58b6f;
  --accent-hover-color: #ebb098;
  --accent-text-color: #ebb098;
  --focus-color: #ebb098;
}
```

## Change the writing width and rhythm

```css
#write {
  max-width: 820px;
  font-size: 1.025rem;
  line-height: 1.8;
}
```

The distributed theme uses a `752px` maximum width and `1.72` line height. Wider columns work well for tables and technical documents; narrower columns are often more comfortable for prose.

## Change body and code fonts

```css
:root {
  --font-body: "Source Han Sans SC", "PingFang SC", system-ui, sans-serif;
  --font-code: "Maple Mono", "JetBrains Mono", ui-monospace, monospace;
}
```

Only reference fonts already installed on your computer if you want the theme to remain offline and portable.

## Make text slightly larger on small screens

```css
@media screen and (max-width: 720px) {
  #write {
    font-size: 1.05rem;
    padding-inline: 1.25rem;
  }
}
```

## Restore a customization

Remove the relevant rule from the user CSS file. To restore every default, temporarily rename or delete the user CSS file and restart Typora. Avoid editing the distributed theme files unless you intend to maintain a permanent fork.

---

<a id="中文说明"></a>

## 中文说明

Typora 会在所选主题之后加载用户 CSS。建议把个性化设置放在以下文件中，避免主题升级时覆盖你的修改：

- `base.user.css`：对所有 Typora 主题生效；
- `claude-light.user.css`：只对 Claude Light 生效；
- `claude-dark.user.css`：只对 Claude Dark 生效。

这些文件位于 Typora 的主题文件夹中。可以通过 `设置 / 偏好设置 → 外观 → 打开主题文件夹` 打开。

上面的示例可以直接用于：

- 修改陶土色强调色和焦点颜色；
- 调整默认 `752px` 正文宽度与 `1.72` 行高；
- 更换已经安装在本机的正文或代码字体；
- 单独优化小窗口下的字号和左右留白。

如需恢复默认样式，只要移除对应覆盖规则即可。若要彻底排查自定义问题，可暂时重命名用户 CSS 文件并重启 Typora。

[Back to README](../README.md) · [返回中文 README](../README.zh-CN.md)
