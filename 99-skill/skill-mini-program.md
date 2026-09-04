# Skill：小程序开发

依赖顺序：页面 → 接口 → Model → Store → Component → Page

目录规范见 03-frontend/mini-program-standard.md

原则：
- 页面不直接请求接口，统一走 api/ 层
- 数据先过 models 再进页面
- 公共逻辑下沉 hooks / components
