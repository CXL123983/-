# 🖥️ Codex配置教程

欢迎使用 Codex 桌面应用！这是最适合新手的版本，拥有直观的图形界面，操作简单易上手。

## 📋 目录

[Windows](#windows)
[macOS](#macos)
[Linux](#linux)
[常见问题解答](#常见问题解答)
[1、安装问题](#1、安装问题)
[2、配置问题](#2、配置问题)

### 获取 API 密钥

1. 登录[API 密钥 - 拓垦API](https://token.gepinkeji.com/keys)，进入 **API 密钥** 页面，点击 **创建密钥**
![输入图片说明](https://github.com/CXL123983/-/blob/main/codex/24816166-6415-46b3-84b8-b9ede25e6c9d.png?raw=true)
![输入图片说明](https://github.com/CXL123983/-/blob/main/codex/1d708f55-97d8-468f-b569-c560582ba0f3.png?raw=true)
> **安全提示**：API Key 等同于账号凭证，请妥善保管，切勿提交到代码仓库或公开分享。
2. 复制密钥（格式：`sk-xxxxx`）
![输入图片说明](https://github.com/CXL123983/-/blob/main/codex/dca448ff-05c7-4d4e-896f-a3b35cacc8ae.png?raw=true)
3. 妥善保存

### 安装前检查

**Windows**：
- 确保有管理员权限
- 至少 2GB 可用磁盘空间
- 稳定的网络连接

**macOS**：
- 确保有管理员密码
- 允许安装来自未知开发者的应用
- 至少 2GB 可用磁盘空间

**Linux**：
- 确保有 sudo 权限
- 至少 2GB 可用磁盘空间
- 依赖系统库：glibc 2.17+


## Windows

### 第一步：下载安装包

1. 访问[ Codex 官网](https://openai.com/zh-Hans-CN/codex/)或[ GitHub Releases 页面](https://github.com/openai/codex/releases)
![输入图片说明](https://github.com/CXL123983/-/blob/main/codex/ee50078e-dac6-4f14-af82-2d9ad2bf4a3c.png?raw=true)
2. 选择 Windows 版本下载（文件名如：`Codex-Setup-x.x.x.exe`）
![输入图片说明](https://github.com/CXL123983/-/blob/main/codex/cad73569-ba4e-42b8-b415-07ba8a645ac9.png?raw=true)
3. 等待下载完成（约 100-200MB）
![输入图片说明](https://github.com/CXL123983/-/blob/main/codex/58faf2e9-dc13-4e00-abb9-a295d99467cb.png?raw=true)
### 第二步：安装应用

1. 找到下载的 `.exe` 安装包
2. **右键点击** → 选择"以管理员身份运行"
![输入图片说明](https://github.com/CXL123983/-/blob/main/codex/0f69dc74-4d2c-427d-bd07-12a37ae3e22b.png?raw=true)
![输入图片说明](https://github.com/CXL123983/-/blob/main/codex/58faf2e9-dc13-4e00-abb9-a295d99467cb.png?raw=trueg)
3. 如果弹出安全警告，点击"是"
4. 在安装向导中：
   - 点击"下一步"
   - 选择安装路径（默认：`C:\Program Files\Codex`）
   - 勾选"创建桌面快捷方式"
   - 点击"安装"
5. 等待安装完成（约 1-2 分钟）
6. 点击"完成"

### 第三步：启动应用

**方式一：从桌面启动**
- 双击桌面上的 Codex 图标

**方式二：从开始菜单启动**
- 点击开始菜单
- 搜索 "Codex"
![输入图片说明](/https://github.com/CXL123983/-/blob/main/codex/45d98e6a-5a4b-40ac-ba63-b4b45f56a93c.png?raw=true)
- 点击应用图标

### 第四步：首次配置

1. 应用启动后会弹出配置向导
2. 使用 ChatGPT 账号或 API Key 登录
![输入图片说明](/https://github.com/CXL123983/-/blob/main/codex/b00764b9-fd8c-4d27-80f9-5bd458c36141.png?raw=true)
3. 输入你的 API 密钥：
   ```
   sk-xxxxx（替换为你的真实密钥）
   ```
   ![输入图片说明](https://github.com/CXL123983/-/blob/main/codex/cea8da14-08fb-4bb2-a78d-31213563b3f3.png?raw=true)
4. 选择 API 站点：
   - 点击"自定义 API 站点"
   - 输入：`https://api.gpapi.com/v1`
5. 选择模型版本：

| 模型 | 特点 | 适用场景 |
|------|------|---------|
| gpt-5.4 | OpenAI最新旗舰模型，统一Codex和GPT系列，1M+上下文窗口，支持文本和图像输入 | 生产代码、复杂任务、高上下文推理、多模态分析 |
| gpt-5.4-pro | 极致性能版本，专为最难问题设计，ARC-AGI-2测试达83.3% | 专业研究、极端复杂推理、顶尖工程任务 |
| gpt-5.4-thinking | 全能旗舰，综合能力最强，专业工作能力达人类专家水平 | 日常使用、专业工作、端到端任务执行 |

**推荐选择**：`gpt-5.4-thinking`
6. 选择推理级别：

| 级别 | 特点 | 速度 | 质量 |
|------|------|------|------|
| High | 最高质量 | 慢 | 最高 |
| Medium | 平衡模式 | 中等 | 中等 |
| Low | 快速响应 | 快 | 基础 |

**建议选择**：`High`（最高质量）

7. 点击"测试连接"
8. 如果测试成功，点击"保存并继续"
9. 选择界面语言（中文/英文）
10. 点击"完成"


## macOS

### 第一步：下载安装包

1. 访问[ Codex 官网](https://openai.com/zh-Hans-CN/codex/)或[ GitHub Releases 页面](https://github.com/openai/codex/releases)
2. 选择 macOS 版本下载（文件名如：`Codex-x.x.x.dmg`）
3. 等待下载完成（约 150-250MB）

### 第二步：安装应用

1. 打开下载的 `.dmg` 文件
2. 你会看到一个窗口，里面有 Codex 应用图标和"应用程序"文件夹图标
3. 拖拽 Codex 图标到"应用程序"文件夹
4. 等待复制完成（约 30 秒）
5. 弹出窗口可以关闭

### 第三步：解决安全警告（如果出现）

如果你在首次启动时看到安全警告：

**方法一：系统设置解除**
1. 打开"系统设置" → "隐私与安全性"
2. 找到 "Codex 已被阻止" 的消息
3. 点击"仍要打开"
4. 输入管理员密码
5. 点击"打开"

**方法二：右键菜单打开**
1. 在 Finder 中找到 Codex 应用
2. **右键点击** Codex 图标
3. 按住 **Option 键**，点击"打开"
4. 点击"打开"确认

### 第四步：启动应用
**首次启动：**
1. 按照上述"第三步"的方法，解决安全警告（如果出现）
2. 然后使用以下方式启动：

**方式一：从启动台启动**
- 打开启动台（Launchpad）
- 找到并点击 Codex 图标

**方式二：从应用程序文件夹启动**
- 打开 Finder
- 进入"应用程序"文件夹
- 双击 Codex 应用

### 第五步：首次配置

配置流程与 Windows 相同，参考上述"首次配置"部分。


## Linux

### 方式一：使用 AppImage（推荐）

#### 第一步：下载 AppImage

1. 访问[ Codex 官网](https://openai.com/zh-Hans-CN/codex/)或[ GitHub Releases 页面](https://github.com/openai/codex/releases)
2. 选择 Linux AppImage 版本下载（文件名如：`Codex-x.x.x.AppImage`）
3. 等待下载完成（约 100-200MB）

#### 第二步：设置执行权限

打开终端，执行：

```bash
# 进入下载目录
cd ~/Downloads

# 设置执行权限
chmod +x Codex-x.x.x.AppImage
```

#### 第三步：运行应用

```bash
# 直接运行
./Codex-x.x.x.AppImage
```

#### 第四步：创建桌面快捷方式（可选）

**建议先将AppImage移动到固定位置：**

```bash
# 创建本地应用目录
mkdir -p ~/.local/bin

# 移动AppImage到固定位置
mv ~/Downloads/Codex-x.x.x.AppImage ~/.local/bin/codex.AppImage
```


**创建桌面快捷方式：**

```bash
# 创建 .desktop 文件
cat > ~/.local/share/applications/codex.desktop << EOF
[Desktop Entry]
Name=Codex
Comment=AI Programming Assistant
Exec=/home/$USER/.local/bin/codex.AppImage
Icon=codex
Terminal=false
Type=Application
Categories=Development;
EOF

# 更新桌面数据库
update-desktop-database ~/.local/share/applications/
```

> **注意**：
> - 如果你移动了AppImage文件的位置，需要更新桌面快捷方式中的路径
> - `Icon=codex` 需要图标文件存在。你可以：
>   1. 下载Codex图标并放置在 `~/.local/share/icons/` 目录
>   2. 或修改 .desktop 文件使用通用图标：`Icon=applications-development`
>   3. 或指定图标文件的完整路径：`Icon=/home/$USER/.local/share/icons/codex.png`
#### 第五步：首次配置

1. 应用启动后会弹出配置向导
2. 使用 ChatGPT 账号或 API Key 登录
3. 输入你的 API 密钥：
   ```
   sk-xxxxx（替换为你的真实密钥）
   ```
4. 选择 API 站点：
   - 点击"自定义 API 站点"
   - 输入：`https://api.gpapi.com/v1`
5. 选择模型版本：

| 模型 | 特点 | 适用场景 |
|------|------|---------|
| gpt-5.4 | OpenAI最新旗舰模型，统一Codex和GPT系列，1M+上下文窗口，支持文本和图像输入 | 生产代码、复杂任务、高上下文推理、多模态分析 |
| gpt-5.4-pro | 极致性能版本，专为最难问题设计，ARC-AGI-2测试达83.3% | 专业研究、极端复杂推理、顶尖工程任务 |
| gpt-5.4-thinking | 全能旗舰，综合能力最强，专业工作能力达人类专家水平 | 日常使用、专业工作、端到端任务执行 |

**推荐选择**：`gpt-5.4-thinking`

6. 选择推理级别：

| 级别 | 特点 | 速度 | 质量 |
|------|------|------|------|
| High | 最高质量 | 慢 | 最高 |
| Medium | 平衡模式 | 中等 | 中等 |
| Low | 快速响应 | 快 | 基础 |

7. 点击"测试连接"
8. 如果测试成功，点击"保存并继续"
9. 选择界面语言（中文/英文）
10. 点击"完成"


### 方式二：使用 .deb 包（Ubuntu/Debian）

#### 第一步：下载 .deb 包

1. 访问[ Codex 官网](https://openai.com/zh-Hans-CN/codex/)或[ GitHub Releases 页面](https://github.com/openai/codex/releases)
2. 选择 Debian/Ubuntu 版本下载（文件名如：`codex-x.x.x.deb`）

#### 第二步：安装

```bash
# 进入下载目录
cd ~/Downloads

# 安装 .deb 包
sudo dpkg -i codex-x.x.x.deb

# 修复可能的依赖问题
sudo apt-get install -f
```

#### 第三步：启动
**首次启动前检查配置目录**：

```bash
# 确保配置目录存在
mkdir -p ~/.config/Codex
```

从应用菜单或终端输入 `codex` 启动。
#### 第四步：首次配置

配置流程与 AppImage 方式相同，参考上述"第五步：首次配置"部分。


### 方式三：使用 .rpm 包（Fedora/CentOS）

#### 第一步：下载 .rpm 包

1. 访问[ Codex 官网](https://openai.com/zh-Hans-CN/codex/)或[ GitHub Releases 页面](https://github.com/openai/codex/releases)
2. 选择 Fedora/RHEL 版本下载（文件名如：`codex-x.x.x.rpm`）

#### 第二步：安装

```bash
# 进入下载目录
cd ~/Downloads

# 安装 .rpm 包
sudo dnf install codex-x.x.x.rpm

# 或使用 yum（CentOS/RHEL）
sudo yum install codex-x.x.x.rpm
```

#### 第三步：启动
**首次启动前检查配置目录**：

```bash
# 确保配置目录存在
mkdir -p ~/.config/Codex
```
从应用菜单或终端输入 `codex` 启动。
#### 第四步：首次配置

配置流程与 AppImage 方式相同，参考上述"第五步：首次配置"部分。



## 常见问题解答

### 1、安装问题

**Q: Windows 安装时提示"此应用无法在你的 PC 上运行"**
- 确保下载的是 Windows 64位版本
- 检查系统版本是否为 Windows 10 或更高
- 尝试以管理员身份运行安装程序

**Q: macOS 提示"已损坏，无法打开"**
- 这是因为应用未签名，这是正常的
- 参考"解决安全警告"部分的方法解除限制
- 或在终端执行：`sudo xattr -cr /Applications/Codex.app`

**Q: Linux AppImage 无法运行**
- 确保已设置执行权限：`chmod +x xxx.AppImage`
- 检查是否安装了必要的系统库：`ldd xxx.AppImage`
- 尝试安装 FUSE 库：
  - Ubuntu/Debian: `sudo apt install libfuse2`
  - Fedora: `sudo dnf install fuse`

### 2、配置问题

**Q: 测试 API 连接失败**
- 检查 API 密钥是否正确
- 确认网络连接正常
- 检查 API 端点地址：`https://api.gpapi.com/v1`
- 尝试在浏览器访问 API 站点确认是否可访问

**Q: 提示"密钥无效"或"额度不足"**
- 重新检查 API 密钥格式（应为 `sk-xxxxx`）
- 确认 API 站点上的密钥状态是否正常
- 检查是否有足够的调用额度

**Q: 如何更换 API 密钥？**
- 打开设置 → API 设置
- 点击"更改密钥"
- 输入新的 API 密钥
- 点击"保存并测试"



