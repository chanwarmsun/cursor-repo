个人网站产品需求文档
1. 文档信息
 * 项目名称: 个人展示与资源分享网站
 * 版本: 1.0
 * 创建日期: 2025年6月12日
 * 创建人: [warmsun]
 * 目标受众: 潜在雇主、同行、对AI智能体和提示词感兴趣的用户、Web开发初学者
2. 产品概述
本网站旨在构建一个个人展示与资源分享平台。它将以Bento Grid风格呈现，并模仿Apple官网的流畅动态效果，提供个人信息展示、智能体分发、提示词分享和HTML教学资源下载等核心功能。整体设计将注重用户体验，确保界面美观、交互丝滑。
3. 产品目标
 * 提升个人品牌和可见度,打造个人IP: 有效展示个人技能、项目和经验。
 * 促进AI智能体和提示词的分享与应用: 为用户提供方便的智能体和提示词获取渠道。
 * 赋能Web开发初学者: 提供实用的HTML教学资源。
 * 打造卓越的用户体验: 实现Bento Grid风格和Apple官网般的动态效果。
4. 用户画像
 * 潜在雇主/合作方: 希望快速了解我的个人背景、技能和项目。
 * AI爱好者/开发者: 寻找可用的智能体和高质量的提示词。
 * Web开发初学者: 寻求HTML学习资源和实践指导。
5. 功能需求
5.1. 个人信息展示 (核心功能)
 * 模块: 首页顶部横幅或单独区块。
 * 内容:
   * 个人照片/头像。
   * 姓名、职业/头衔。
   * 简短的个人介绍/Slogan（突出个人特色和技能）。
   * 指向简历（PDF下载）、GitHub、LinkedIn等外部链接。
   * 教育背景（可选）。
   * 专业技能（如编程语言、工具、设计软件等，可用图标或进度条展示）。
 * 设计要求:
   * Bento Grid中的一个大区块，醒目且易于访问。
   * 动画效果：滚动时信息渐入、技能条填充动画。
5.2. 全站信息搜索框 (核心功能)
 * 模块: 导航栏或固定在页面顶部。
 * 功能:
   * 用户输入关键词，搜索网站内的所有内容（包括智能体名称、提示词关键词、HTML教学资源标题等）。
   * 支持模糊搜索和关键词匹配。
   * 搜索结果应快速、准确地展示，并提供跳转链接。
 * 设计要求:
   * 搜索框样式简洁，带有搜索图标。
   * 聚焦时有平滑的展开动画。
   * 搜索结果展示卡片化，视觉清晰。
5.3. 智能体分发 (核心功能)
 * 模块: 独立的Bento Grid区块，名为“我的AI智能体”或类似。
 * 功能:
   * 展示多个“扣子”发布好的智能体卡片。
   * 每个卡片包含：
     * 智能体名称。
     * 简短描述。
     * 智能体图标/图片。
     * 核心：提供“打开使用”按钮。点击后可根据智能体类型，提供以下交互方式：
       * 如果智能体需要外部平台（如Botpress, Rasa等）: 弹出模态框，引导用户到相应平台并提供智能体ID或链接。
       * 如果智能体是纯文本/代码片段: 在网站内嵌入一个聊天框或代码运行环境供用户测试（如果技术可行且时间允许，否则以下载或复制代码为主）。
       * 如果智能体可下载: 提供下载链接。
 * 设计要求:
   * 每个智能体卡片应有精致的Bento Grid样式。
   * 卡片悬停时有微妙的动画效果（如放大、阴影变化）。
   * “打开使用”按钮应醒目，点击后有平滑的过渡动画。
5.4. 提示词收藏与下载 (核心功能)
 * 模块: 独立的Bento Grid区块，名为“精选提示词”或类似。
 * 功能:
   * 展示个人收藏的提示词列表。
   * 每个提示词条目包含：
     * 提示词标题/用途。
     * 简要说明/示例。
     * 核心：提供“下载”按钮（下载为.txt或.md文件）或“复制”按钮。
     * 可添加标签或分类，方便用户筛选。
 * 设计要求:
   * 提示词列表以卡片或列表形式展示，简洁明了。
   * 下载/复制按钮有明确的视觉提示。
   * 支持无限滚动或分页加载。
   * 悬停时卡片有轻微的放大或阴影变化。
