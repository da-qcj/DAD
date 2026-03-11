# OpenClaw 培训手册 - 静态网站

一个专业的 OpenClau 培训知识库网站，采用纯 HTML + CSS + JavaScript 实现，无需后端服务，可直接在浏览器中打开使用。

## 📋 功能特性

### 核心功能
- **响应式布局**：适配桌面端和移动端
- **章节导航**：左侧可折叠的章节树形导航
- **内容展示**：专业的排版和样式
- **搜索功能**：实时搜索章节标题和内容
- **主题切换**：支持浅色/深色模式
- **键盘快捷键**：Ctrl/Cmd + K 快速聚焦搜索框

### UI/UX 特性
- 精致的渐变设计和阴影效果
- 平滑的过渡动画
- 专业的代码高亮样式
- 丰富的图标使用（FontAwesome）
- 清晰的信息层级和视觉引导

## 🚀 快速开始

### 方法一：直接打开
1. 双击 `index.html` 文件
2. 在浏览器中自动打开

### 方法二：本地服务器
```bash
# 使用 Python
python -m http.server 8000

# 使用 Node.js
npx serve

# 然后访问 http://localhost:8000
```

## 📁 项目结构

```
oc-prj/
├── index.html          # 主文件（包含所有逻辑）
├── README.md           # 项目说明
└── assets/            # 资源目录（可选）
    └── content/       # 章节内容（如果需要扩展）
```

## 🎨 技术栈

- **HTML5**：语义化标签，结构清晰
- **CSS3**：Grid 布局，Flexbox，CSS 变量，动画
- **JavaScript (ES6+)**：模块化，事件处理，状态管理
- **外部依赖**：
  - Google Fonts（Noto Sans SC, JetBrains Mono）
  - FontAwesome（图标）
  - 无框架依赖，纯原生实现

## 📖 内容结构

### 三大章节部分
1. **基础与架构** (Part 01)
   - OpenClaw 核心概念
   - 系统架构设计
   - 安装与配置

2. **配置与开发** (Part 02)
   - 四大配置文件详解
   - Agent 创建与管理
   - Skill 系统开发

3. **应用与进阶** (Part 03)
   - 多 Agent 协作
   - 企业应用场景
   - 最佳实践与安全

### 章节统计
- 总章节数：44
- Part 01：19章
- Part 02：15章
- Part 03：10章

## 🎯 使用指南

### 导航使用
- **顶部菜单**：快速跳转到主要章节部分
- **左侧导航**：详细的章节树形导航，可点击展开/收起
- **面包屑**：显示当前所在位置，可点击返回上级

### 搜索使用
1. 点击顶部搜索框或使用快捷键 `Ctrl/Cmd + K`
2. 输入关键词进行实时搜索
3. 点击搜索结果跳转到对应章节

### 主题切换
- 点击顶部导航栏的月亮/太阳图标
- 在浅色和深色主题之间切换
- 主题偏好会自动保存（基于 CSS 变量）

## 🔧 自定义配置

### 修改主题颜色
在 `<style>` 标签中找到 `:root` 部分，修改 CSS 变量：

```css
:root {
    --primary-color: #1e40af;      /* 主色调 */
    --primary-light: #3b82f6;      /* 浅色变体 */
    --secondary-color: #0f172a;    /* 次要色 */
    --accent-color: #f59e0b;       /* 强调色 */
    /* ... */
}
```

### 添加新章节
在 `<script>` 标签中的 `chapters` 对象中添加：

```javascript
part1: {
    title: "基础与架构",
    chapters: [
        {
            id: "1.1",
            title: "新章节标题",
            content: `<h1>章节标题</h1><p>章节内容...</p>`
        }
    ]
}
```

### 修改布局尺寸
在 `:root` 中修改布局变量：

```css
:root {
    --sidebar-width: 280px;       /* 侧边栏宽度 */
    --header-height: 64px;        /* 顶部导航高度 */
    --footer-height: 48px;        /* 页脚高度 */
}
```

## 🌐 浏览器兼容性

- ✅ Chrome/Edge 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Opera 76+

## 📝 注意事项

1. **纯静态文件**：无需后端服务，可直接部署到静态托管平台
2. **CDN 依赖**：需要网络连接加载字体和图标（可选本地化）
3. **本地文件**：图片和资源建议使用相对路径或 Base64 编码
4. **HTTPS**：部署到生产环境建议使用 HTTPS

## 🚢 部署选项

### GitHub Pages
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/your-username/your-repo.git
git push -u origin main
```

### Netlify
直接拖拽文件夹到 Netlify 部署

### Vercel
连接 GitHub 仓库自动部署

### 其他静态托管
- Cloudflare Pages
- AWS S3 + CloudFront
- 阿里云 OSS + CDN

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📄 许可证

MIT License

## 🔗 相关链接

- [OpenClaw 官方文档](https://docs.openclaw.ai)
- [OpenClaw GitHub](https://github.com/openclaw/openclaw)
- [OpenClaw 社区](https://discord.gg/clawd)

---

**© 2026 OpenClaw Foundation | 从聊天机器人到数字员工**