# BLS-KOX Admin

BLS-KOX 多租户 SaaS 平台的后台管理前端项目，基于 **Ant Design Pro + UmiJS Max** 构建。

## 仓库关系

本仓库是从 [BLS-KOX](https://github.com/npcxl/BLS-KOX) 总仓库拆分出的独立前端子项目，对应总仓库中的 `bls-admin` 目录。

| 独立仓库 | 说明 | 总仓库路径 |
|---------|------|-----------|
| **BLS-KOX-Admin** (当前) | React 前端 | `bls-admin/` |
| [BLS-KOX-Koa](https://github.com/npcxl/BLS-KOX-Koa) | Koa 后端 | `bls-server/` |
| [BLS-KOX-Java](https://github.com/npcxl/BLS-KOX-Java) | Java 后端 | `bls-java-server/` |
| [BLS-KOX-Event-Service](https://github.com/npcxl/BLS-KOX-Event-Service) | 事件微服务 | `bls-event-service/` |
| [BLS-KOX-Deploy](https://github.com/npcxl/BLS-KOX-Deploy) | 部署配置 | 根目录部署文件 |

## 快速开始

```bash
# 1. 安装依赖
npm install

# 2. 配置环境变量（复制示例文件后按需修改）
cp .env.example .env

# 3. 启动开发服务器（默认端口 9000）
npm run dev

# 4. 构建生产版本
npm run build
```

默认连接后端 API 地址为 `http://localhost:8080`，可在 `.env` 中修改。

## 技术栈

- **React 19** + **TypeScript**
- **Ant Design Pro** (UmiJS Max)
- **Ant Design 6** 组件库
- **@tanstack/react-query** 数据请求
- **Tailwind CSS** 样式
- **Biome** 代码检查与格式化
- **Vitest** 单元测试

## 项目定位

BLS-KOX Admin 面向平台运营、租户管理员和系统维护人员，提供统一的管理控制台，覆盖以下核心业务：

- 租户与租户套餐管理
- 用户与部门管理
- 角色与菜单（RBAC 权限）
- 字典与系统配置
- 登录日志、操作日志、审计日志
- 文件与存储资源管理
- 主题配置

系统核心特点是 **多租户隔离**：同一套前端界面服务于多个租户，不同租户在数据、权限、菜单和资源范围上进行隔离管理。

## 目录结构

```
src/
├── components/       # 通用组件
├── hooks/            # 自定义 Hooks
├── pages/            # 页面
│   └── system/       # 系统管理页面
│       ├── config/       # 系统配置
│       ├── dept/         # 部门管理
│       ├── dict/         # 字典管理
│       ├── file-config/  # 文件与存储配置
│       ├── log/          # 日志中心
│       ├── menu/         # 菜单管理
│       ├── role/         # 角色管理
│       ├── tenant-package/ # 租户与套餐
│       ├── theme/        # 主题配置
│       └── user/         # 用户管理
├── services/         # API 接口
├── types/            # TypeScript 类型
└── utils/            # 工具函数
```
