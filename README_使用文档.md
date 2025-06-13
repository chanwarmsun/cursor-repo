# WarmSun 个人展示与资源分享网站

## 📋 项目概述

这是一个基于 React + TypeScript + Framer Motion + Tailwind CSS 构建的现代化个人展示网站，采用 Apple 风格的 Bento Grid 布局和丝滑动画效果。网站集成了个人信息展示、AI智能体分发、提示词分享、HTML教学资源下载等核心功能。

## ✨ 核心功能

### 🏠 个人信息展示
- **个人头像与基本信息**：动态头像、姓名、职业标题
- **技能展示**：带进度条的技能等级展示，支持动画效果
- **社交链接**：GitHub、LinkedIn、邮箱等社交媒体链接
- **简历下载**：一键下载PDF格式简历文件
- **响应式设计**：完美适配桌面端、平板和移动设备

### 🔍 全站搜索功能
- **智能搜索**：支持模糊搜索和关键词匹配
- **全局搜索**：搜索智能体、提示词、HTML资源等所有内容
- **实时结果**：输入即搜索，结果实时更新
- **搜索建议**：智能搜索建议和相关性排序

### 🤖 AI智能体分发
- **智能体展示**：精美卡片展示多个AI智能体
- **多种类型支持**：
  - 外部链接型：跳转到第三方平台使用
  - 下载型：直接下载智能体文件
- **详细信息**：每个智能体包含名称、描述、标签、使用说明
- **模态框预览**：点击查看详细信息和使用指南

### 💡 提示词收藏与下载
- **提示词库**：精选高质量提示词集合
- **分类标签**：按用途和类型分类管理
- **双重操作**：支持复制到剪贴板和下载为文件
- **使用统计**：显示下载次数和受欢迎程度
- **详细预览**：模态框显示完整提示词内容

### 📚 HTML教学资源下载
- **资源分类**：教程、项目、速查表、电子书等多种类型
- **难度标识**：初级、中级、高级难度分级
- **评分系统**：用户评分和评价展示
- **下载统计**：实时下载次数统计
- **资源预览**：详细的资源信息和使用说明

### 🎨 用户体验特性
- **Apple风格动画**：丝滑的滚动动画、悬停效果、点击反馈
- **主题切换**：支持明暗主题切换，带圆形遮罩动画
- **响应式布局**：移动优先的响应式设计
- **性能优化**：GPU加速动画、懒加载、内存管理
- **无障碍支持**：键盘导航、屏幕阅读器支持

## 🛠 技术栈

### 前端框架
- **React 18.2.0**：现代化React框架
- **TypeScript**：类型安全的JavaScript超集
- **Vite**：快速的构建工具和开发服务器

### 样式与动画
- **Tailwind CSS 3.3.6**：实用优先的CSS框架
- **Framer Motion 10.16.16**：强大的React动画库
- **React Icons 4.12.0**：丰富的图标库

### 功能库
- **Fuse.js 7.0.0**：模糊搜索引擎
- **clsx & tailwind-merge**：条件样式管理

### 开发工具
- **ESLint**：代码质量检查
- **PostCSS & Autoprefixer**：CSS后处理
- **TypeScript编译器**：类型检查

## 📦 安装与运行

### 环境要求
- Node.js >= 16.0.0
- npm >= 8.0.0 或 yarn >= 1.22.0

### 安装步骤

1. **克隆项目**
```bash
git clone <项目地址>
cd 个人网站
```

2. **安装依赖**
```bash
npm install
# 或
yarn install
```

3. **启动开发服务器**
```bash
npm run dev
# 或
yarn dev
```

4. **访问网站**
打开浏览器访问 `http://localhost:3000`

### 其他命令

```bash
# 构建生产版本
npm run build

# 预览生产版本
npm run preview

# 代码检查
npm run lint

# 类型检查
npm run type-check
```

## 🚀 部署指南

### Vercel 部署（推荐）

