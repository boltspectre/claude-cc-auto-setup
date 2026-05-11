# AI 提示词：自动化环境配置（Node.js, Claude Code, cc switch）

## 目标
在当前环境中**全自动**完成：
1. 检测 Node.js
2. 安装 Claude Code（不需要配置 API Key）
3. 下载并启动 cc switch（用于配置密钥和管理供应商）

**所有下载地址由 AI 自动搜索获取，用户不需要配置任何参数。**

## 详细步骤

### 步骤 1：检测 Node.js
- 运行 `node --version` 检测是否已安装
- 如果未安装，自动搜索下载最新 LTS 版本并安装

### 步骤 2：安装 Claude Code
- 执行 `npm install -g @anthropic-ai/claude-code`
- 运行 `claude --version` 验证安装
- **不需要配置 API Key，不需要创建任何配置文件**

### 步骤 3：下载并启动 cc switch
- 使用 WebSearch 搜索 "cc switch GitHub release download"
- 使用 WebFetch 访问 `https://github.com/farion1231/cc-switch/releases/latest` 获取最新版下载 URL
- 下载对应系统的版本到当前目录
- 解压到 `.\cc-switch\`
- 启动并验证进程

## 输出示例
```
## 📋 环境配置完成

### ✅ 执行状态
| 步骤 | 状态 | 详情 |
|------|------|------|
| Node.js 检测 | ✅ | vXX.XX.X |
| Claude Code 安装 | ✅ | vX.X.X |
| cc switch 下载并启动 | ✅ | 正在运行 (PID: XXXXX) |

### 📝 使用说明
1. **Claude Code**：终端运行 `claude`
2. **cc switch**：系统托盘图标打开界面，配置 API Key 和管理供应商
```

## 注意事项
- 所有下载地址必须从 GitHub 自动搜索获取
- 所有文件下载到 `./cc-switch/`，不创建多余文件

现在根据文档做一个plan，然后开始执行
