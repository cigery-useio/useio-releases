<div align="center">

   <img src="https://github.com/cigery-useio/useio-releases/blob/main/logo_200.png" width="130" height="130" alt="UseIO Logo">

# UseIO

### 用输入输出重新定义人机协作

一款运行在你电脑上的本地桌面 AI 助手，专为编程开发和复杂任务而生。

![Version](https://img.shields.io/badge/version-1.0.0--beta.5-6c5ce7?style=flat-square)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-00cec9?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-00b894?style=flat-square)
![Local First](https://img.shields.io/badge/100%25-Local--First-6c5ce7?style=flat-square)

[官网](https://www.useio.com) · [下载](#-下载安装) · [功能](#-核心功能) · [更新日志](#-更新日志) · [FAQ](#-常见问题)

</div>

---

## 📖 简介

**UseIO** 是一款 100% 本地运行的桌面端 AI 助手。它能读懂你的意图，解析 Office 文档、精准识别图片内容，更能接管你的工作流——直接在你的电脑上写代码、改文档、整理资料、执行命令、查看电脑屏幕并分析屏幕内容来帮助你完成复杂任务。

具备可视化的记忆图谱管理，多层记忆分层协作：核心信息常驻对话上下文，相关历史按需语义召回，本地知识库也会在需要时自动注入。**所有数据都只在你的设备上处理与存储，隐私零上传。** 用得越久，就越懂你的习惯与偏好。

### 为什么选择 UseIO？

| | 传统云端 AI 工具 | UseIO |
|---|---|---|
| **数据隐私** | 对话上传至云端服务器 | 100% 本地处理，零上传 |
| **文件操作** | 只能对话，无法直接操作你的文件 | 13 种原子能力，直接读写编辑你的项目 |
| **代码执行** | 无法在你的环境中运行代码 | 内置 JS/Python 沙箱 + 集成终端 |
| **记忆能力** | 每次对话从零开始 | 可视化记忆图谱，越用越懂你 |
| **模型自由度** | 绑定单一模型 | 自由配置任意 OpenAI 兼容模型 |

---

## ✨ 核心功能

### 🧠 Agent 工具调用

内置 **13 种原子能力**，自动拆解复杂任务链逐步完成：

| 能力 | 说明 |
|------|------|
| 文件读取 | 完整读取 / 范围读取 / 尾部读取 |
| 文件写入 | 创建或覆盖文件 |
| 文件编辑 | 增量编辑 + diff 补丁模式 |
| 目录列表 | 浏览目录结构，树形展示 |
| 文件操作 | 创建 / 删除 / 复制 / 移动 |
| 文件信息 | 存在检查 + 详细元信息 |
| 文件搜索 | 文件名匹配 + 内容全文检索 |
| 命令执行 | Shell 命令，支持后台常驻进程 |
| 进程管理 | 终止后台进程 |
| JavaScript 执行 | 子进程沙箱，安全隔离 |
| Python 执行 | 增强安全检查，模块黑名单 |
| 打开目标 | 用系统默认程序打开文件/URL |
| 路径解析 | 相对路径 → 绝对路径 |

### 🖥️ 屏幕读取与视觉分析

查看电脑屏幕、捕获全屏画面，配合视觉模型精准识别 UI 结构、错误信息、图表数据，辅助开发调试。支持多显示器，可通过 `instruction` 参数引导视觉模型聚焦特定区域。

### 💬 记忆图谱管理

可视化多层记忆分层协作：

- **核心信息** — 常驻对话上下文，始终可用
- **相关历史** — 按需语义召回，智能匹配
- **本地知识库** — 需要时自动注入，无需手动检索

所有记忆数据均在本地处理，基于 HNSW 向量索引实现毫秒级语义检索。

### 📚 知识库语义检索

本地向量嵌入模型（all-MiniLM-L6-v2 + ONNX Runtime）驱动的语义检索引擎：

- 自动将文档/笔记向量化并入库
- 对话中自动检索相关知识并注入上下文
- 支持 Office 文档（Word / Excel / PowerPoint）与 PDF 解析
- 全程本地运行，文档内容不上传任何服务器

### 🔧 技能系统扩展

通过 `SKILL.md` 自定义技能，打造专属工作流：

- 编写 SKILL.md 定义技能触发条件与执行逻辑
- 导入 / 导出 / 管理技能库
- 社区化扩展能力边界

### 🔒 隐私优先 · 零云端

- **没有云端服务** — 不依赖任何 UseIO 官方服务器
- **数据不出设备** — 所有对话、记忆、知识库均在本地处理与存储
- **模型自主可控** — 你自行配置 LLM API，UseIO 不内置任何模型
- **安全防护** — 系统目录黑名单、代码执行限制、启动密码验证、自动备份

---

## 📥 下载安装

### Windows

| 类型 | 说明 | 适合人群 |
|------|------|---------|
| **NSIS 安装包** (`.exe`) | 标准安装程序，支持自定义安装路径、创建快捷方式 | 大多数用户 |
| **便携版** (`.exe`) | 免安装，解压即用，不写注册表 | 需要便携使用的用户 |

> 下载地址：前往 [Releases 页面](https://github.com/cigery-useio/useio-releases/releases) 选择最新版本

### macOS

| 格式 | 说明 |
|------|------|
| **DMG** (`.dmg`) | 标准 macOS 安装镜像，支持 Apple Silicon 和 Intel |

> 下载地址：前往 [Releases 页面](https://github.com/cigery-useio/useio-releases/releases) 选择最新版本

### Linux

| 格式 | 说明 |
|------|------|
| **AppImage** (`.AppImage`) | 免安装，下载后赋予执行权限即可运行 |

```bash
chmod +x UseIO-*.AppImage
./UseIO-*.AppImage
```

> 下载地址：前往 [Releases 页面](https://github.com/cigery-useio/useio-releases/releases) 选择最新版本

---

## 🚀 快速上手

### Step 1：安装并启动

下载对应平台的安装包，按提示完成安装后启动 UseIO。

### Step 2：配置大语言模型

UseIO 不内置任何模型，你需要自行配置一个 LLM API：

1. 进入 **设置 → 模型管理**
2. 点击 **添加模型**，填写以下信息：
   - **模型名称** — 如 `glm-5.2`、`kimi-k2.7-code`、`deepseek-v4-pro`、`claude-4-5-sonnet`、`mimo-v2.5-pro`、`minimax-m3` 等
   - **API Base URL** — 你的 API 服务地址（如 `https://api.openai.com/v1`）
   - **API Key** — 你的密钥
3. 保存后即可在对话中使用

> 💡 UseIO 兼容所有 OpenAI API 格式的模型服务，包括但不限于 OpenAI、DeepSeek、Moonshot、智谱、Ollama 等。

### Step 3：开始第一个任务

在对话框中直接描述你的需求，例如：

```
帮我分析 src/components 目录，找出未使用的组件并清理
```

UseIO 会自动：
1. 调用 `plan` 工具拆解任务
2. 扫描目录、交叉引用分析
3. 生成清理方案
4. 经你确认后执行删除

---

## ⚙️ 配置指南

### 模型配置

UseIO 支持配置多个模型，可在对话中随时切换：

- **对话模型** — 主力模型，负责理解意图和生成回复
- **视觉模型** — 用于屏幕截图分析（需支持 vision 能力）
- **嵌入模型** — 本地向量嵌入，用于知识库和记忆检索（已内置，无需配置）

### 工作区设置

- **用户工作空间** — 设置项目根目录，UseIO 将以此为基础执行文件操作和命令
- **内置工作区** — UseIO 内部数据目录（Plan 文件、草稿等），无需手动管理

### 安全设置

- **启动密码** — 设置应用启动密码，防止未授权访问
- **自动审批** — 可配置特定工具自动执行，无需每次确认
- **数据备份** — 支持手动 / 自动备份，可导出为压缩包

---

## 🔒 隐私与安全

### 数据流向说明

```
你的输入 ──→ UseIO 本地处理 ──→ 你配置的 LLM API（仅对话内容）
                │
                ├──→ 本地记忆库（IndexedDB）
                ├──→ 本地知识库（向量索引）
                └──→ 本地文件系统（工作区）
```

- **对话内容**：仅发送至你配置的 LLM API 服务，UseIO 不经手任何中间数据
- **记忆与知识库**：100% 存储在本地 IndexedDB 中
- **文件操作**：所有文件读写均在本地完成
- **屏幕截图**：截图仅在本地处理，发送至你配置的视觉模型 API

### 安全防护机制

| 层级 | 机制 |
|------|------|
| 系统目录保护 | 黑名单机制，禁止访问 Windows / Linux / macOS 系统敏感目录 |
| 代码执行限制 | JS 代码 ≤ 50KB / 5s 超时；Python 代码 ≤ 100KB / 10s 超时 |
| Python 模块黑名单 | 禁止 `os`、`sys`、`subprocess`、`socket` 等危险模块 |
| JS 沙箱隔离 | 在子进程中执行，与主进程隔离 |
| 启动验证 | 可选密码保护，防止未授权启动 |
| 操作确认 | 文件写入 / 删除 / 命令执行等操作需用户确认（可配置自动审批） |

---

## ❓ 常见问题

<details>
<summary><b>UseIO 是开源的吗？</b></summary>

UseIO 目前处于 Beta 阶段，源码暂未公开。Release 仓库提供免费的二进制安装包下载。
</details>

<details>
<summary><b>UseIO 需要联网吗？</b></summary>

UseIO 本身不需要联网即可运行。但 AI 对话功能需要你配置一个 LLM API（如 OpenAI、DeepSeek 等），这部分网络请求直接从你的电脑发送至你配置的 API 服务，不经过 UseIO 的任何服务器。
</details>

<details>
<summary><b>支持哪些 LLM 模型？</b></summary>

UseIO 兼容所有 OpenAI API 格式的模型服务，包括但不限于：
- OpenAI（GPT-5 / GPT-5.5 等）
- Anthropic Claude（通过兼容接口）
- DeepSeek
- Moonshot（Kimi）
- 智谱 GLM
- Mimo
- MiniMax
- Ollama（本地部署模型）
- 任何 OpenAI 兼容的 API 服务
</details>

<details>
<summary><b>Windows 安装时提示"SmartScreen 已阻止启动"？</b></summary>

这是因为 UseIO 的代码签名证书尚未被 Windows 识别。点击 **"更多信息"** → **"仍要运行"** 即可继续安装。后续版本将申请正式代码签名。
</details>

<details>
<summary><b>macOS 打开时提示"无法验证开发者"？</b></summary>

前往 **系统设置 → 隐私与安全性**，在底部找到提示信息，点击 **"仍要打开"** 即可。或通过终端执行：
```bash
xattr -cr /Applications/UseIO.app
```
</details>

<details>
<summary><b>数据存储在哪里？如何备份？</b></summary>

所有数据存储在本地用户目录下：
- **Windows**: `%APPDATA%/useio/`
- **macOS**: `~/Library/Application Support/useio/`
- **Linux**: `~/.config/useio/`

可在 **设置 → 通用 → 数据备份** 中导出完整数据备份。
</details>

<details>
<summary><b>如何卸载？</b></summary>

- **Windows**: 通过控制面板或设置中的"应用"卸载
- **macOS**: 将应用拖入废纸篓
- **Linux**: 删除 AppImage 文件即可

卸载不会自动删除用户数据，如需彻底清除请手动删除上述数据目录。
</details>

---

## 📋 更新日志

### v1.0.0-beta.5

> Beta 阶段持续迭代中

#### ✨ 核心功能
- Agent 工具调用引擎，13 种原子能力
- 屏幕读取与视觉分析
- 可视化记忆图谱，多层记忆分层协作
- 知识库语义检索，本地嵌入模型驱动
- 技能系统，SKILL.md 自定义技能扩展
- Office / PDF 文档解析与 OCR
- JS / Python 代码沙箱执行
- 集成终端，多会话管理
- 自动备份与恢复
- 启动验证密码保护
- Windows / macOS / Linux 三端支持
- 100% 本地运行，零云端依赖

---

## 🤝 社区与支持

| 渠道 | 地址 |
|------|------|
| 🌐 官方网站 | [www.useio.com](https://www.useio.com) |
| 📧 联系邮箱 | cy@useio.com |
| 🐛 问题反馈 | [GitHub Issues](https://github.com/cigery-useio/useio-releases/issues) |
| 💬 GitHub | [cigery-useio/useio-releases](https://github.com/cigery-useio/useio-releases) |

> 在使用中遇到任何问题，欢迎通过 GitHub Issues 或邮箱反馈。

---

## 📄 许可证

UseIO 是一款免费软件，采用自定义的 [最终用户许可协议（EULA）](LICENSE.md)。

**核心要点：**
- ✅ 个人和企业均可免费使用
- ❌ 禁止逆向工程、反编译、反汇编
- ❌ 禁止转售、再分发、捆绑销售
- ❌ 禁止作为商业产品/服务的一部分进行销售或集成

**AI 功能特别免责条款：**
- AI 输出基于概率算法生成，具有不确定性、不可预测性和随机性
- 用户应自行验证 AI 输出的准确性和安全性
- 因使用或依赖 AI 功能造成的任何损失和风险由用户自行承担
- AI 输出不能替代专业人士的判断、建议或服务

完整协议请参见 [LICENSE.md](LICENSE.md) 文件。

---

<div align="center">

© 2026 UseIO.com All rights reserved.

**用输入输出重新定义人机协作**

</div>
