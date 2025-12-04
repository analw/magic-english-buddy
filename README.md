<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />

# Magic English Buddy ✨

**专为儿童设计的 AI 英语阅读学习助手**

[![React](https://img.shields.io/badge/React-19-61DAFB?logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178C6?logo=typescript)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-6-646CFF?logo=vite)](https://vitejs.dev/)
[![Gemini](https://img.shields.io/badge/Gemini-AI-4285F4?logo=google)](https://ai.google.dev/)

</div>

---

## 📖 项目简介

Magic English Buddy 是一款面向小学生的英语阅读学习工具。通过 **语音合成(TTS)** 技术实现文本朗读，配合 **实时单词高亮** 功能，帮助孩子们在听读中学习英语发音和阅读。同时集成 **Google Gemini AI**，可根据孩子感兴趣的主题智能生成个性化英语故事，还支持 **OCR 文字识别**，拍照即可识别英语文本开始练习。

## ✨ 功能特点

### 📚 四种内容输入方式
- **手写模式** - 自由输入或粘贴任意英语文本
- **预设故事库** - 40+ 精选英语小故事（寓言、日常、科普、趣味）
- **AI 智能生成** - 输入主题，Gemini AI 自动生成适龄故事
- **📷 OCR 识别** - 拍照或从相册选图，自动识别提取英语文本

### 🎧 交互式阅读体验
- **全文朗读** - 一键播放整篇文章
- **实时高亮** - 朗读时当前单词高亮并自动滚动
- **点击发音** - 点击任意单词即可单独听发音
- **选中朗读** - 选中任意文本段落后可单独朗读

### ⚙️ 灵活的语音控制
- **语速调节** - 0.5x ~ 1.5x 自由调整
- **多语音选择** - 自动获取系统英语语音（优先本地语音）
- **播放控制** - 播放/暂停/停止
- **iOS 兼容** - 针对 iOS 设备特殊优化

### 🌍 其他特性
- **中英文界面** - 支持一键切换
- **响应式设计** - 完美适配手机和电脑
- **儿童友好 UI** - 色彩丰富，动画流畅
- **分享功能** - 一键生成分享链接，分享阅读内容
- **仅英文过滤** - 可选择过滤非英文字符

## 🛠️ 技术栈

| 类别 | 技术 |
|------|------|
| 前端框架 | React 19 |
| 开发语言 | TypeScript |
| 构建工具 | Vite 6 |
| AI 服务 | Google Gemini API |
| 语音合成 | Web Speech API |
| OCR 识别 | Tesseract.js |
| 国际化 | i18next |
| 样式方案 | Tailwind CSS |
| 图标库 | Lucide React |

## 📁 项目结构

```
magic-english-buddy/
├── components/              # React 组件
│   ├── Home.tsx            # 首页（内容输入）
│   ├── Player.tsx          # 播放器页面
│   ├── TextDisplay.tsx     # 文本展示组件
│   ├── Controls.tsx        # 播放控制组件
│   ├── CameraCapture.tsx   # 相机拍照/OCR 组件
│   └── StoryGenerator.tsx  # 故事生成组件
├── hooks/
│   └── useWebSpeech.ts     # Web Speech API Hook
├── services/
│   ├── geminiService.ts    # Gemini AI 服务
│   ├── ocrService.ts       # OCR 识别服务
│   └── tesseractWorker.ts  # Tesseract Worker 管理
├── data/
│   └── presets.ts          # 预设故事数据（40+篇）
├── App.tsx                 # 应用入口
├── types.ts                # TypeScript 类型定义
├── i18n.ts                 # 国际化配置
└── index.tsx               # 渲染入口
```

## 🚀 快速开始

### 环境要求

- Node.js 18+
- pnpm / npm / yarn

### 安装依赖

```bash
# 使用 pnpm（推荐）
pnpm install

# 或使用 npm
npm install
```

### 配置 API Key

1. 获取 [Google Gemini API Key](https://ai.google.dev/)
2. 在项目根目录创建 `.env.local` 文件：

```env
VITE_API_KEY=your_api_key_here
```

### 启动开发服务器

```bash
# 使用 pnpm
pnpm dev

# 或使用 npm
npm run dev
```

访问 http://localhost:5173 查看应用

### 构建生产版本

```bash
pnpm build
```

## 📖 使用指南

### 1️⃣ 选择内容

在首页选择四种方式之一获取阅读内容：

- **手写** - 直接输入英语文本
- **预设** - 从故事库选择（支持分类筛选）
- **AI 生成** - 输入主题 + 选择难度，点击生成
- **OCR 扫描** - 点击扫描按钮，拍照或选择图片识别文字

### 2️⃣ 开始练习

点击「开始练习」进入播放器页面

### 3️⃣ 交互学习

- 点击 **播放按钮** 开始全文朗读
- **点击单词** 听单个单词发音
- **选中文本** 后点击悬浮按钮朗读选中部分
- 使用控制面板调整 **语速** 和 **语音**

### 4️⃣ 分享内容

- 在首页或播放页点击 **分享按钮**
- 移动端会调起系统分享面板
- 桌面端会复制分享链接到剪贴板

### 🐛 调试模式

在 URL 后添加 `?debug=true` 可开启 TTS 调试面板，查看：
- 当前播放状态
- 语音引擎信息
- 字符索引和匹配的单词
- 事件触发时间

## 📄 许可证

MIT License

---

<div align="center">

**Made with ❤️ for kids learning English**

</div>
