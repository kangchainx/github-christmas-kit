# GitHub Profile Christmas Kit

中文 | [English](README.md)

仅提供圣诞节主题 SVG 图标，用于装点 GitHub Profile README。  
本项目不提供个人主页/README 的整体设计或生成。

在线演示：https://kangchainx.github.io/github-christmas-kit/

## 项目内容

- `index.html`：单文件 SPA（React 18 + Tailwind CDN）
- `assets/svg/`：带循环动画的 SVG 图标（`viewBox="0 0 64 64"`）

## 如何使用

1. 打开在线演示，挑选你喜欢的图标。
2. 在图标卡片上点击 `Markdown` / `URL` / `HTML` 完成复制。
3. 打开你的 GitHub Profile README（与用户名同名仓库：`<username>/<username>`），粘贴后提交保存，刷新个人主页查看效果。

### Base URL（图标地址前缀）

- GitHub Pages 图标 Base URL： https://kangchainx.github.io/github-christmas-kit/assets/svg/
- 示例（Markdown）：

```md
[![Santa Hat](https://kangchainx.github.io/github-christmas-kit/assets/svg/santa-hat.svg)](https://kangchainx.github.io/github-christmas-kit/)
```

## 本地运行

### 方式 A：直接打开单文件

直接用浏览器打开 `index.html`（需要联网加载 CDN 资源）。

注意：用 `file://` 打开可能会导致剪贴板不可用。建议用本地静态服务：

```bash
python3 -m http.server 5173
# 打开 http://localhost:5173/
```

### 方式 B：使用 Vite（可选）

```bash
npm install
npm run dev
```

## 贡献指南

### 快速开始

1. 设计一个 SVG 图标（小尺寸也要清晰），并包含循环动画（`repeatCount="indefinite"`）。
2. 将文件放入 `assets/svg/`（文件名使用 kebab-case，例如 `santa-hat.svg`）。
3. 提交 Pull Request。
   - 可选：在 `index.html` 的 `assets/icons.json`（图标清单）中补充你的图标信息。

小提示：你可以先在网站底部的「Contributor Lab / 贡献者实验室」里粘贴 SVG 代码实时预览，再提交 PR。

### AI 提示词模板

```text
请生成一个“圣诞帽（Santa Hat）”的 SVG 小图标，viewBox="0 0 64 64"，透明背景，适合暗色背景展示。风格要简洁可爱、线条清晰、形状大胆。

配色与结构：
- 帽身为红色，并带轻微的竖向渐变：顶部 #fb7185 → 底部 #ef4444（linearGradient id="hatRed"）
- 帽檐为柔和的白色（圆角矩形/路径），可加一条浅灰高光线
- 帽尖有一个白色绒球（circle）

动画（循环播放 repeatCount="indefinite"）：
- 整体上下漂浮：animateTransform translate 值 "0 0; 0 -2; 0 0"，dur="1.6s"
- 轻微左右摇摆：animateTransform rotate 围绕 (32,44) 值 "-3 32 44; 3 32 44; -3 32 44"，dur="1.6s"
- 绒球轻微弹跳：circle 的 r 值 "6; 6.6; 6"，dur="1.6s"

请只返回 SVG 代码（不要 markdown 包裹），不要引用外部资源，保持代码简洁。想生成其他同风格图标，把“圣诞帽”替换为其他圣诞元素即可。
```

### 图标规范

- 格式：SVG
- 尺寸：`viewBox="0 0 64 64"`
- 背景：必须透明
- 颜色：推荐红色（`#ef4444`、`#dc2626`）、绿色（`#22c55e`、`#15803d`）、白色

## License

MIT — 详见 `LICENSE`。
