# Knowledge Base · 本地知识库

把项目从需求到上线的规范、Schema、API、工程标准、可复用 Skill 统一沉淀到本地文件，
供开发时人 / AI 共同查阅和维护，而不是散落在聊天记录里。

## 目录结构
- 00-product/ 产品层：业务流程、角色权限、术语表
- 01-schema/ 数据模型：核心实体字段与关系
- 02-api/ API 规范：接口 / 响应 / 分页 / 错误码
- 03-frontend/ 前端工程规范（含小程序）
- 04-backend/ 后端技术规范（Spring Boot / MySQL / Redis / 部署）
- 05-ui/ 设计系统
- 06-project/ 项目档案：小蜗找房 / 黑石经纪人 / Admin 后台
- 99-skill/ 可复用开发流程（Skill）

## 建议配合 AI 的开发顺序
1. 读 00-product 对应业务流程与术语
2. 设计 Schema：参考 01-schema 既有实体，避免重复造表
3. 设计 API：遵守 02-api 规范，同步到 Apifox 并出 Mock
4. 开发：前端按 03-frontend，后端按 04-backend
5. 界面：按 05-ui 设计系统
6. 收尾：更新 06-project 档案，把新经验写回 99-skill

## 维护约定
- 每个文件顶部标注「适用范围 / 维护人 / 最后更新」。
- 公共规范影响所有项目，改动需写明理由。
- 客户资料、密钥等敏感信息禁止入库。
