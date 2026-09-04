# Web 开发规范（建议初稿，待确认）

> 适用范围：React / Vue 等 Web 应用 ｜ 维护人：待定 ｜ 最后更新：2026-09-04

## 技术栈（按实际项目确认后回写）
- 框架：React / Vue（二选一，避免混用）。
- 构建：Vite（默认）/ Webpack。
- 样式：CSS Modules / Tailwind / Less（统一一种）。
- 状态：Redux / Zustand / Pinia（按框架生态）。

## 目录（示例）
src/
  api/          接口封装
  components/   公共组件
  pages|views/  路由级页面（按业务模块分目录）
  router/       路由集中配置
  store/        状态
  hooks/        逻辑复用
  utils/        工具
  constants/    常量
  styles/       样式
  types/        类型定义

## 规范要点
- 路由集中配置，页面懒加载（React.lazy / 动态 import）。
- 权限：路由守卫 + 按钮级权限码，与后端权限点对应（见 10-产品设计/角色权限规范.md）。
- 请求层统一封装：baseURL、超时、错误码处理（见 30-接口API）。
- 样式变量统一走 60-界面设计/色彩系统.md，禁止硬编码色值。
- 优先复用组件库（Antd / Element 或自建），避免重复造轮子。
- 代码质量：ESLint + Prettier 必须接入，提交前通过。
- 明确目标浏览器与响应式断点；移动端适配与 60-界面设计 一致。

## 测试与构建
- 单测 Vitest / Jest（关键逻辑）；端到端 Playwright（主流程）。
- 构建产物部署：静态托管 / CDN / Nginx（见 50-后端/部署规范.md）。
