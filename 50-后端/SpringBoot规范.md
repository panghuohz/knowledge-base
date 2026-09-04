# Spring Boot 规范（建议初稿，待确认）

> 适用范围：通用 ｜ 维护人：待定 ｜ 最后更新：2026-09-04

- 分层：controller / service / mapper(dao) / entity / dto / vo
- 接口入参出参用 DTO/VO，不直接暴露 entity
- 统一异常处理 + 统一响应（见 30-接口API）
- 敏感配置走环境变量 / 配置中心