5.5. HTML教学资源下载 (核心功能)
 * 模块: 独立的Bento Grid区块，名为“HTML学习区”或类似。
 * 功能:
   * 展示HTML教学资源列表（如电子书、代码示例、教程PDF等）。
   * 每个资源条目包含：
     * 资源标题。
     * 简要描述。
     * 核心：提供“下载”按钮。
   * 可添加资源类型（如教程、项目、速查表）或难度标签。
 * 设计要求:
   * 资源卡片样式统一，信息清晰。
   * 下载按钮突出。
   * 考虑未来扩展性，可能添加视频链接或在线预览。
6. 非功能性需求
6.1. 性能
 * 加载速度: 页面加载时间应在3秒以内。
 * 响应速度: 交互动画和页面切换应流畅，无卡顿。
 * 兼容性: 兼容主流浏览器（Chrome, Firefox, Safari, Edge）的最新两个版本。
 * 移动适配: 网站应具备良好的响应式设计，在不同尺寸的移动设备上展现良好。
6.2. 安全性
 * 数据安全: 若有用户数据（如访问统计），确保数据传输安全。
 * 内容安全: 确保上传的智能体和资源无恶意内容。
6.3. 可维护性与可扩展性
 * 代码结构: 代码应模块化、清晰，易于理解和维护。
 * 内容管理: 考虑未来内容的更新和增加，例如通过简单的配置文件或后台管理界面（若需要，可简化）。
 * 组件化: 尽可能使用可复用的组件，提高开发效率。
6.4. 用户体验 (UX)
 * Bento Grid风格: 采用清晰、有组织的Bento Grid布局，每个区块独立且美观。
 * 苹果官网丝滑动态效果:
   * 滚动动画: 元素随滚动渐入、视差滚动、卡片浮动等。
   * 悬停动画: 元素悬停时有微妙的放大、阴影变化、颜色渐变等效果。
   * 点击动画: 按钮点击、链接跳转时有平滑的过渡效果。
   * 全局动画: 导航栏、背景元素的微动。
 * 配色方案: 简洁、现代，可参考Apple官网的风格。
 * 字体: 选择清晰、易读的字体。
 * 导航: 导航清晰、直观，方便用户在不同模块之间切换。
7. 技术栈 (供Cursor参考，可根据实际情况调整)
 * 前端框架: React (推荐，便于实现复杂动画和组件化) / Vue.js / Next.js (如果需要SSR)
 * 动画库: Framer Motion / GSAP (用于实现苹果官网级别的丝滑动画)
 * CSS框架: Tailwind CSS (推荐，便于快速构建Bento Grid布局和响应式设计) / Styled Components
 * 图标库: React Icons / Font Awesome
 * 部署: Vercel / Netlify (便于CI/CD和静态网站部署)
 * 数据存储: 静态JSON文件 (对于智能体、提示词、HTML资源列表，最简单快捷) / Headless CMS (如Strapi, Sanity，如果内容量大且需要更便捷的管理)
8. 待确认事项 (Cursor开发者可就此进行沟通)
 * 智能体“打开使用”的具体实现方式：是否需要集成外部API？还是仅仅提供跳转链接/下载？
 * 提示词和HTML教学资源的具体文件格式和下载方式。
 * Bento Grid布局的具体设计稿或参考案例。
 * 动画效果的详细需求（如缓动曲线、持续时间等），最好能提供视频参考。
9. 成功指标
 * 网站上线并稳定运行。
 * 核心功能（个人信息展示、智能体分发、提示词下载、HTML资源下载）均可正常使用。
 * 用户访问量和停留时间达到预期。
 * Bento Grid风格和动画效果获得用户正面反馈。
