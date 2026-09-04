# 小程序开发规范

> 最后更新：2026-09-04

依赖顺序：页面 → 接口 → Model → Store → Component → Page

目录：
src/
  api/        接口封装
  models/     数据模型
  pages/      页面
  components/ 组件
  store/      状态
  hooks/      逻辑复用
  utils/      工具
  constants/  常量

原则：
- 页面内不直接发请求，统一走 api/ 层
- 数据先过 models 再进页面，避免散落 any
- 公共逻辑下沉 hooks / components
