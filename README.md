# 口译练习工具 · Interpretation Practice Tool

> A bilingual PWA for professional interpreter training — TTS playback, pause countdown, audio cues, and per-segment recording. All in the browser. No API keys needed.

一款面向专业口译员的**浏览器端**练习工具。支持原文 TTS 朗读、停顿倒计时、四音提示系统、逐段录音存档。纯前端，无需任何 API Key，无需注册。

---

## ✨ 功能亮点 · Features

- **段落智能识别** — 双换行 / `//` 标记自动分段，支持手动编辑合并
- **双语 TTS 朗读** — 浏览器原生 Web Speech API，自动检测中/英文，可调速可调音调
- **四音提示系统** — 朗读开始、朗读结束、停顿开始、停顿结束，四阶段独立音效
- **停顿倒计时** — 5~120 秒可调，可视化进度条，支持提前跳过
- **逐段录音** — MediaRecorder API，每段独立存档，支持回放 / 单段下载 / 全部 zip 打包
- **离线可用** — PWA 架构，安装到手机主屏幕后即使断网也能使用
- **零隐私风险** — 全部运算在浏览器本地完成，无任何数据上传

## 📲 使用方式 · How to Use

### 在线访问 · Web App
```
https://chrismzhu-del.github.io/interpretation-practice-pwa/
```

### 安装到手机 · Install on Phone
1. 用 **Safari**（iOS）或 **Chrome**（Android）打开上方网址
2. iOS：底部「分享」→「添加到主屏幕」
3. Android：顶部横幅「安装」或菜单「添加到主屏幕」
4. 安装后即可像原生 App 一样使用，支持离线

### 录音须知 · Microphone Note
- 首次点击录音时需**允许麦克风权限**
- iOS Safari 仅支持 HTTPS 下获取麦克风（本工具部署在 GitHub Pages 即 HTTPS，请放心）

## 🛠 技术栈 · Tech Stack

| 能力 | 技术 |
|------|------|
| TTS 朗读 | Web Speech API（SpeechSynthesis） |
| 提示音合成 | Web Audio API（OscillatorNode） |
| 录音 | MediaRecorder API + getUserMedia |
| 打包下载 | JSZip（CDN） |
| PWA 离线 | Service Worker + Cache API |
| 部署 | GitHub Pages（HTTPS） |

## 📁 项目结构 · Project Structure

```
interpretation-pwa/
├── index.html          # 主应用（单文件）
├── manifest.json       # PWA 清单
├── sw.js               # Service Worker（离线缓存）
├── icon-192.png        # 主屏幕图标 192×192
├── icon-512.png        # 主屏幕图标 512×512
└── README.md           # 本文件
```

## 📄 许可 · License

**保留所有权利 — All Rights Reserved**

本软件仅供**个人非商业使用**。未经作者书面许可，禁止：

- 用于商业目的（包括但不限于销售、捆绑推广、付费服务）
- 修改、反编译或创建衍生作品
- 再次分发或公开传播

This software is licensed for **personal, non-commercial use only**. Without explicit written permission from the author, you may not:

- Use it for commercial purposes (including sales, bundling, paid services)
- Modify, decompile, or create derivative works
- Redistribute or publicly distribute it
