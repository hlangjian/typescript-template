# TypeScript Template

一个现代化的 TypeScript 库模板，使用 ESM 输出格式，集成了完整的开发工具链。

## ✨ 特性

- 🚀 **现代 TypeScript**: 使用最新的 TypeScript 特性和严格模式
- 📦 **ESM 优先**: 仅输出 ES Module 格式，符合现代 JavaScript 生态
- 🔧 **tsup 构建**: 快速、零配置的 TypeScript 打包工具
- 📝 **类型声明**: 自动生成 `.d.ts` 类型声明文件
- 🎯 **ESLint 集成**: 现代化的 ESLint 配置，确保代码质量
- 🛡️ **严格类型检查**: 启用所有严格类型检查选项
- 📁 **清晰的项目结构**: 标准化的目录结构和命名规范

## 📦 安装

```bash
# 克隆模板
git clone <your-repo-url>
cd typescript-template

# 安装依赖
npm install
# 或
yarn install
# 或
pnpm install
```

## 🛠️ 开发

### 可用脚本

```bash
# 开发模式（监听文件变化自动重新构建）
npm run dev

# 构建生产版本
npm run build

# 代码检查
npm run lint

# 自动修复代码问题
npm run lint:fix
```

### 项目结构

```
typescript-template/
├── src/
│   ├── index.ts          # 主入口文件
│   └── utils/
│       └── index.ts      # 工具函数
├── dist/                 # 构建输出目录
├── package.json          # 项目配置
├── tsconfig.json         # TypeScript 配置
├── tsup.config.ts        # 构建工具配置
├── eslint.config.js      # ESLint 配置
├── .gitignore           # Git 忽略文件
└── README.md            # 项目文档
```

## 📚 使用示例

### 基本用法

```typescript
import { greet, delay, User, formatUser } from 'typescript-template'
import { isString, debounce } from 'typescript-template/utils'

// 使用主函数
console.log(greet('World')) // "Hello, World!"

// 使用异步函数
await delay(1000)
console.log('延迟完成！')

// 使用接口和工具函数
const user: User = { id: 1, name: 'Alice', email: 'alice@example.com' }
console.log(formatUser(user)) // "Alice (alice@example.com)"

// 使用工具函数
if (isString(someValue)) {
    console.log(someValue.toUpperCase())
}

// 使用防抖函数
const debouncedFn = debounce(() => {
    console.log('防抖执行')
}, 300)
```

## ⚙️ 配置说明

### TypeScript 配置

- **目标**: ES2022
- **模块**: ESNext
- **模块解析**: bundler
- **严格模式**: 启用所有严格检查
- **输入文件**: `src/**/*`
- **排除文件**: `node_modules`, `dist`, 测试文件

### 构建配置

- **入口**: `src/index.ts`
- **输出格式**: ESM
- **输出目录**: `dist/`
- **类型声明**: 自动生成 `.d.ts` 文件
- **源码映射**: 生成 sourcemap 文件
- **清理构建**: 每次构建前清空输出目录

### ESLint 配置

使用现代化的 ESLint flat config 格式：

- TypeScript 专用规则
- 代码风格统一（单引号、无分号等）
- 导入排序和类型导入优化
- 禁用 `console.log` 和 `debugger`

## 🚀 发布

1. 更新 `package.json` 中的版本号
2. 运行构建命令：
   ```bash
   npm run build
   ```
3. 发布到 npm：
   ```bash
   npm publish
   ```

## 🔧 开发环境要求

- **Node.js**: >= 18.0.0
- **TypeScript**: ^5.0.0
- **包管理器**: npm, yarn, 或 pnpm

## 📄 许可证

MIT License

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开 Pull Request

## 📖 相关文档

- [TypeScript 官方文档](https://www.typescriptlang.org/docs/)
- [tsup 文档](https://tsup.egoist.dev/)
- [ESLint 文档](https://eslint.org/docs/latest/)
