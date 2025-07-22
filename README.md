# AI Prompt Generator

<div align="center">

![AI Prompt Generator](https://img.shields.io/badge/AI-Prompt%20Generator-blue?style=for-the-badge&logo=openai)
![Vue 3](https://img.shields.io/badge/Vue-3.4.0-4FC08D?style=for-the-badge&logo=vue.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5.3.0-3178C6?style=for-the-badge&logo=typescript)
![Vite](https://img.shields.io/badge/Vite-5.0.0-646CFF?style=for-the-badge&logo=vite)

**将简单的想法转换为专业的 AI 提示词，为你的创意提供无限可能**

[在线演示](#) | [快速开始](#快速开始) | [功能特性](#功能特性) | [API 文档](#api文档)

</div>

## 📖 项目简介

AI Prompt Generator 是一个现代化的 Web 应用，专门用于将用户的简单想法转换为结构化、专业的 AI 提示词。通过智能分析和增强，帮助用户获得更好的 AI 响应效果。

### ✨ 核心价值

-   🚀 **提升效率**: 快速将简单想法转换为专业提示词
-   🎯 **精准优化**: 基于场景智能分析，提供针对性增强
-   💡 **创意激发**: 结构化的提示词模板激发更多创意可能
-   🔒 **隐私安全**: 数据加密传输，保护用户隐私

## 🎯 功能特性

### 🤖 智能提示词增强

-   **场景识别**: 自动识别写作、编程、分析、创意等不同场景
-   **结构化输出**: 生成包含角色设定、任务描述、执行标准的完整提示词
-   **多模板支持**: 针对不同场景提供专业模板
-   **实时预览**: 支持 Markdown 渲染和源码查看

### 📚 历史记录管理

-   **智能存储**: 自动保存生成历史，支持本地持久化
-   **快速检索**: 弹框式历史记录，支持快速查找和重用
-   **精确管理**: 支持单条删除和批量清空
-   **智能时间**: 人性化的时间显示（今天、昨天、几天前）

### ⚙️ 个性化设置

-   **API 配置**: 支持自定义 API 端点、模型和密钥
-   **界面定制**: 可调整预览模式、历史记录数量等
-   **数据管理**: 灵活的自动保存和数据清理选项

### 🎨 现代化界面

-   **响应式设计**: 完美适配桌面端和移动端
-   **毛玻璃效果**: 现代化的视觉设计和动画效果
-   **直观交互**: 流畅的用户体验和操作反馈
-   **无障碍支持**: 符合 Web 无障碍标准

## 🚀 快速开始

### 环境要求

-   Node.js >= 16.0.0
-   npm >= 7.0.0 或 yarn >= 1.22.0

### 安装步骤

1. **克隆项目**

    ```bash
    git clone https://github.com/your-username/ai-prompt-generator.git
    cd ai-prompt-generator
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

4. **访问应用**

    打开浏览器访问 `http://localhost:3000`

### 构建部署

```bash
# 构建生产版本
npm run build

# 预览构建结果
npm run preview
```

## 🏗️ 项目结构

```
ai-prompt-generator/
├── public/                 # 静态资源
├── src/
│   ├── components/         # Vue组件
│   │   ├── PromptGenerator.vue    # 主组件
│   │   ├── SettingsModal.vue      # 设置弹框
│   │   └── HistoryModal.vue       # 历史记录弹框
│   ├── services/          # 服务层
│   │   └── aiService.ts   # AI服务接口
│   ├── types/             # TypeScript类型定义
│   │   └── index.ts
│   ├── App.vue            # 根组件
│   └── main.ts            # 应用入口
├── index.html             # HTML模板
├── package.json           # 项目配置
├── tsconfig.json          # TypeScript配置
├── vite.config.ts         # Vite配置
└── README.md              # 项目文档
```

## 🔧 技术栈

### 前端框架

-   **Vue 3.4.0**: 渐进式 JavaScript 框架
-   **TypeScript 5.3.0**: 类型安全的 JavaScript 超集
-   **Vite 5.0.0**: 下一代前端构建工具

### 核心依赖

-   **@vueuse/core**: Vue 组合式 API 工具集
-   **axios**: HTTP 客户端（已移除，使用原生 fetch）

### 开发工具

-   **vue-tsc**: Vue TypeScript 编译器
-   **@vitejs/plugin-vue**: Vue 单文件组件支持

## 📡 API 文档

### AIService 类

#### 构造函数

```typescript
constructor(config?: Partial<ApiConfig>)
```

#### 主要方法

##### enhancePrompt

增强用户输入的提示词

```typescript
async enhancePrompt(request: PromptRequest): Promise<PromptResponse>
```

**参数:**

-   `request.input`: 用户输入的原始提示词
-   `request.apiKey`: 可选的 API 密钥

**返回值:**

-   `enhanced`: 增强后的提示词
-   `original`: 原始输入

### 类型定义

```typescript
interface PromptRequest {
    input: string
    apiKey?: string
}

interface PromptResponse {
    enhanced: string
    original: string
}

interface ApiConfig {
    endpoint: string
    model: string
    apiKey: string
}
```

## 🎨 界面设计

### 设计理念

-   **现代简约**: 采用现代化的设计语言，界面简洁直观
-   **渐变美学**: 紫色渐变背景，营造科技感氛围
-   **毛玻璃效果**: 半透明背景和模糊效果，增强视觉层次
-   **流畅动画**: 丰富的交互动画，提升用户体验

### 响应式布局

-   **桌面端**: 宽屏布局，充分利用屏幕空间
-   **平板端**: 自适应布局，保持良好的可读性
-   **移动端**: 单列布局，优化触摸操作

### 色彩方案

-   **主色调**: 渐变紫色 (#667eea → #764ba2)
-   **辅助色**: 白色、灰色系
-   **强调色**: 蓝色、绿色、红色（用于不同状态）

## 🔒 隐私与安全

### 数据处理

-   **加密传输**: 所有 API 请求使用 HTTPS 加密传输
-   **本地存储**: 历史记录和设置保存在浏览器本地
-   **无服务器存储**: 不在服务器端存储用户数据

### API 安全

-   **密钥保护**: API 密钥仅在客户端使用，不会泄露
-   **请求验证**: 所有 API 请求都经过身份验证
-   **错误处理**: 完善的错误处理机制，防止信息泄露

## 🚀 部署指南

### Vercel 部署

1. 连接 GitHub 仓库到 Vercel
2. 配置构建命令: `npm run build`
3. 配置输出目录: `dist`
4. 部署完成

### Netlify 部署

1. 连接 GitHub 仓库到 Netlify
2. 构建命令: `npm run build`
3. 发布目录: `dist`
4. 部署完成

### 自定义服务器

```bash
# 构建项目
npm run build

# 将dist目录部署到Web服务器
cp -r dist/* /var/www/html/
```

## 📄 许可证

本项目采用 [MIT License](LICENSE) 许可证。

## 🙏 致谢

感谢以下开源项目和服务：

-   [Vue.js](https://vuejs.org/) - 渐进式 JavaScript 框架
-   [Vite](https://vitejs.dev/) - 下一代前端构建工具
-   [TypeScript](https://www.typescriptlang.org/) - JavaScript 的超集
-   [智谱 AI](https://open.bigmodel.cn/) - AI 模型服务提供商
