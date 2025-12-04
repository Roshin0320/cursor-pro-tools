<div align="center">
<h1>🚀 Cursor 账号管理器 - 专业的 Cursor IDE 管理工具</h1>

![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS-blue?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

**一键管理您的 Cursor IDE 账户、Token 注入、机器码重置**

[📥 立即下载](#-下载安装) · [📖 使用指南](#-使用指南) · [❓ 常见问题](#-常见问题) · [💬 加入群聊](#-交流群组)

</div>

---

## ✨ 核心功能

### 🔄 账号管理

| 功能                | 说明                                     |
| ------------------- | ---------------------------------------- |
| ✅ **快速切换账号** | 一键切换多个 Cursor Pro 账号，秒级完成   |
| ✅ **Token 注入**   | 直接修改 Cursor 认证数据库，无需复制文件 |
| ✅ **快速导入**     | 一键从当前 Cursor 导入已登录账号         |
| ✅ **会话完整保留** | 切换账号时聊天历史、工作区状态不丢失     |

### 🔑 机器码管理

| 功能              | 说明                           |
| ----------------- | ------------------------------ |
| ✅ **机器码重置** | 重置设备标识，避免封禁风险     |
| ✅ **深度重置**   | 系统级彻底重置，恢复到全新状态 |
| ✅ **自动备份**   | 所有高风险操作都有自动备份机制 |

### 💾 备份恢复

| 功能            | 说明                                     |
| --------------- | ---------------------------------------- |
| ✅ **会话备份** | 备份和恢复 Cursor 会话、工作区、历史记录 |
| ✅ **设置备份** | 备份和恢复编辑器设置、快捷键、代码片段   |
| ✅ **一键恢复** | 出问题时可随时恢复备份                   |

### 🎨 其他特性

| 功能              | 说明                              |
| ----------------- | --------------------------------- |
| ✅ **跨平台支持** | 完美支持 Windows 10/11 和 macOS   |
| ✅ **现代化界面** | 美观易用的图形界面，深色/浅色主题 |
| ✅ **本地存储**   | 所有数据本地存储，不上传任何信息  |

---

## 📦 下载安装

<div align="center">

|                                   📥 **立即下载最新版本**                                    |
| :------------------------------------------------------------------------------------------: |
| 🎯 **[GitHub Releases - 点击下载](https://github.com/Roshin0320/cursor-pro-tools/releases)** |
|                   **💻 支持平台：Windows 10/11 • macOS (Intel & M 芯片)**                    |

</div>

### 🌟 平台兼容性

| 平台        | 架构                  | 格式                   | 状态    |
| ----------- | --------------------- | ---------------------- | ------- |
| **Windows** | x64                   | `.exe` (安装版/便携版) | ✅ 支持 |
| **macOS**   | Intel / Apple Silicon | `.dmg` / `.zip`        | ✅ 支持 |

### 📋 安装步骤

#### Windows 用户

1. 下载 `Cursor账号管理器 Setup x.x.x.exe` (安装版) 或 `Cursor账号管理器 x.x.x.exe` (便携版)
2. 双击运行安装程序
3. 如遇到 SmartScreen 警告，点击 "更多信息" → "仍要运行"

#### macOS 用户

1. 下载 `Cursor账号管理器-x.x.x.dmg` 或 `.zip` 文件
2. 打开 DMG 文件，将应用拖入 Applications 文件夹
3. 如提示 "文件已损坏"，请参考 [常见问题](#q-macos-打开应用提示文件已损坏或无法打开)

---

## 📖 使用指南

### 1️⃣ 添加账号

点击 "添加账号" 按钮，填写以下信息：

- \*\* session
- **邮箱地址**: Cursor 账号的邮箱
- **Access Token**: 从 Cursor 配置中获取的 Token

#### 🔑 如何获取 Token？

<details>
<summary><b>方法一：使用本工具导入（推荐）</b></summary>

1. 在 Cursor 中登录账号
2. 在本工具中点击 **"导入当前账号"**
3. 自动获取当前登录账号的 Token

</details>

<details>
<summary><b>方法二：手动提取</b></summary>

**Mac 系统：**

```bash
sqlite3 "~/Library/Application Support/Cursor/User/globalStorage/state.vscdb" \
  "SELECT value FROM ItemTable WHERE key='cursorAuth/accessToken'"
```

**Windows 系统：**

```cmd
sqlite3 "%APPDATA%\Cursor\User\globalStorage\state.vscdb" \
  "SELECT value FROM ItemTable WHERE key='cursorAuth/accessToken'"
```

</details>

### 2️⃣ 切换账号

1. 在账号列表中选择要切换的账号
2. 点击 **"切换"** 按钮
3. 工具会自动关闭 Cursor 并注入新的 Token
4. 根据设置自动重启 Cursor 或手动启动

> 💡 **提示**：切换账号时，您的所有聊天历史、工作区状态、用户设置都会完整保留！

### 3️⃣ 重置机器码

当频繁切换账号导致被限制时：

1. 点击 **"重置机器码"** 按钮
2. 工具会生成新的设备标识
3. Cursor 会被识别为新设备

> ⚠️ **注意**：重置机器码会清除当前登录状态，需要重新登录

### 4️⃣ 深度重置

执行更彻底的系统级重置：

1. 点击 **"🔥🔥 深度重置 🔥🔥"** 按钮
2. 根据系统执行以下操作：

<details>
<summary><b>Mac 系统</b></summary>

- 修改系统 UUID
- 清除 DNS 缓存
- 修改 Cursor 程序文件
- 移除并重新签名应用

</details>

<details>
<summary><b>Windows 系统（8 个步骤）</b></summary>

- 修改注册表 MachineGuid（需要管理员权限）
- 修改系统标识符（ProductId、InstallDate）
- 清除 DNS 缓存
- 清除网络缓存（ARP、NetBIOS）
- 处理 MAC 地址信息
- 清除 Windows 事件日志
- 清除 Windows 缓存和临时文件
- 修改 Cursor 程序文件（增强版，8 种匹配模式）

</details>

> ⚠️ **重要提示**：
>
> - Windows 需要以 **管理员身份** 运行才能完整执行深度重置
> - Mac 上首次启动修改后的 Cursor 可能需要在 "系统偏好设置 → 安全性" 中允许
> - 建议深度重置后重启计算机

---

## ❓ 常见问题

### Q: macOS 打开应用提示"文件已损坏"或"无法打开"？

这是因为应用未经 Apple 签名，macOS Gatekeeper 会阻止运行。

<details>
<summary><b>🔧 解决方案（点击展开）</b></summary>

**方法一：终端命令（推荐）**

```bash
# 移除隔离属性
xattr -cr /Applications/Cursor账号管理器.app

# 如果上面命令无效，使用 sudo
sudo xattr -rd com.apple.quarantine /Applications/Cursor账号管理器.app
```

**方法二：右键打开**

1. 右键点击应用
2. 选择 "打开"
3. 在弹出对话框中点击 "打开"

**方法三：系统设置**

1. 打开 "系统设置" → "隐私与安全性"
2. 滚动到底部，找到被阻止的应用
3. 点击 "仍要打开"

</details>

---

### Q: 切换账号后 Cursor 无法启动？

<details>
<summary><b>🔧 解决方案</b></summary>

1. 确保在切换前完全关闭了 Cursor
2. 手动强制关闭 Cursor 进程：
   - **Windows**：任务管理器 → 结束 Cursor 进程
   - **Mac**：活动监视器 → 强制退出 Cursor
3. 等待 3-5 秒后再启动

</details>

---

### Q: Token 失效怎么办？

<details>
<summary><b>🔧 解决方案</b></summary>

1. 在 Cursor 中重新登录该账号
2. 使用 **"导入当前账号"** 功能更新 Token

</details>

---

### Q: 重置机器码后仍然被限制？

<details>
<summary><b>🔧 解决方案</b></summary>

1. 检查是否完全清除了缓存
2. 尝试执行 **"深度重置"**
3. 尝试重新安装 Cursor
4. 等待一段时间后再尝试

</details>

---

### Q: Windows 系统中，Cursor 路径应该填写什么？

<details>
<summary><b>🔧 解决方案</b></summary>

应该填写 **Cursor 的文件夹路径**，而不是 exe 文件路径。

**✅ 正确示例：**

- `C:\Users\你的用户名\AppData\Local\Programs\Cursor`
- `C:\Program Files\Cursor`

**❌ 错误示例：**

- `C:\Users\你的用户名\AppData\Local\Programs\Cursor\Cursor.exe`

**常见默认路径：**

- 用户安装：`%LOCALAPPDATA%\Programs\Cursor`
- 系统安装：`%PROGRAMFILES%\Cursor` 或 `%PROGRAMFILES(X86)%\Cursor`

</details>

---

### Q: 备份的数据存储在哪里？

<details>
<summary><b>📂 数据存储位置</b></summary>

**Mac：**

- 应用数据：`~/Library/Application Support/cursor-account-manager/`
- 数据库：`~/Library/Application Support/cursor-account-manager/accounts.db`
- Cursor 配置：`~/Library/Application Support/Cursor/`

**Windows：**

- 应用数据：`%APPDATA%\cursor-account-manager\`
- 数据库：`%APPDATA%\cursor-account-manager\accounts.db`
- Cursor 配置：`%APPDATA%\Cursor\`

</details>

---

## 🔒 安全说明

| 安全特性          | 说明                                   |
| ----------------- | -------------------------------------- |
| ✅ **本地存储**   | 所有账号数据存储在本地 SQLite 数据库中 |
| ✅ **无网络上传** | 不会上传任何数据到远程服务器           |
| ✅ **自动备份**   | 所有高风险操作都有自动备份机制         |
| ✅ **错误恢复**   | 提供恢复功能，可以随时恢复备份         |
| ✅ **数据隔离**   | Token 数据仅用于本地切换账号           |

---

## 💬 交流群组

<div align="center">

|              💬 **QQ 交流群：[872329220]**              |
| :-----------------------------------------------------: |
| 🎯 **使用教程和问题解答 • 版本更新通知 • 用户经验交流** |

<img src="./assets/images/qq-code.jpg" width="400" alt="QQ群二维码">

</div>

**加群须知：**

- 📢 群内会第一时间发布新版本
- 💡 遇到问题可以在群里交流
- 🚫 禁止发布违规内容

---

## ☕ 赞助支持

如果这个项目对你有帮助，欢迎赞助支持！

<div align="center">

|                      微信赞助                       |                       支付宝赞助                        |
| :-------------------------------------------------: | :-----------------------------------------------------: |
| ![微信](./assets/images/wechat-code.jpg) 微信收款码 | ![支付宝](./assets/images/alipay-code.jpg) 支付宝收款码 |

</div>

## ⚖️ 免责声明

> ⚠️ **重要声明**

本工具 **仅供学习和研究使用**，使用本工具所产生的任何后果由使用者自行承担。

- 请遵守 Cursor 的服务条款
- 频繁切换账号可能违反服务协议，请谨慎使用
- 本工具不会收集或上传任何用户数据

This tool is only for learning and research purposes, and any consequences arising from the use of this tool are borne by the user.

---

<div align="center">

**🚀 让 Cursor 智能编程更优雅！**

Made with ❤️ by Roshin

</div>
