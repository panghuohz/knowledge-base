# App 开发规范（建议初稿，待确认）

> 适用范围：移动 App（原生 / React Native / Flutter / uni-app） ｜ 维护人：待定 ｜ 最后更新：2026-09-04

## 技术栈
原生 / RN / Flutter / uni-app——选型确认后，把框架选型与目录写入本文件再开发。

## 与小程序/Web 的主要差异
| 维度 | 差异 |
| --- | --- |
| 页面 | 原生导航栈 / 路由，非 URL 路由（uni-app / Taro 类除外） |
| 尺寸 | dp（RN/原生）、逻辑像素（Flutter），无 rpx |
| 组件 | 各框架自己的组件体系，不直接复用 Web 组件 |
| 状态 | 框架生态：Riverpod / Provider / Redux 等 |
| 能力 | 相机 / 定位 / 推送等原生能力需权限与原生桥接 |
| 发布 | 应用商店审核、签名、版本灰度，非 Web 即时发布 |

## 目录（按框架，示例）
- Flutter：lib/（pages/ widgets/ models/ services/ state/ utils/）。
- RN：src/（风格同 Web：api / components / screens / store / hooks / utils）。
- uni-app：pages/ components/ static/ + pages.json / manifest.json（可复用小程序规范）。

## 规范要点
- 本文件为初稿：真正做 App 项目时，先确定框架并把目录、状态方案、发布流程写进来再开发。
- 原生权限按需申请，遵守隐私合规。
- 版本号与商店上架资料管理记录在项目档案。
