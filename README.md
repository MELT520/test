# PakePlus Cloud Builds

极简云端打包仓库 — 不需要 Fork 任何原仓库，把网页打包成 Android/iOS/桌面应用。

## 使用步骤

### 1. 创建你的仓库

在 GitHub 上新建一个仓库（名称随意，如 `pakeplus-builds`），把本目录所有文件上传。

### 2. 创建 GitHub Token

[点此创建](https://github.com/settings/tokens/new?scopes=repo,workflow)，勾选 `repo` 和 `workflow` 权限。

### 3. 在 PakePlus 中配置

- 仓库名填 `你的用户名/pakeplus-builds`
- Token 填上一步创建的

### 4. 触发构建

选择平台 → 填写参数 → 点击「云端构建」。

构建结果会自动上传到你的仓库 Releases 页面。

## 支持平台

| 平台 | Workflow 文件 | 说明 |
|------|-------------|------|
| Android | `android.yml` | 自动拉取 PakePlus-Android 模板 |
| iOS | `ios.yml` | 自动拉取 PakePlus-iOS 模板 |
| Windows/macOS/Linux | `desktop.yml` | 自动拉取 PakePlus 桌面模板 |

## 工作原理

Workflow 运行时会自动 `git clone` 原作者的平台模板仓库，然后注入你的配置（应用名、URL 等），无需 Fork 任何仓库。
