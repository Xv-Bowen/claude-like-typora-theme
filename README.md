# Claude-like Typora Theme

[简体中文](README.zh-CN.md) · English

A carefully engineered light-and-dark theme pair for Typora, inspired by the calm reading experience associated with Claude. Warm neutrals, restrained clay accents, and a complete application-shell treatment create a writing space that feels quiet without feeling unfinished.

This is more than a document color preset. Each variant contains roughly 3,400 lines of CSS covering typography, Markdown components, technical writing, navigation, editing modes, window chrome, responsive behavior, and print output.

## Preview

### Claude Light

![Claude Light preview](Image/claude-light-preview.png)

### Claude Dark

![Claude Dark preview](Image/claude-dark-preview.png)

## At a glance

| Area | What is included |
| --- | --- |
| Theme variants | Independently tuned light and dark palettes |
| Reading | 752 px content column, 1.72 line height, balanced headings and paragraphs |
| Markdown | Lists, tasks, tables, quotes, links, footnotes, TOC, YAML metadata |
| Technical writing | Inline code, fenced code, language labels, syntax highlighting, math, Mermaid |
| GFM content | Note, tip, important, warning, and caution alert blocks |
| Typora UI | Tabs, file list, file tree, outline, search, footer, menus, preferences, export panels |
| Editing modes | Source mode, focus mode, and typewriter mode refinements |
| Output | Print/PDF rules, page-break protection, and exact color handling |
| Accessibility | Visible focus states, readable contrast, responsive breakpoints, reduced-motion support |
| Dependencies | No CDN, web font, image, or network dependency in the theme CSS |

## Why this theme feels different

### Two palettes, not one palette inverted

Claude Light and Claude Dark share the same visual language, but their surfaces, borders, syntax colors, selections, shadows, and muted text are tuned independently. Dark mode uses warm charcoal rather than pure black; light mode uses a soft off-white rather than a stark white canvas.

| Token | Claude Light | Claude Dark |
| --- | --- | --- |
| Canvas | `#f9f9f7` | `#2d2d2b` |
| Raised surface | `#ffffff` | `#3d3d3a` |
| Primary text | `#2d2d2b` | `#f9f9f7` |
| Shared accent | `#cc7d5e` | `#cc7d5e` |

### Typography designed for sustained reading

The writing area uses a stable 752 px measure, generous line height, careful paragraph spacing, and a restrained heading scale. Chinese and mixed Chinese-English documents remain compact enough to scan while still having room to breathe.

The theme uses a system-first UI font stack and prefers JetBrains Mono for code when it is installed. Every font has local fallbacks, so the theme remains fully usable offline without bundling third-party font files.

### A complete Markdown component system

Common elements are treated as one coherent system rather than unrelated patches:

- headings from H1 through H6 with balanced wrapping;
- emphasis, deletion, underline, selection, and wavy highlight states;
- ordered, unordered, nested, and task lists with custom checkboxes;
- tables with deliberate header hierarchy, row feedback, borders, and editing controls;
- blockquotes and all five GitHub-style alert types;
- links, footnotes, table of contents, horizontal rules, and YAML metadata;
- images, figures, audio, video, embedded content, math, and diagrams.

### Code that belongs in the document

Inline code uses a lightweight label treatment. Fenced code blocks have their own surface, border, language label, focused state, and syntax palette. Source mode reuses the same visual logic so moving between rendered writing and Markdown source feels continuous.

The syntax system distinguishes comments, keywords, strings, numbers, tags, definitions, variables, and default code text without turning a document into an over-saturated IDE.

### Typora itself is part of the theme

The theme continues beyond `#write` and styles the surrounding application:

- top tabs, footer panels, context menus, scrollbars, and inputs;
- file list, file tree, root node, folder states, search results, and file indicators;
- outline hierarchy with connector lines, filtering, hover, and active states;
- in-document TOC with full-row interaction and readable hierarchy;
- integrated title bar, macOS traffic-light spacing, and Windows unibody adjustments;
- open/export interactions, preferences shell, and integrated menu refinements.

Subtle menu, tree, and panel transitions are included, while `prefers-reduced-motion` disables non-essential motion for users who request it.

### Thoughtful export and small-window behavior

Print rules preserve color, avoid breaking tables and code blocks across pages where possible, and keep headings with the content that follows them. Responsive breakpoints at 1440, 1200, 992, 768, and 720 px progressively protect the writing column and application layout on smaller windows.

## Installation

### Download the release

1. Open the [latest release](https://github.com/Xv-Bowen/claude-like-typora-theme/releases/latest).
2. Download and extract `claude-like-typora-theme-v1.0.0.zip`.
3. In Typora, open `Preferences → Appearance → Open Theme Folder`.
4. Copy `claude-light.css` and `claude-dark.css` into that folder.
5. Restart Typora.
6. Select `Claude Light` or `Claude Dark` from the Themes menu.

### Install from the repository

Copy the two files from [`Theme/`](Theme/) directly into Typora's theme folder, then restart Typora.

| Platform | Default theme folder |
| --- | --- |
| macOS | `~/Library/Application Support/abnerworks.Typora/themes` |
| Windows | `%APPDATA%\Typora\themes` |
| Linux | `~/.config/Typora/themes` |

No resource folder is required. Both CSS files are self-contained.

## Included files

```text
.
├── Theme/
│   ├── claude-light.css
│   └── claude-dark.css
├── Image/
│   ├── claude-light-preview.png
│   ├── claude-dark-preview.png
│   └── claude-like-xv-bowen-thumbnail.png
├── docs/
│   └── CUSTOMIZATION.md
├── CHANGELOG.md
├── LICENSE
├── README.md
├── README.zh-CN.md
└── preview.md
```

[`preview.md`](preview.md) is a reusable visual test document covering long-form text, alerts, tables, tasks, code, math, Mermaid, and footnotes.

## Customization

Typora loads `base.user.css` and theme-specific user CSS after the selected theme. This lets you change the accent, fonts, content width, or spacing without editing the distributed theme files.

See the [customization guide](docs/CUSTOMIZATION.md) for copy-ready examples.

## Compatibility and testing

- Designed and visually verified on macOS with the current desktop version of Typora.
- Includes explicit macOS integrated-window and traffic-light treatment.
- Includes Windows unibody selectors and multiple responsive breakpoints.
- Windows and Linux are not yet fully regression-tested; issue reports and screenshots are welcome.
- The theme relies on Typora's application DOM, so future Typora releases may require selector updates outside the document area.

## Feedback and contributions

Bug reports should include your Typora version, operating system, active theme variant, a screenshot, and a small Markdown sample when possible. Pull requests are welcome when they keep the light and dark variants visually aligned.

## License

Theme code and repository documentation are released under the [MIT License](LICENSE).

## Trademark notice

Claude is a trademark of Anthropic, PBC. This independent community theme is not affiliated with, endorsed by, or sponsored by Anthropic. “Claude-like” describes only its visual and reading-experience inspiration.
