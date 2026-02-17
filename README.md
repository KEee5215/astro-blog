# 🚀 Astro Blog

一个基于 **Astro** 框架构建的轻量级、高性能个人博客项目。本项目旨在记录编程学习之旅，分享技术心得与算法笔记。

🌐 **在线预览**: [keee-blog.netlify.app](https://keee-blog.netlify.app/blog/)
💻 **源代码**: [GitHub Repository](https://github.com/KEee5215/astro-blog)

## ✨ 项目特色

- **⚡️ 极速性能**: 利用 Astro 的零 JavaScript 默认输出（Zero JS by default），确保页面加载速度极快。
- **📝 内容优先**: 支持 Markdown (`.md`) 和 Astro 组件 (`.astro`) 混合编写，专注于内容创作。
- **🎨 简洁设计**: 采用极简主义设计风格，提供舒适的阅读体验。
- **🔧 易于部署**: 完美适配 Netlify 等静态站点托管平台，一键部署。
- **📱 响应式布局**: 完美适配桌面端与移动端设备。

## 🛠 技术栈

- **框架**: [Astro](https://astro.build/) - 现代静态站点生成器
- **包管理器**: [pnpm](https://pnpm.io/)
- **部署平台**: [Netlify](https://www.netlify.com/)
- **语言**: Markdown, Astro Components

## 📂 项目结构

```text
/
├── public/              # 静态资源（如图片、favicon等）
├── src/
│   ├── components/      # 可复用的 UI 组件 (Astro/React/Vue等)
│   ├── layouts/         # 页面布局模板
│   └── pages/           # 页面路由 (.astro 或 .md 文件)
│       ├── index.astro  # 首页
│       ├── blog/        # 博客列表页
│       └── posts/       # 具体文章详情
├── package.json         # 项目依赖配置
└── README.md            # 项目说明文档
```

Astro 会自动将 `src/pages/` 目录下的文件转换为基于文件名的路由。

## 🚀 快速开始

### 前置要求

- Node.js (v18.14.1 或更高版本)
- pnpm

### 安装与运行

1. **克隆项目**
   ```bash
   git clone https://github.com/KEee5215/astro-blog.git
   cd astro-blog
   ```

2. **安装依赖**
   ```bash
   pnpm install
   ```

3. **启动本地开发服务器**
   ```bash
   pnpm dev
   ```
   访问 `http://localhost:4321` 预览博客。

4. **构建生产版本**
   ```bash
   pnpm build
   ```
   构建产物将输出到 `./dist/` 目录。

5. **本地预览生产构建**
   ```bash
   pnpm preview
   ```

## 📄 常用命令

| 命令 | 描述 |
| :--- | :--- |
| `pnpm install` | 安装项目依赖 |
| `pnpm dev` | 启动本地开发服务器 |
| `pnpm build` | 构建生产环境静态站点 |
| `pnpm preview` | 本地预览构建后的站点 |
| `pnpm astro ...` | 运行 Astro CLI 命令 (如 `astro add`, `astro check`) |

## 📝 博客内容

本博客主要包含以下类别的文章：
- **框架学习**: 如 Astro 框架的初试与搭建总结。
- **算法笔记**: 数据结构与算法的学习记录（例如：二叉树的遍历）。
- **编程随笔**: 记录日常编程学习中的感悟与技巧。

## 🤝 贡献

欢迎提交 Issue 或 Pull Request 来改进这个项目！

## 📄 许可证

MIT License © 2026 KEee

---

> 💡 **提示**: 如果你是一名经验丰富的开发者，可以删除此文件中的默认说明部分，根据实际需求进行定制。更多详情请参阅 [Astro 官方文档](https://docs.astro.build/)。
