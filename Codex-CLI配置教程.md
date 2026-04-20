
Codex CLI 配置教程

Codex 是支持 OpenAI API 兼容接口的 CLI 工具，使用配置文件的方式进行设置。本教程涵盖 Windows、macOS 和 Linux 的安装和配置。

Codex CLI依赖 Node.js 运行环境，请先参考[Node.js环境安装教程](/%E6%8E%A5%E5%85%A5%E6%96%87%E6%A1%A3/Node.js%E7%8E%AF%E5%A2%83%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B.md)完成安装并验证。
## 📋 目录

[Windows](#windows-)
[macOS](#macos-安装指南)
[Linux](#linux-安装指南)
[配置详解](#配置详解)
[常见问题解答](#常见问题解答)
[1、安装问题](#1、安装问题)
[2、配置问题](#2、配置问题)




## Windows 

### 第一步：安装 Codex CLI

**方式一：使用 CMD/PowerShell**

1. 以管理员身份打开 CMD 或 PowerShell
2. 执行以下命令：

```bash
npm install -g @openai/codex
```
![输入图片说明](/imgs/2026-04-16/qfONxCPEfXFc5NqU.png)
以上命令会从 npm 官方仓库下载并安装最新版本的 Codex 工具。

3. 等待安装完成（可能需要 2-5 分钟）
![输入图片说明](/imgs/2026-04-16/cTfoAWW4xld2Zhbv.png)

**方式二：使用 Git Bash**

1. 打开 Git Bash
2. 执行相同的命令：

```bash
npm install -g @openai/codex
```
### 第二步：验证安装

```bash
codex --version
```
![输入图片说明](/imgs/2026-04-16/L4Ozzt1lxL0JXP7w.png)

如果显示版本号，恭喜你！Codex 已经成功安装了。
### 第三步：获取API密钥
1. 登录 [GPAPI控制台](http://192.168.3.92:3000/login)，进入 **API 密钥** 页面，点击 **创建密钥**
![输入图片说明](/imgs/2026-04-18/2yWEz4escUgx8aRY.png)
![输入图片说明](/imgs/2026-04-18/CmRhUAwjxsLoJ6bA.png)
> **安全提示**：API Key 等同于账号凭证，请妥善保管，切勿提交到代码仓库或公开分享。
2. 复制密钥（格式：`sk-xxxxx`）
![输入图片说明](/imgs/2026-04-18/gd9q1C4aZGGN3W0B.png)
3. 妥善保存
### 第四步：创建配置目录
Codex 使用配置文件进行连接设置，需要创建 `config.toml` 和 `auth.json` 两个文件。
1. 打开文件资源管理器
2. 进入用户目录：`C:\Users\你的用户名`
3. 如果看不到隐藏文件，点击"查看"→ 勾选"隐藏的项目"
4. 创建 `.codex` 文件夹

**使用命令创建**：

```bash
# 删除旧目录并创建新目录
if (Test-Path "$env:USERPROFILE\.codex") { Remove-Item -Recurse -Force "$env:USERPROFILE\.codex" }
mkdir "$env:USERPROFILE\.codex"

# Git Bash
mkdir ~/.codex
```

### 第五步：创建配置文件

#### 1、创建 auth.json
点击密钥旁的**复制**按钮获取API Key：

![输入图片说明](/imgs/2026-04-16/ubfHSogs9aLJNtJL.png)

在 `.codex` 文件夹中创建 `auth.json` 文件，将 `YOUR_API_KEY` 替换为你在控制台创建的密钥：
```json
{
  "OPENAI_API_KEY": "sk-xxxxx"
}
```
**注意**：将 `sk-xxxxx` 替换为你的真实 API 密钥。
#### 2、创建 config.toml

在配置目录下创建 `config.toml`：
- Windows: `%USERPROFILE%\.codex\config.toml`
- macOS/Linux: `~/.codex/config.toml`

```toml
model_provider = "GPAPI"
model = "gpt-4.1"
model_reasoning_effort = "high"
disable_response_storage = true
preferred_auth_method = "apikey"

[model_providers.GPAPI]
name = "GPAPI"
base_url = "https://api.gpapi.com/v1"
```
**配置参数说明**：

| 参数 | 说明 | 可选值 |
|------|------|--------|
| `model_provider` | 提供商名称 | `GPAPI` |
| `model` | 使用的模型 | `gpt-4.1`, `gpt-4.1-mini` 等 |
| `model_reasoning_effort` | 推理级别 | `high`, `medium`, `low` |
| `disable_response_storage` | 禁用响应存储 | `true`, `false` |
| `preferred_auth_method` | 认证方式 | `apikey` |
| `base_url` | API 端点 | `https://api.gpapi.com/v1` |

### 第六步：重启终端

**重要**：配置完成后，必须重启终端才能使配置生效！

### 第七步：启动 Codex

1. 进入你的项目目录：

```bash
cd your-project-folder
```

2. 启动 Codex：

```bash
codex
```

3. 如果看到欢迎界面，说明配置成功！
![输入图片说明](/imgs/2026-04-16/2t7myJNOP6w3lTYg.png)

更多使用说明请参考 [OpenAI 官方文档](https://platform.openai.com/docs)。

## macOS

### 第一步：安装 Codex CLI

打开终端（Terminal），执行：

```bash
sudo npm install -g @openai/codex
```

**注意**：
- 需要输入管理员密码
- 输入密码时不会显示任何字符
- 输入完成后按 Enter 确认

### 第二步：验证安装

```bash
codex --version
```
如果显示版本号，恭喜你！Codex 已经成功安装了。
### 第三步：获取API密钥
1. 登录 [GPAPI控制台](http://192.168.3.92:3000/login)，进入 **API 密钥** 页面，点击 **创建密钥**
![输入图片说明](/imgs/2026-04-18/2yWEz4escUgx8aRY.png)
![输入图片说明](/imgs/2026-04-18/CmRhUAwjxsLoJ6bA.png)
> **安全提示**：API Key 等同于账号凭证，请妥善保管，切勿提交到代码仓库或公开分享。
2. 复制密钥（格式：`sk-xxxxx`）
![输入图片说明](/imgs/2026-04-18/gd9q1C4aZGGN3W0B.png)
3. 妥善保存
### 第四步：创建配置目录

```bash
# 删除旧目录并创建新目录
rm -rf ~/.codex && mkdir -p ~/.codex
```

### 第五步：创建配置文件

#### 创建 auth.json

```bash
vi ~/.codex/auth.json
```

按 `i` 进入编辑模式，粘贴以下内容：

```json
{
  "OPENAI_API_KEY": "sk-xxxxx"
}
```

按 `ESC` 键，输入 `:wq` 后按 Enter 保存退出。

#### 创建 config.toml

```bash
vi ~/.codex/config.toml
```

按 `i` 进入编辑模式，粘贴以下内容：

```toml
model_provider = "GPAPI"
model = "gpt-4.1"
model_reasoning_effort = "high"
disable_response_storage = true
preferred_auth_method = "apikey"

[model_providers.GPAPI]
name = "GPAPI"
base_url = "https://api.gpapi.com/v1"
```

按 `ESC` 键，输入 `:wq` 后按 Enter 保存退出。

**替代方案**：使用 VS Code 编辑

如果你不熟悉 vi 编辑器，可以使用 VS Code：

```bash
code ~/.codex/auth.json
code ~/.codex/config.toml
```

### 第六步：重启终端

**重要**：配置完成后，必须重启终端！

### 第七步：启动 Codex

```bash
cd your-project-folder
codex
```



## Linux 安装指南
### 第一步：安装 Codex CLI

```bash
npm install -g @openai/codex
```

如果提示权限不足：

```bash
sudo npm install -g @openai/codex
```

### 第二步：验证安装

```bash
codex --version
```
如果显示版本号，恭喜你！Codex 已经成功安装了。
### 第三步：获取API密钥
1. 登录 [GPAPI控制台](http://192.168.3.92:3000/login)，进入 **API 密钥** 页面，点击 **创建密钥**
![输入图片说明](/imgs/2026-04-18/2yWEz4escUgx8aRY.png)
![输入图片说明](/imgs/2026-04-18/CmRhUAwjxsLoJ6bA.png)
> **安全提示**：API Key 等同于账号凭证，请妥善保管，切勿提交到代码仓库或公开分享。
2. 复制密钥（格式：`sk-xxxxx`）
![输入图片说明](/imgs/2026-04-18/gd9q1C4aZGGN3W0B.png)
3. 妥善保存
### 第四步：创建配置目录

```bash
# 删除旧目录并创建新目录
rm -rf ~/.codex && mkdir -p ~/.codex
```

### 第五步：创建配置文件

#### 创建 auth.json

```bash
vi ~/.codex/auth.json
```

按 `i` 进入编辑模式，粘贴：

```json
{
  "OPENAI_API_KEY": "sk-xxxxx"
}
```

按 `ESC`，输入 `:wq`，按 Enter 保存退出。

#### 创建 config.toml

```bash
vi ~/.codex/config.toml
```

按 `i` 进入编辑模式，粘贴：

```toml
model_provider = "GPAPI"
model = "gpt-4.1"
model_reasoning_effort = "high"
disable_response_storage = true
preferred_auth_method = "apikey"

[model_providers.GPAPI]
name = "GPAPI"
base_url = "https://api.gpapi.com/v1"
```

按 `ESC`，输入 `:wq`，按 Enter 保存退出。

### 第六步：重启终端

**重要**：配置完成后，必须重启终端！

### 第七步：启动 Codex

```bash
cd your-project-folder
codex
```


## 配置详解
### 配置文件位置

| 操作系统 | 配置目录 |
|---------|---------|
| Windows | `C:\Users\用户名\.codex` |
| macOS/Linux | `~/.codex` |

### 配置文件说明

#### auth.json
1. 点击密钥旁的 **复制** 按钮获取 API Key：
![输入图片说明](/imgs/2026-04-16/5xaFVMKjsayMMpHJ.png)

在同一目录下创建 `auth.json`，将 `YOUR_API_KEY` 替换为你在控制台创建的密钥：
```json
{
  "OPENAI_API_KEY": "sk-xxxxx"
}
```

**安全提示**：
- 不要将 `auth.json` 提交到版本控制系统
- 建议添加到 `.gitignore`
- 定期更新 API 密钥

#### config.toml

存储模型和站点配置：

```toml
# 基础配置
model_provider = "GPAPI"
model = "gpt-4.1"
model_reasoning_effort = "high"
disable_response_storage = true
preferred_auth_method = "apikey"

# 自定义提供商配置
[model_providers.GPAPI]
name = "GPAPI"
base_url = "https://api.gpapi.com/v1"
```

### 高级配置选项

#### 推理级别

| 级别 | 说明 | 速度 | 质量 | 适用场景 |
|------|------|------|------|---------|
| `high` | 最高质量 | 慢 | 最高 | 生产代码、复杂问题 |
| `medium` | 平衡模式 | 中等 | 中等 | 日常开发 |
| `low` | 快速响应 | 快 | 基础 | 快速测试、原型 |


### 项目级配置

你可以在项目目录创建 `.codex` 文件夹，放置项目特定的配置：

```
your-project/
├── .codex/
│   ├── auth.json
│   └── config.toml
├── src/
└── package.json
```

项目级配置会覆盖全局配置。

### 环境变量

也可以通过环境变量配置：

**Windows (PowerShell)：**

```powershell
$env:OPENAI_API_KEY="sk-xxxxx"
$env:OPENAI_BASE_URL="https://api.gpapi.com/v1"
```

**macOS/Linux：**

```bash
export OPENAI_API_KEY="sk-xxxxx"
export OPENAI_BASE_URL="https://api.gpapi.com/v1"
```

永久设置（添加到 `~/.bashrc` 或 `~/.zshrc`）：

```bash
echo 'export OPENAI_API_KEY="sk-xxxxx"' >> ~/.bashrc
echo 'export OPENAI_BASE_URL="https://api.gpapi.com/v1"' >> ~/.bashrc
source ~/.bashrc
```


## 斜杠命令

输入 `/` 可以看到所有可用命令：

| 命令 | 说明 | 示例 |
|------|------|------|
| `/mode` | 切换编辑模式 | `/mode auto-edit` |
| `/model` | 切换 AI 模型 | `/model gpt-4.1` |
| `/init` | 创建项目配置 | `/init` |
| `/status` | 查看当前状态 | `/status` |
| `/diff` | 显示 Git 差异 | `/diff` |
| `/clear` | 清除对话历史 | `/clear` |
| `/help` | 显示帮助信息 | `/help` |
| `/exit` | 退出 Codex | `/exit` |



## 常见问题解答

### 1、安装问题

**Q: npm install 失败**

检查 Node.js 版本：
```bash
node --version  # 应该 >= 18
npm --version   # 应该 >= 10
```

如果版本过低，重新安装 Node.js。

**Q: 权限不足**

Windows：以管理员身份运行
macOS/Linux：使用 `sudo`

```bash
sudo npm install -g @openai/codex
```

**Q: 命令找不到**

检查 PATH 环境变量：
```bash
which codex   # macOS/Linux
where codex   # Windows
```

如果没有找到，尝试重新安装或手动添加到 PATH。

### 2、配置问题

**Q: API Key 无效**

1. 检查密钥格式（`sk-xxxxx`）
2. 确认 API 站点地址正确
3. 验证密钥状态是否正常
4. 检查网络连接

**Q: 配置文件不生效**

1. 确认文件位置正确
2. 检查文件名拼写（`.toml` 扩展名）
3. 重启终端
4. 检查 JSON/TOML 语法是否正确

**Q: 如何切换配置**

创建多个配置文件：
```bash
~/.codex/config.dev.toml
~/.codex/config.prod.toml
```

使用时指定：
```bash
codex --config ~/.codex/config.prod.toml
```

