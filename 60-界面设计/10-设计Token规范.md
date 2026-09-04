# 设计 Token 规范（配置文件约定）

> 适用范围：全端 UI ｜ 维护人：待定 ｜ 最后更新：2026-09-04

## 目标
用一份机器可读的 token 配置文件（类似 Figma Tokens Studio / W3C Design Tokens）作为样式唯一事实源，避免“规范文档漂移”与硬编码。改样式 = 改 token 文件，不逐页改。

## 文件位置（项目级）
- 推荐：<项目仓库>/design-tokens/tokens.json（或 src/styles/tokens.json）
- 若存在 Figma 设计稿：用 Tokens Studio 插件读写同一份文件，设计稿与代码同源。

## 结构（三层）
1. global：原始值（颜色、字号、间距、圆角、阴影的具体数值）
2. semantic：语义/品牌（color-primary、text-1、bg、border、radius-md）
3. component：组件级（按钮高度、输入框高度、卡片圆角），可选

## 命名规则（为 AI 与跨端优化）
- 全部小写，用 . 或 - 分层语义：color.primary.500 / color-primary-500
- 名称描述用途而非外观：text-1（主文字），而不是 gray-900
- 代码禁止魔法值：所有颜色/间距/字号/圆角/阴影引用 token

## 默认 token（模板默认，可按品牌覆盖）
- 间距（4 基准）：4 / 8 / 12 / 16 / 24 / 32 → space-1..space-6
- 字号：12 / 14 / 16 / 20 / 24 / 32 → font-12..font-32
- 圆角：4 / 8 / 12 / 50% → radius-sm / md / lg / full
- 阴影与层级：0~3（平级 / 卡片 / 弹层 / 全屏浮层）
- 颜色语义名见 20-色彩系统.md；示例值见 tokens/tokens.json

## 生成（端差异在生成层解决）
| 端 | 生成物 | 说明 |
| --- | --- | --- |
| Web | :root CSS 变量 / tailwind theme | 直接引用 token |
| 小程序 | app.wxss 变量 | rpx 换算在生成层做（1px≈2rpx） |
| App | Flutter ThemeData / RN theme | 框架主题 |

工具参考：Style Dictionary、token-transformer、Tokens Studio 导出；小项目也可用最小脚本生成 CSS 变量。

## 修改流程
1. 改 tokens.json（唯一入口）
2. 重新生成各端变量文件
3. 提交 tokens.json + 生成物
4. 语义名增删时同步 20-色彩系统.md（只改名/用途，不改值）

## 反例
- ❌ 页面里直接写 #1677ff / 16px / 8px
- ❌ 在 Markdown 维护一份与 tokens.json 不一致的色板
- ✅ 只写 token 名：color-primary、space-4、font-16、radius-md
