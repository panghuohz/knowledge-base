# 响应规范（建议初稿，待确认）

> 适用范围：全平台 ｜ 最后更新：2026-09-04

统一包装：
{
  code: 0,
  message: ok,
  data: { }
}

- 成功 code = 0（或 200，全端统一二选一）
- 列表类 data 结构见 pagination-standard
- 禁止把业务错误当作 HTTP 500 返回
