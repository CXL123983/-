# VS Code Codex 插件配置教程

欢迎使用 VS Code Codex 插件！这是专为 VS Code 用户设计的版本，提供深度集成的 AI 编程体验，让 AI 助手无缝融入你的开发工作流。

开始前请先完成[VS-Code环境安装教程](https://github.com/CXL123983/-/blob/main/VS-Code%E7%8E%AF%E5%A2%83%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B.md)和[Node.js环境安装教程](https://github.com/CXL123983/-/blob/main/Node.js%E7%8E%AF%E5%A2%83%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B.md)以及[Codex-CLI配置教程](https://github.com/CXL123983/-/blob/main/Codex-CLI%E9%85%8D%E7%BD%AE%E6%95%99%E7%A8%8B.md)。
## 📋 目录

[Windows](#windows)
[macOS](#macOS)
[Linux](#linux)
[常见问题解答](#常见问题解答)
[1、安装问题](#1、安装问题)
[2、配置问题](#2、配置问题)



## Windows
### 第一步：安装 Codex 插件
**方式一：通过官方网站**

1. 访问[官方网站](https://chatgpt.com/codex)
![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code-Codex/bdd25c8b-e2e0-4545-b0c7-95dc1924cfa4.png?raw=true)
2. 开始安装流程
![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code-Codex/c087ad6f-e01d-4a58-bf75-38d39f964d9e.png?raw=true)
3.跳转到 VS Code 插件市场
系统会引导您安装 VS Code 插件。
点击相应按钮后，会自动跳转到 VS Code 插件市场。
![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code-Codex/ebf70bc0-aa05-403d-a5f9-341eb0e0dbd7.png?raw=true)
4. 完成安装
在 VS Code 插件市场中，点击 “安装” 按钮即可完成 Codex 插件的安装。
安装完成后，您就可以在 VS Code 中使用 Codex 的各项功能了。
![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code-Codex/5223ce12-0c3e-49cc-b868-d6e36f4198cf.png?raw=true)

**方式二：通过[官方插件](https://marketplace.visualstudio.com/items?itemName=openai.chatgpt)**

**方式三：通过命令行**

打开 PowerShell 或 CMD：

```powershell
code --install-extension openai.chatgpt
```

### 第二步：登录认证
1. 重启VS Code
2. 在**右侧边栏**找到Codex图标
3. 点击"Sign in"
4. 使用ChatGPT账号登录

### 第三步：配置 API 密钥

**通过设置：**
1. 按 Ctrl + , 打开设置
2. 搜索"Codex"
3. 找到"Codex: API Key"
4. 粘贴你的API密钥
5. 保存设置


### 第四步：选择模型
1. 在Codex聊天界面中
2. 点击模型下拉菜单
3. 选择模型版本

| 模型 | 特点 | 适用场景 |
|------|------|---------|
| gpt-5.4 | OpenAI最新旗舰模型，统一Codex和GPT系列，1M+上下文窗口，支持文本和图像输入 | 生产代码、复杂任务、高上下文推理、多模态分析 |
| gpt-5.4-pro | 极致性能版本，专为最难问题设计，ARC-AGI-2测试达83.3% | 专业研究、极端复杂推理、顶尖工程任务 |
| gpt-5.4-thinking | 全能旗舰，综合能力最强，专业工作能力达人类专家水平 | 日常使用、专业工作、端到端任务执行 |

**推荐选择**：`gpt-5.4-thinking`

### 第五步：设置推理级别（可选）
1. 在Codex设置中
2. 找到"Codex: Reasoning Effort"
3. 选择：High / Medium / Low
   - High：最高质量，速度最慢
   - Medium：平衡模式
   - Low：快速响应，质量较低

### 第六步：验证安装

1. 在VS Code中打开任意代码文件
2. 点击右侧边栏的Codex图标
3. 如果看到Codex面板，说明安装成功
4. 尝试输入消息，测试API连接


## macOS
### 第一步：安装 Codex 插件
1. 打开VS Code
2. 点击左侧扩展图标（或按 Cmd + Shift + X）
3. 在搜索框输入"Codex"
4. 找到"Codex – OpenAI's coding agent"
5. 点击"Install"按钮

### 第二步：登录认证
1. 重启VS Code
2. 在**右侧边栏**找到Codex图标
3. 点击"Sign in"
4. 选择登录方式：
   - **使用ChatGPT账号**（推荐，有订阅计划直接可用）
   - **使用API密钥**（需额外配置，参考第三步）

### 第三步：配置 API 密钥

1. 按 Cmd + , 打开设置
2. 搜索"Codex"
3. 找到"Codex: API Key"
4. 粘贴你的API密钥
5. 等待扩展自动保存配置


**通过配置文件：**

```json
{
  "openai-codex.apiKey": "sk-xxxxx",
  "openai-codex.baseUrl": "https://api.gpapi.com/v1",
  "openai-codex.model": "gpt-5.4",
  "openai-codex.reasoningEffort": "high"
}
```

### 第三步：选择模型和设置
1. 在Codex聊天界面中
2. 点击模型下拉菜单
3. 选择模型版本

| 模型 | 特点 | 适用场景 |
|------|------|---------|
| gpt-5.4 | OpenAI最新旗舰模型，统一Codex和GPT系列，1M+上下文窗口，支持文本和图像输入 | 生产代码、复杂任务、高上下文推理、多模态分析 |
| gpt-5.4-pro | 极致性能版本，专为最难问题设计，ARC-AGI-2测试达83.3% | 专业研究、极端复杂推理、顶尖工程任务 |
| gpt-5.4-thinking | 全能旗舰，综合能力最强，专业工作能力达人类专家水平 | 日常使用、专业工作、端到端任务执行 |

**推荐选择**：`gpt-5.4-thinking`


## Linux

### 第一步：安装 Codex 插件
**方式一：通过 VS Code 扩展市场（推荐）**
1. 打开 VS Code
2. 点击左侧扩展图标（或按 `Ctrl + Shift + X`）
3. 在搜索框中输入 "Codex"
4. 找到"Codex – OpenAI's coding agent"（发布者：OpenAI）
5. 点击"安装"
6. 等待安装完成

**方式二：通过命令行**
打开终端，执行：

```bash
code --install-extension openai.chatgpt
```
### 第二步：登录认证
1. 重启VS Code
2. 在**右侧边栏**找到Codex图标
3. 点击"Sign in"
4. 选择登录方式：
   - **使用ChatGPT账号**（推荐，有订阅计划直接可用）
   - **使用API密钥**（需额外配置）


### 第三步：配置 API 密钥（如使用API密钥登录）

**通过设置：**

1. 按 Ctrl + , 打开设置
2. 搜索"Codex"
3. 找到"Codex: API Key"
4. 粘贴你的OpenAI API密钥
5. 保存设置

**通过配置文件：**

1. 编辑配置文件：
   ```bash
   code ~/.config/Code/User/settings.json
   ```

2. 添加配置：
   ```json
   {
     "openai-codex.apiKey": "sk-xxxxx",
     "openai-codex.baseUrl": "https://api.gpapi.com/v1",
     "openai-codex.model": "gpt-5.4",
     "openai-codex.reasoningEffort": "high"
   }
   ```

**验证安装：**

```bash
code --list-extensions | grep chatgpt
# 如果显示 openai.chatgpt，说明安装成功
```

### 第四步：选择模型和设置（图形界面）
1. 在Codex聊天界面中
2. 点击模型下拉菜单
3. 选择模型版本

| 模型 | 特点 | 适用场景 |
|------|------|---------|
| gpt-5.4 | OpenAI最新旗舰模型，统一Codex和GPT系列，1M+上下文窗口，支持文本和图像输入 | 生产代码、复杂任务、高上下文推理、多模态分析 |
| gpt-5.4-pro | 极致性能版本，专为最难问题设计，ARC-AGI-2测试达83.3% | 专业研究、极端复杂推理、顶尖工程任务 |
| gpt-5.4-thinking | 全能旗舰，综合能力最强，专业工作能力达人类专家水平 | 日常使用、专业工作、端到端任务执行 |

**推荐选择**：`gpt-5.4-thinking`




## 常见问题解答

### 1、安装问题

**Q: 插件安装失败**

1. 检查 VS Code 版本（需 >= 1.75）
2. 尝试重启 VS Code
3. 检查网络连接
4. 尝试使用命令行安装：

```bash
code --install-extension openai.chatgpt
```

**Q: 找不到 Codex 图标**

1. 确认插件已安装（在扩展列表中查看）
2. 尝试禁用后重新启用插件
3. 重启 VS Code
4. 通过命令面板打开："Codex: Open Panel"

**Q: 内联补全不工作**

1. 检查是否已启用："Codex: Enable Inline Completion"
2. 检查设置中的 `openai-codex.inlineCompletion.enable`
3. 尝试手动触发：`Ctrl/Cmd + Alt + /`
4. 检查 API 密钥配置

### 2、配置问题

**Q: API Key 无效**

1. 检查密钥格式（`sk-xxxxx`）
2. 确认 API 端点配置正确
3. 测试 API 连接："Codex: Test Connection"
4. 检查 API 站点状态

**Q: 如何更换 API 密钥？**

1. `Ctrl/Cmd + Shift + P` → "Codex: Set API Key"
2. 或在设置中修改：`openai-codex.apiKey`

**Q: 配置不生效**

1. 确认 JSON 格式正确（无语法错误）
2. 尝试重新加载窗口：`Ctrl/Cmd + Shift + P` → "Developer: Reload Window"
3. 检查是否有工作区配置覆盖了用户配置
