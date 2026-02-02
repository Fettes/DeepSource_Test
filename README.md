# DeepSource Test App

这是一个用于测试 DeepSource 代码质量分析的 React + TypeScript 前端项目。

## 项目特点

- **React 18** + **TypeScript** 现代前端技术栈
- **Vite** 快速构建工具
- **ESLint** 代码规范检查
- 包含多种代码质量问题供 DeepSource 检测

## 包含的代码质量问题示例

本项目故意包含以下代码质量问题，用于测试 DeepSource 的检测能力：

### TypeScript 相关
- `any` 类型的使用
- 不安全的类型断言
- 非空断言操作符滥用
- 未使用的变量和函数

### React 相关
- 使用数组 index 作为 key
- 缺少 useMemo/useCallback 优化
- 直接修改状态数组

### 代码风格
- 过高的圈复杂度
- 重复代码
- 魔法数字
- 冗余的条件表达式

### 安全问题
- 硬编码的敏感信息
- eval() 的使用
- 可能的 ReDoS 正则表达式

## 快速开始

### 安装依赖

```bash
npm install
```

### 启动开发服务器

```bash
npm run dev
```

### 构建生产版本

```bash
npm run build
```

### 代码检查

```bash
npm run lint
```

## 项目结构

```
src/
├── components/           # React 组件
│   ├── Counter.tsx      # 计数器组件
│   ├── TodoList.tsx     # 待办事项组件
│   └── UserList.tsx     # 用户列表组件
├── types/               # TypeScript 类型定义
│   └── index.ts
├── utils/               # 工具函数
│   └── helpers.ts
├── App.tsx              # 主应用组件
├── App.css              # 应用样式
├── main.tsx             # 入口文件
└── index.css            # 全局样式
```

## DeepSource 配置

项目根目录包含 `.deepsource.toml` 配置文件，已配置：
- JavaScript/TypeScript 分析器
- React 插件支持
- Prettier 格式化器

## 使用 DeepSource

1. 将项目推送到 GitHub/GitLab/Bitbucket
2. 在 [DeepSource](https://deepsource.io) 上连接仓库
3. DeepSource 将自动分析代码并报告问题

## 许可证

MIT
