# 前端目录规范（建议初稿，待确认）

> 最后更新：2026-09-04

通用 Web 建议结构：
src/
  api/ 接口封装
  components/ 公共组件
  pages|views/ 页面（按业务模块分目录）
  store|state/ 状态管理
  hooks/ 逻辑复用
  utils/ 工具
  constants/ 常量
  styles/ 样式
  types/ 类型定义

- 页面按业务模块分文件夹；公共组件放 components，业务组件就近放页面目录。
