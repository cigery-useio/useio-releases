<div align="center">

   <img src="https://raw.githubusercontent.com/cigery-useio/assets/main/logo-200.png" width="130" height="130" alt="UseIO Logo">

# UseIO

### 住在你电脑里的 AI 搭档

一款 100% 本地运行的桌面 AI 智能体。不是 IDE 插件，不是终端工具，而是一个独立应用 —
自研 Agent Loop 引擎驱动 18 项原子能力、30 余种内置工具，直接接管你的文件、代码、终端、浏览器和屏幕。
数据零上传，模型自由配置，记忆持久沉淀，越用越懂你。

![Latest Release](https://img.shields.io/github/v/release/cigery-useio/useio-releases?style=flat-square&color=6c5ce7)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-00cec9?style=flat-square)
![License](https://img.shields.io/badge/license-EULA-00b894?style=flat-square)
![Local First](https://img.shields.io/badge/100%25-Local--First-6c5ce7?style=flat-square)

[官网](https://www.useio.com) · [文档](https://www.useio.com/docs.html) · [下载](#-下载安装) · [更新日志](https://github.com/cigery-useio/useio-releases/releases) · [FAQ](#-常见问题)

</div>

---

## 📸 产品预览

<table>
  <tr>
    <td width="50%" align="center">
      <img src="https://raw.githubusercontent.com/cigery-useio/assets/main/screenshots/chat.png" alt="Agent 执行任务">
      <br><sub>对它说一句话，Agent 自动拆解任务、调用工具、逐步执行</sub>
    </td>
    <td width="50%" align="center">
      <img src="https://raw.githubusercontent.com/cigery-useio/assets/main/screenshots/memories.png" alt="记忆图谱">
      <br><sub>可视化记忆图谱，多层记忆分层协作，越用越懂你</sub>
    </td>
  </tr>
  <tr>
    <td width="50%" align="center">
      <img src="https://raw.githubusercontent.com/cigery-useio/assets/main/screenshots/image.png" alt="屏幕读取与视觉分析">
      <br><sub>查看电脑屏幕，视觉模型识别 UI、错误信息、图表数据</sub>
    </td>
    <td width="50%" align="center">
      <img src="https://raw.githubusercontent.com/cigery-useio/assets/main/screenshots/skills.png" alt="技能系统与 MCP">
      <br><sub>SKILL.md 自定义技能 + MCP 工具集成，无限扩展能力边界</sub>
    </td>
  </tr>
</table>

> 📌 截图即将上线。将截图文件上传至 `cigery-useio/assets` 仓库的 `screenshots/` 目录即可自动展示。

---

## 🎯 UseIO 的定位

UseIO 住在你电脑里，接管的是你整台电脑的工作流。编程只是它能力的一部分 — 它还能解析你的 Office 文档和 PDF、读取你的屏幕帮你排查问题、管理你的文件和资料、操作浏览器采集数据。所有数据 100% 本地处理，零上传；不绑定任何模型，自由配置；记忆持久沉淀，越用越懂你。

---

## ✨ 核心特点

### 🤖 Agent Loop 引擎 — 精准调用工具，一次做对

自研 Agent Loop 引擎采用「感知 → 决策 → 执行 → 反馈」循环架构。你提出需求，引擎自动拆解为多个步骤，每步选择合适的工具执行，根据结果决定下一步，直到任务完成。内置自纠错机制和三级递进死循环检测，确保任务始终向前推进。

**18 项原子能力 + 30 余种内置工具**，覆盖文件操作、代码执行、命令行、进程管理、浏览器自动化、屏幕读取、文档解析等全方位场景。原子能力可自由组合，灵活应对从简单问答到复杂多步任务的任意场景。工具按安全级别三级管理：低风险静默执行，中风险需确认，高风险始终需确认。

更重要的是，原子能力是模型无关的 — 当你切换到更强的模型时，同样的工具集会随模型能力提升而表现更好。**模型越强，能力越强，无需重新适应。**

**精准的工具调用机制**是任务质量的关键保障：

- **上下文感知** — 每次调用前，引擎将当前任务状态、文件内容、历史执行结果注入上下文，让 LLM 在充分信息下做决策
- **工具语义匹配** — 根据任务意图自动筛选最相关的工具子集，避免 LLM 在 30+ 工具中迷失方向
- **参数校验与消歧** — 工具调用前自动校验参数完整性，多匹配时主动消歧，匹配失败时返回最相似片段供参考
- **执行结果反馈** — 每次工具执行的结果都回传给 LLM，形成闭环验证，做错了能自己发现并纠正

这套机制让 LLM 每次都能选对工具、传对参数、拿到正确结果 — 最大程度减少反复修改和调试，**节约你的 API 调用次数和 Token 消耗**。

> **场景举例**：输入「分析 src/components 目录，找出未使用的组件并清理」
>
> UseIO 自动 → 扫描目录 → 交叉引用分析 → 生成清理方案 → 你确认后执行删除 → 验证结果

### 🧠 记忆图谱 — 个人 AI 资产飞轮

可视化的多层记忆系统，不是每次对话从零开始：

- **核心信息** — 常驻对话上下文，始终可用（你的偏好、习惯、项目背景）
- **相关历史** — 按需语义召回，对话中自动匹配相关记忆
- **本地知识库** — 需要时自动注入，无需手动翻找

记忆不会随会话结束而消散。你在使用过程中创建的 Skill、积累的记忆与知识，在本地持续沉淀 — 这不是临时上下文，而是**只属于你的、可不断复用的数字能力体系**。

这是一个正向飞轮：用得越久，UseIO 越懂你的习惯与偏好，记忆越丰富，知识库越充实，技能越完善 — 每一次使用都在为下一次积累优势，工作效率获得复利增长。

### 🖥️ 屏幕读取与视觉分析 — 看得见你的屏幕

读取所有显示器的全屏画面（支持多屏），配合视觉模型精准识别 UI 结构、错误信息、图表数据。通过 `instruction` 参数引导视觉模型聚焦特定区域，大幅提升分析精度。

> **场景举例**：编译报错了？对它说「看看屏幕上这个错误」→ 它截屏、识别错误信息、定位问题、给出修复方案。

还能直接读取本地图片文件（png/jpg/jpeg/webp）并分析内容，适用于分析 UI 设计稿、图表数据、截图等场景。

### 🔒 100% 本地运行 — 数据不出设备

- **没有云端服务** — 不依赖任何 UseIO 官方服务器
- **数据不出设备** — 所有对话、记忆、知识库均在本地处理与存储
- **模型自主可控** — 你自行配置 LLM API，UseIO 不内置任何模型
- **安全防护** — 系统目录黑名单、代码执行沙箱、启动密码保护、自动备份与恢复

```
你的输入 ──→ UseIO 本地处理 ──→ 你配置的 LLM API（仅对话内容）
                │
                ├──→ 本地记忆库（本地数据库）
                ├──→ 本地知识库（向量索引）
                └──→ 本地文件系统（工作区）
```

### 🔧 模型自由 + 无限扩展

**不绑定任何模型** — 兼容所有 OpenAI API 格式的服务：

| 类型 | 示例 |
|------|------|
| 国内模型 | DeepSeek、智谱 GLM、Kimi、通义千问、MiniMax |
| 国际模型 | OpenAI GPT 系列、Anthropic Claude（通过兼容接口） |
| 本地模型 | Ollama / LM Studio / vLLM 等本地部署 |
| 第三方服务 | 阿里百炼、火山方舟、腾讯云等 |

> 具体模型名称请查阅各服务商最新文档。支持配置多个模型，对话中随时切换。

**可扩展能力体系**：

- **SKILL.md 技能系统** — 编写 SKILL.md 定义自定义技能，打造专属工作流，支持导入 / 导出和社区分享
- **MCP 工具集成** — 通过 MCP 协议接入外部工具（数据库查询、API 调用、第三方服务），Agent 像调用内置工具一样使用它们

---

## 📥 下载安装

### Windows

| 类型 | 说明 | 适合人群 |
|------|------|---------|
| **NSIS 安装包** (`.exe`) | 标准安装程序，支持自定义安装路径 | 大多数用户 |
| **便携版** (`.exe`) | 免安装，解压即用，不写注册表 | 需要便携使用的用户 |

### macOS

| 格式 | 说明 |
|------|------|
| **DMG** (`.dmg`) | 标准 macOS 安装镜像，支持 Apple Silicon 和 Intel |

### Linux

| 格式 | 说明 |
|------|------|
| **AppImage** (`.AppImage`) | 免安装，下载后赋予执行权限即可运行 |

```bash
chmod +x UseIO-*.AppImage
./UseIO-*.AppImage
```

> 📥 前往 [Releases 页面](https://github.com/cigery-useio/useio-releases/releases) 选择最新版本下载

### 系统要求

| 平台 | 最低系统版本 | 架构 | 磁盘空间 |
|------|------------|------|---------|
| Windows | Windows 10 1809+ | x64 | > 2 GB |
| macOS | macOS 11 Big Sur+ | Apple Silicon / Intel | > 2 GB |
| Linux | Ubuntu 20.04+ | x64 | > 2 GB |

---

## 🚀 快速上手

### Step 1：安装并启动

下载对应平台的安装包，按提示完成安装后启动 UseIO。

### Step 2：配置大语言模型

UseIO 不内置任何模型，你需要配置一个 LLM API：

1. 进入 **设置 → 模型管理**，点击 **添加模型**
2. 填写 API Base URL、API Key、模型名称
3. 保存后即可在对话中使用

> 💡 以智谱 GLM 为例：
> - API Base URL: `https://open.bigmodel.cn/api/paas/v4`
> - Model Name: `glm-5.3`
>
> 如需使用屏幕读取 / 图片分析功能，还需额外配置一个支持视觉的模型。

### Step 3：开始第一个任务

在对话框中直接描述你的需求：

```
帮我分析 src/components 目录，找出未使用的组件并清理
```

UseIO 会自动拆解任务、调用工具、逐步执行，你只需确认关键决策点。

> 💡 在对话框中输入 `@` 可以触发提及菜单，快速引用工作空间中的文件、目录或技能。

---

## 📋 功能全景

| 功能 | 说明 |
|------|------|
| **Agent 工具调用** | 18 项原子能力 + 30 余种内置工具，自动拆解任务链逐步完成 |
| **屏幕读取与视觉分析** | 截取全屏画面，视觉模型识别 UI 结构、错误信息、图表数据 |
| **记忆图谱** | 多层记忆分层协作，核心信息常驻、历史按需召回、知识库自动注入 |
| **知识库语义检索** | 本地向量嵌入模型驱动，自动注入相关知识，支持 Office / PDF 解析 |
| **技能系统** | 通过 SKILL.md 自定义技能，导入 / 导出 / 社区分享 |
| **MCP 工具集成** | 标准化协议接入外部工具，无限扩展能力边界 |
| **浏览器自动化** | 控制 Chrome 执行多步骤网页操作、数据采集、表单填写 |
| **代码沙箱** | 内置 JavaScript / Python 执行环境，安全隔离 |
| **集成终端** | 执行 shell 命令，支持常驻进程管理和多会话 |
| **文档解析** | Word / Excel / PowerPoint / PDF 结构化提取 + OCR 图片文字识别 |
| **@提及功能** | 快速引用工作空间中的文件、目录或技能 |
| **检查点与撤销** | 敏感操作前自动创建检查点，支持撤销 / 重做 |

> 📖 详细使用指南请参阅 [官方文档](https://www.useio.com/docs.html)

---

## ❓ 常见问题

<details>
<summary><b>UseIO 是开源的吗？</b></summary>

UseIO 目前在持续快速迭代，源码暂未公开。Release 仓库提供免费的二进制安装包下载。
</details>

<details>
<summary><b>UseIO 需要联网吗？</b></summary>

UseIO 本身不需要联网即可运行。但 AI 对话功能需要你配置一个 LLM API，这部分网络请求直接从你的电脑发送至你配置的 API 服务，不经过 UseIO 的任何服务器。
</details>

<details>
<summary><b>支持哪些 LLM 模型？</b></summary>

兼容所有 OpenAI API 格式的模型服务，包括 DeepSeek、智谱 GLM、Kimi、通义千问、MiniMax、OpenAI GPT 系列、Anthropic Claude（通过兼容接口）、Ollama 本地模型等。具体模型名称请查阅各服务商最新文档。支持配置多个模型，在对话中随时切换。
</details>

<details>
<summary><b>Windows 安装时提示"SmartScreen 已阻止启动"？</b></summary>

这是因为 UseIO 的代码签名证书尚未被 Windows 识别。点击 **"更多信息"** → **"仍要运行"** 即可继续安装。
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

## 🤝 社区与支持

| 渠道 | 地址 |
|------|------|
| 🌐 官方网站 | [www.useio.com](https://www.useio.com) |
| 📖 使用文档 | [docs.useio.com](https://www.useio.com/docs.html) |
| 📧 联系邮箱 | cy@useio.com |
| 🐛 问题反馈 | [GitHub Issues](https://github.com/cigery-useio/useio-releases/issues) |

> 在使用中遇到任何问题，欢迎通过 GitHub Issues 或邮箱反馈。

---

## 📄 许可证

UseIO 是一款免费软件，采用自定义的 [最终用户许可协议（EULA）](LICENSE.md)。

**核心要点：**
- ✅ 个人和企业均可免费使用
- ✅ 数据完全本地化，你拥有全部控制权
- ✅ 可自由配置任意模型，不受厂商锁定
- ✅ 支持自定义技能和 MCP 工具扩展能力边界

**AI 功能特别免责条款：**
- AI 输出基于概率算法生成，具有不确定性
- 用户应自行验证 AI 输出的准确性和安全性
- 因使用或依赖 AI 功能造成的任何损失和风险由用户自行承担

完整协议请参见 [LICENSE.md](LICENSE.md) 文件。

---

<div align="center">

© 2026 UseIO.com All rights reserved.

**用输入输出重新定义人机协作**

</div>
