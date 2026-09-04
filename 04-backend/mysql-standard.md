# MySQL 规范（建议初稿，待确认）

> 最后更新：2026-09-04

- 表名小写加下划线，建议前缀 t_
- 必备字段：id、created_at、updated_at；软删可选 deleted
- 索引：idx_字段；唯一键：uk_字段
- 金额用 decimal；状态用 tinyint 并登记枚举含义（见 01-schema）
- 表结构变更需同步更新 01-schema 对应文件
