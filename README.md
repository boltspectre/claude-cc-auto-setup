# Claude CC Auto Setup

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js](https://img.shields.io/badge/Node.js-≥18-green)](https://nodejs.org/)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Latest-blue)](https://github.com/anthropics/claude-code)
[![cc-switch](https://img.shields.io/badge/cc--switch-Latest-orange)](https://github.com/farion1231/cc-switch)

> One-click auto-install Claude Code + cc switch | Auto-detects Node.js, Claude Code, cc switch | Zero config AI prompt

[English](#english) | [中文](#中文)

***

## 中文

### 🎯 项目简介

本项目提供**一键自动化环境配置**，帮助用户快速搭建 Claude Code 开发环境，无需手动配置任何参数。

### ✨ 功能特性

| 功能                      | 描述                          |
| ----------------------- | --------------------------- |
| 🔍 **自动检测 Node.js**     | 检测系统是否已安装 Node.js，如未安装则自动下载安装，并配置环境 |
| 📦 **自动安装 Claude Code** | 通过 npm 全局安装最新版 Claude Code  |
| 🔄 **自动下载 cc-switch**   | 从 GitHub Releases 自动获取最新版本  |
| 🚀 **自动启动**             | 解压并启动 cc-switch，无需手动操作      |
| ⚙️ **零配置**              | 所有下载地址自动搜索获取，用户无需配置任何参数     |

### 🚀 快速开始

#### 方式一：使用 AI 智能体执行（推荐）

将 [claude-cc-auto-setup.md](./claude-cc-auto-setup.md) 的内容发送给 AI 智能体，AI 将**全自动完成**所有配置步骤，启动前建议给ai智能体赋予自动执行命令权限。


**例如（包括但不限于）：**

| 类型 | 工具名称 |
|------|----------|
| **IDE 内置 AI** | Cursor、Trae、Windsurf、Qoder、Kiro、CodeBuddy |
| **IDE 插件** | GitHub Copilot、Cline、通义灵码、Kilo Code |

> 💡 **使用方法**：打开任意 AI 智能体，将 `claude-cc-auto-setup.md` 文件内容粘贴到 AI 对话框，AI 会自动执行安装流程。

#### 方式二：手动执行

```bash
# 1. 检测 Node.js
node --version

# 2. 安装 Claude Code
npm install -g @anthropic-ai/claude-code

# 3. 下载 cc-switch（Windows 便携版）
curl -L -o cc-switch.zip https://github.com/farion1231/cc-switch/releases/latest/download/CC-Switch-Windows-Portable.zip

# 4. 解压并运行
Expand-Archive -Path cc-switch.zip -DestinationPath cc-switch
.\cc-switch\cc-switch.exe
```

### 📋 环境要求

| 组件      | 最低版本       | 说明               |
| ------- | ---------- | ---------------- |
| Windows | Windows 10 | x64 架构           |
| Node.js | 18.x LTS   | 用于运行 Claude Code |
| 网络连接    | 科学上网          | 用于下载依赖           |

> 🌐 **国内用户注意**：安装过程需要从 GitHub 和 npm 下载资源，请确保网络环境可以正常访问上述网站。如有必要，请提前配置好科学上网工具。

### 📁 项目结构

```
.
├── claude-cc-auto-setup.md    # AI 提示词文档（自动化配置脚本）
├── cc-switch/               # cc-switch 安装目录（自动生成）
│   ├── cc-switch.exe       # 主程序
│   └── portable.ini        # 便携版配置文件
└── README.md               # 本文件
```

### 🎮 使用说明

#### Claude Code

```bash
# 启动 Claude Code
claude

# 查看版本
claude --version
```

#### cc-switch

1. 查看系统托盘，找到 cc-switch 图标
2. 点击图标打开配置界面
3. 添加 API Key 和配置供应商
4. 一键切换不同 AI 供应商

### 🔧 支持的供应商

cc-switch 支持管理以下 AI 工具的供应商配置：

- **Claude Code** - Anthropic Claude
- **Codex** - OpenAI Codex
- **Gemini CLI** - Google Gemini
- **OpenCode** - 开源 AI 代码助手

### 📊 执行流程

```
┌─────────────────┐
│  检测 Node.js   │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ 安装 Claude Code│
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ 下载 cc-switch  │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ 启动 cc-switch  │
└─────────────────┘
```

### ❓ 常见问题

#### Q: 安装过程中出现权限错误？

A: 请以管理员身份运行 PowerShell 或终端。

#### Q: 如何更新 cc-switch？

A: 删除 `cc-switch` 目录，重新运行配置流程即可自动下载最新版本。

#### Q: 如何配置 API Key？

A: 启动 cc-switch 后，在系统托盘图标右键打开界面，添加供应商配置即可。

### 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！

### 📄 许可证

本项目采用 [MIT License](LICENSE) 开源许可证。

***

## English

### 🎯 Introduction

This project provides **one-click automated environment setup** to help users quickly set up the Claude Code development environment without any manual configuration.

### ✨ Features

| Feature                         | Description                                                       |
| ------------------------------- | ----------------------------------------------------------------- |
| 🔍 **Auto-detect Node.js**      | Detects if Node.js is installed, can auto-download if not         |
| 📦 **Auto-install Claude Code** | Installs latest Claude Code globally via npm                      |
| 🔄 **Auto-download cc-switch**  | Fetches latest version from GitHub Releases automatically         |
| 🚀 **Auto-launch**              | Extracts and launches cc-switch automatically                     |
| ⚙️ **Zero Config**              | All download URLs are auto-searched, no user configuration needed |

### 🚀 Quick Start

#### Option 1: Use AI Agent (Recommended)

Send the content of [claude-cc-auto-setup.md](./claude-cc-auto-setup.md) to your AI agent, and it will **automatically complete** all configuration steps.

**Examples (including but not limited to):**

| Type | Tool Name |
|------|-----------|
| **IDE Built-in AI** | Cursor, Trae, Windsurf, Qoder, Kiro, CodeBuddy |
| **IDE Plugins** | GitHub Copilot, Cline, Tongyi Lingma, Kilo Code |

> 💡 **How to use**: Open any AI agent, paste the content of `claude-cc-auto-setup.md` into the AI chat dialog, and the AI will automatically execute the installation process.

#### Option 2: Manual Execution

```bash
# 1. Check Node.js
node --version

# 2. Install Claude Code
npm install -g @anthropic-ai/claude-code

# 3. Download cc-switch (Windows Portable)
curl -L -o cc-switch.zip https://github.com/farion1231/cc-switch/releases/latest/download/CC-Switch-Windows-Portable.zip

# 4. Extract and run
Expand-Archive -Path cc-switch.zip -DestinationPath cc-switch
.\cc-switch\cc-switch.exe
```

### 📋 Requirements

| Component | Minimum Version | Notes                                 |
| --------- | --------------- | ------------------------------------- |
| Windows   | Windows 10      | x64 architecture                      |
| Node.js   | 18.x LTS        | Required for Claude Code              |
| Internet  | -               | Required for downloading dependencies |

> 🌐 **Note for users in China**: The installation process requires downloading from GitHub and npm. Please ensure your network can access these sites. Configure a VPN/proxy if necessary.

### 📁 Project Structure

```
.
├── claude-cc-auto-setup.md    # AI prompt document (automation script)
├── cc-switch/               # cc-switch installation directory (auto-generated)
│   ├── cc-switch.exe       # Main executable
│   └── portable.ini        # Portable version config
└── README.md               # This file
```

### 🎮 Usage

#### Claude Code

```bash
# Start Claude Code
claude

# Check version
claude --version
```

#### cc-switch

1. Check system tray for cc-switch icon
2. Click icon to open configuration interface
3. Add API Key and configure providers
4. Switch between AI providers with one click

### 🔧 Supported Providers

cc-switch supports managing provider configurations for:

- **Claude Code** - Anthropic Claude
- **Codex** - OpenAI Codex
- **Gemini CLI** - Google Gemini
- **OpenCode** - Open-source AI coding assistant

### 📊 Execution Flow

```
┌─────────────────┐
│ Check Node.js   │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Install Claude  │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Download cc-switch│
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Launch cc-switch│
└─────────────────┘
```

### ❓ FAQ

#### Q: Permission errors during installation?

A: Please run PowerShell or terminal as administrator.

#### Q: How to update cc-switch?

A: Delete the `cc-switch` directory and re-run the configuration process to auto-download the latest version.

#### Q: How to configure API Key?

A: After launching cc-switch, right-click the system tray icon to open the interface and add provider configurations.

### 🤝 Contributing

Issues and Pull Requests are welcome!

### 📄 License

This project is licensed under the [MIT License](LICENSE).

***

## 🔗 Related Links

- [Claude Code](https://github.com/anthropics/claude-code) - Official Claude Code repository
- [cc-switch](https://github.com/farion1231/cc-switch) - cc-switch official repository
- [Node.js](https://nodejs.org/) - Node.js official website

***

<p align="center">
  Made with ❤️ for Claude Code users
</p>