1. **连接GitHub**
   - 登录 [Vercel](https://vercel.com)
   - 连接GitHub账户
   - 导入项目仓库

2. **配置构建**
   - Framework Preset: `Vite`
   - Build Command: `npm run build`
   - Output Directory: `dist`

3. **环境变量**（如需要）
   ```
   NODE_ENV=production
   ```

4. **自动部署**
   - 推送到main分支自动触发部署
   - 支持预览部署和生产部署

### Netlify 部署

1. **连接仓库**
   - 登录 [Netlify](https://netlify.com)
   - 选择"New site from Git"
   - 连接GitHub仓库

2. **构建设置**
   ```
   Build command: npm run build
   Publish directory: dist
   ```

3. **部署配置**
   创建 `netlify.toml` 文件：
   ```toml
   [build]
     publish = "dist"
     command = "npm run build"

   [[redirects]]
     from = "/*"
     to = "/index.html"
     status = 200
   ```

### 传统服务器部署

1. **构建项目**
```bash
npm run build
```

2. **上传文件**
将 `dist` 目录中的所有文件上传到服务器

3. **配置服务器**
配置服务器支持SPA路由（所有路由指向index.html）

## 📝 使用指南

### 内容管理

#### 修改个人信息
编辑 `src/components/Hero.tsx`：
```typescript
// 修改个人信息
const personalInfo = {
  name: "你的姓名",
  title: "你的职业",
  description: "个人简介",
  skills: [
    { name: 'React', level: 95, icon: '⚛️' },
    // 添加更多技能
  ]
}
```

#### 添加智能体
编辑 `src/data/agents.ts`：
```typescript
export const agents: Agent[] = [
  {
    id: 'new-agent',
    name: '新智能体',
    description: '智能体描述',
    type: 'external', // 或 'download'
    link: 'https://example.com', // 外部链接
    // downloadUrl: '/files/agent.zip', // 下载链接
    tags: ['标签1', '标签2'],
    // ... 其他属性
  }
]
```

#### 添加提示词
编辑 `src/data/prompts.ts`：
```typescript
export const prompts: Prompt[] = [
  {
    id: 'new-prompt',
    title: '新提示词',
    description: '提示词描述',
    content: '完整的提示词内容',
    category: '分类',
    tags: ['标签1', '标签2'],
    // ... 其他属性
  }
]
```

#### 添加学习资源
编辑 `src/data/resources.ts`：
```typescript
export const resources: Resource[] = [
  {
    id: 'new-resource',
    title: '新资源',
    description: '资源描述',
    type: 'tutorial', // 'project', 'cheatsheet', 'ebook'
    difficulty: 'beginner', // 'intermediate', 'advanced'
    downloadUrl: '/files/resource.zip',
    // ... 其他属性
  }
]
```

### 主题定制

#### 修改颜色主题
编辑 `tailwind.config.js`：
```javascript
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: {
          50: '#eff6ff',
          500: '#3b82f6',
          900: '#1e3a8a',
        }
      }
    }
  }
}
```

#### 自定义动画
编辑 `src/index.css`：
```css
@keyframes customAnimation {
  0% { transform: translateY(0); }
  100% { transform: translateY(-10px); }
}

.custom-animation {
  animation: customAnimation 2s ease-in-out infinite;
}
```

### 性能优化

#### 图片优化
- 使用WebP格式图片
- 添加图片懒加载
- 压缩图片文件大小

#### 代码分割
```typescript
// 使用React.lazy进行代码分割
const LazyComponent = React.lazy(() => import('./LazyComponent'))

// 使用Suspense包装
<Suspense fallback={<LoadingSpinner />}>
  <LazyComponent />
</Suspense>
```

## 🔧 常见问题

### Q: 开发服务器启动失败
A: 检查Node.js版本是否>=16，删除node_modules重新安装依赖

### Q: 动画效果不流畅
A: 检查是否启用了GPU加速，减少同时运行的动画数量

### Q: 移动端显示异常
A: 检查CSS媒体查询，确保响应式断点设置正确

### Q: 搜索功能不工作
A: 检查SearchContext是否正确包装App组件

### Q: 下载功能失效
A: 检查文件路径是否正确，服务器是否支持文件下载

## 📄 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 🤝 贡献指南

1. Fork 项目
2. 创建功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📞 联系方式

- 作者：WarmSun
- 邮箱：warmsun@example.com
- GitHub：[@warmsun](https://github.com/warmsun)

---

**享受使用这个现代化的个人展示网站！** 🎉 