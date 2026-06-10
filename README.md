# 🎬 Viral Video Studio Skill

**AI 驱动的自媒体爆款拆解与脚本工坊**

> 输入一个视频链接 → 逐帧分析画面 → 12 维标签拆解 → 飞书资产库自动沉淀 → 基于积累案例生成脚本

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/platform-Douyin%20%7C%20Bilibili%20%7C%20Xiaohongshu-brightgreen)](#)
[![Hermes Agent Skill](https://img.shields.io/badge/Hermes%20Agent-Skill-blue)](#installation)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Supported-purple)](#installation)
[![OpenClaw](https://img.shields.io/badge/OpenClaw-Supported-orange)](#installation)
[![Codex](https://img.shields.io/badge/Codex-Supported-green)](#installation)

---

## ✨ 这是什么？

一个给 AI Agent 使用的 Skill，让你的 AI 助手变成**千万粉自媒体博主**：

1. **🔍 视频拆解** — 输入任意视频链接（抖音/B站/小红书等），AI 自动下载视频、逐帧提取画面、识别字幕，然后从 6 大维度深度拆解
2. **📊 资产库** — 拆解结果自动写入飞书多维表格，12 个爆款基因标签，形成长期积累的优质案例库
3. **📝 脚本工坊** — 基于积累的案例库 + 千万粉博主视角，为用户优化或生成完整视频脚本（含口播文案 + 画面建议）

---

## 🚀 Installation

### Hermes Agent

```bash
# 方式一：使用 Hermes CLI
hermes skill add viral-video-studio

# 方式二：手动复制
cp -r viral-video-studio ~/.hermes/skills/social-media/viral-video-studio/
```

安装后重启 Hermes Agent 即可使用。

### Claude Code

```bash
# 方式一：个人级别安装（推荐）
cp -r viral-video-studio ~/.claude/skills/viral-video-studio/

# 方式二：项目级别安装
cp -r viral-video-studio /your/project/.claude/skills/viral-video-studio/
```

Claude Code 会自动读取 `CLAUDE.md` 作为入口，完整指令在 `SKILL.md` 中。

### OpenClaw

```bash
# 方式一：使用 OpenClaw CLI（推荐）
openclaw skills install git:SinKry/viral-video-studio

# 方式二：手动复制
cp -r viral-video-studio ~/.openclaw/skills/viral-video-studio/
```

OpenClaw 会自动识别 `SKILL.md` 格式的 Skill 定义。

### Codex (OpenAI)

```bash
# 克隆仓库到本地
git clone https://github.com/SinKry/viral-video-studio.git

# AGENTS.md 会被 Codex 自动加载
```

Codex 会自动读取仓库根目录的 `AGENTS.md` 作为指令入口，`SKILL.md` 提供完整的拆解框架定义。

---

## 📋 使用方式

**拆解视频：**
```
帮我拆解视频：https://v.douyin.com/xxxxx
```

**生成脚本：**
```
帮我写一个关于 AI 工具推荐的短视频脚本，60秒，口播类
```

**优化脚本：**
```
帮我优化这个脚本：[粘贴你的脚本]
```

---

## 📐 拆解框架（6 维度 × 12 标签）

### 6 大分析维度

| 维度 | 分析什么 |
|------|---------|
| 🎯 爆款基因 | 情绪触发点、受众定位、信息差、时效性 |
| ✍️ 文案架构 | Hook、冲突构建、信息密度、金句、CTA |
| 🎬 画面呈现 | 封面、镜头语言、字幕花字、BGM、人设 |
| ⏱️ 视频节奏 | 时长、信息节奏、转折点、留白、循环设计 |
| 📱 平台适配 | 算法优化、标签策略、发布时间、互动引导 |
| 🔄 可复用模型 | 核心公式、可复制元素、改良空间 |

### 12 个爆款基因标签（多选）

| 标签 | 含义 |
|------|------|
| 情绪共鸣 | 击中共情/感动/愤怒等情绪 |
| 信息差 | 提供别人不知道的信息 |
| 视觉冲击 | 画面震撼/记忆点强 |
| 实用干货 | 可直接操作的方法论 |
| 反转悬念 | 剧情反转/制造好奇心 |
| 社会证明 | 数据背书/大V推荐/权威感 |
| 焦虑缓解 | 解决受众焦虑/提供安全感 |
| 猎奇新奇 | 新事物/冷知识/反常识 |
| 身份认同 | 让受众觉得"说的就是我" |
| 争议冲突 | 引发讨论/对立观点 |
| 系列追更 | 续集效应/系列感驱动 |
| 热点借势 | 蹭热点/时效性内容 |

---

## 📦 资产库（Feishu Bitable）

自动创建飞书多维表格，字段结构：

| 字段 | 类型 | 说明 |
|------|------|------|
| 标题 | 文本 | 视频标题 |
| 视频链接 | 超链接 | 原始视频 URL |
| 平台 | 单选 | 抖音/B站/小红书/快手/视频号 |
| 博主 | 文本 | 博主昵称 |
| 视频类别 | 单选 | 知识科普/教程/娱乐/... |
| 爆款基因 | **多选** | 12 个预设标签 |
| 核心受众 | 文本 | 目标人群 + 痛点 |
| 解决痛点 | 文本 | 解决了什么问题 |
| 文案结构全文 | 文本 | 分模块完整拆解 |
| 逐字稿 | 文本 | 按时间戳的完整字幕 |
| ... | ... | 更多字段见 SKILL.md |

---

## 🛠 技术栈

- **视频提取**: yt-dlp（抖音/B站/快手） + 浏览器 fallback（小红书/视频号）
- **关键帧分析**: ffmpeg 抽帧 + Vision AI 模型
- **字幕提取**: yt-dlp 字幕 → 无字幕时 vision 逐帧 OCR
- **资产库**: 飞书 Bitable API（lark-cli）

### 平台兼容性

| 文件 | Hermes Agent | Claude Code | OpenClaw | Codex |
|------|:---:|:---:|:---:|:---:|
| `SKILL.md` | ✅ 主入口 | ✅ 参考 | ✅ 主入口 | ✅ 参考 |
| `CLAUDE.md` | — | ✅ 主入口 | — | — |
| `AGENTS.md` | — | — | — | ✅ 主入口 |

---

## 📁 项目结构

```
viral-video-studio/
├── README.md          # 项目说明 & 安装指南
├── LICENSE            # MIT License
├── SKILL.md           # 核心 Skill 定义（Hermes/OpenClaw 主入口）
├── CLAUDE.md          # Claude Code 入口
├── AGENTS.md          # Codex 入口
└── .gitignore
```

---

## 🤝 Contributing

欢迎 PR！如果你发现了新的爆款基因标签、优化了拆解框架、或者适配了新平台，随时提 PR。

## 📄 License

[MIT](LICENSE)

---

> *"其他工具帮你做更多内容，这个工具帮你判断得更准。"*
