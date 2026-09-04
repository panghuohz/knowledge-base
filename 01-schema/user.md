# 用户表 user

> 表名建议：t_user ｜ 最后更新：2026-09-04

## 字段（待按实际确认）
| 字段 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| id | bigint | 是 | 主键 |
| phone | varchar | 是 | 手机号（登录账号） |
| nickname | varchar | 否 | 昵称 |
| avatar | varchar | 否 | 头像 URL |
| status | tinyint | 是 | 状态：0 禁用 1 正常 |
| created_at | datetime | 是 | 创建时间 |
| updated_at | datetime | 是 | 更新时间 |

## 索引 / 唯一键
- [ ] phone 唯一索引

## 关联
- [ ] 与 agent 是否一对一；与 house / follow 一对多
