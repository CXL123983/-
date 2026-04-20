# 💬 Chatbox 配置教程


## 📋 目录

[Windows ](#windows)
[macOS](#macos)
[Linux](#linux)
[常见问题解答](#常见问题解答)
[1、安装问题](#1、安装问题)
[2、配置问题](#2、配置问题)

## Windows 

### 第一步：下载安装包
1. 访问[Chatbox 官网](https://chatboxai.app/zh)
![输入图片说明](/imgs/2026-04-16/vj73u6JHSmFBcChj.png)
2. 选择 Windows 版本下载
![输入图片说明](/imgs/2026-04-16/N0k9ZnAU7YqMTRUx.png)
3. 文件名如：`Chatbox-Setup-x.x.x.exe`
4. 等待下载完成（约 80-150MB）

### 第二步：安装应用

1. 找到下载的 `.exe` 安装包
2. **右键点击** → 选择"以管理员身份运行"
3. 如果弹出安全警告，点击"是"
4. 在安装向导中：
   - 点击"下一步"
   - 选择安装路径（默认：`C:\Program Files\Chatbox`）
   - 勾选"创建桌面快捷方式"
   - 点击"安装"
5. 等待安装完成（约 1-2 分钟）
6. 点击"完成"

### 第三步：启动应用
**方式一：从桌面启动**
- 双击桌面上的 Chatbox 图标

**方式二：从开始菜单启动**
- 点击开始菜单
- 搜索 "Chatbox"
- 点击应用图标

### 第四步：创建API Key
1. 登录 [GPAPI控制台](http://192.168.3.92:3000/login)，进入 **API 密钥** 页面，点击 **创建密钥**
![输入图片说明](/imgs/2026-04-16/W1WUabNUfgeaL63F.png)
![输入图片说明](/imgs/2026-04-16/Pa9uY0zlNp6NGf1z.png)
> **安全提示**：API Key 等同于账号凭证，请妥善保管，切勿提交到代码仓库或公开分享。
2. 复制密钥（格式：`sk-xxxxx`）
![输入图片说明](/imgs/2026-04-18/DMp0WRKIHmQINVBM.png)
3. 妥善保存
### 第五步：导入密钥到Chatbox

1. 应用启动后会显示欢迎界面
2. 点击"开始使用"
3. 输入你的 API 密钥：
   ```
   sk-xxxxx（替换为你的真实密钥）
   ```
4. 选择 API 站点：
   - 点击"高级设置"
   - 在"自定义 API 端点"中输入：`https://api.gpapi.com/v1`
5. 选择模型
6. 点击"测试连接"
7. 如果测试成功，点击"保存并继续"
8. 选择界面语言（中文/英文）
9. 点击"完成"


## macOS

### 第一步：下载安装包

1. 访问[Chatbox 官网](https://chatboxai.app/zh)
![输入图片说明](/imgs/2026-04-16/p2OikLZZS8yX32Vp.png)
2. 选择 macOS 版本下载
![输入图片说明](/imgs/2026-04-16/gvIKtJixyOFZcLx6.png)
3. 文件名如：`Chatbox-x.x.x.dmg`
4. 等待下载完成（约 100-180MB）

### 第二步：安装应用

1. 打开下载的 `.dmg` 文件
2. 你会看到一个窗口，里面有 Chatbox 图标和"应用程序"文件夹
3. 拖拽 Chatbox 图标到"应用程序"文件夹
4. 等待复制完成（约 30 秒）
5. 弹出窗口可以关闭

### 第三步：解决安全警告（如果出现）

如果你在首次启动时看到安全警告：

**方法一：系统设置解除**
1. 打开"系统设置" → "隐私与安全性"
2. 找到 "Chatbox 已被阻止" 的消息
3. 点击"仍要打开"
4. 输入管理员密码
5. 点击"打开"

**方法二：右键菜单打开**
1. 在 Finder 中找到 Chatbox 应用
2. **右键点击** Chatbox 图标
3. 按住 **Option 键**，点击"打开"
4. 点击"打开"确认

### 第四步：启动应用

**方式一：从启动台启动**
- 打开启动台（Launchpad）
- 找到并点击 Chatbox 图标

**方式二：从应用程序文件夹启动**
- 打开 Finder
- 进入"应用程序"文件夹
- 双击 Chatbox 应用




##  Linux 

### 方式一：使用 AppImage（推荐）

#### 第一步：下载 AppImage

1. 访问[Chatbox 官网](https://chatboxai.app/zh)
![输入图片说明](/imgs/2026-04-16/EXyE6sIOfkzgGbur.png)
2. 选择 Linux AppImage 版本下载
![输入图片说明](/imgs/2026-04-16/sdXJWpPWFhZ36CjW.png)
3. 文件名如：`Chatbox-x.x.x.AppImage`
4. 等待下载完成（约 80-150MB）

#### 第二步：设置执行权限

打开终端，执行：

```bash
# 进入下载目录
cd ~/Downloads

# 设置执行权限
chmod +x Chatbox-x.x.x.AppImage
```

#### 第三步：运行应用

```bash
# 直接运行
./Chatbox-x.x.x.AppImage
```

#### 第四步：创建桌面快捷方式（可选）

**建议先将AppImage移动到固定位置：**

```bash
# 创建本地应用目录
mkdir -p ~/.local/bin

# 移动AppImage到固定位置
mv ~/Downloads/Chatbox-x.x.x.AppImage ~/.local/bin/chatbox.AppImage
```

**创建桌面快捷方式：**

```bash
# 创建 .desktop 文件
cat > ~/.local/share/applications/chatbox.desktop << EOF
[Desktop Entry]
Name=Chatbox
Comment=AI Chat Assistant
Exec=/home/$USER/.local/bin/chatbox.AppImage
Icon=chatbox
Terminal=false
Type=Application
Categories=Development;Utility;
EOF

# 更新桌面数据库
update-desktop-database ~/.local/share/applications/
```

> **注意**：如果你移动了AppImage文件的位置，需要更新桌面快捷方式中的路径。

### 方式二：使用 .deb 包（Ubuntu/Debian）

#### 第一步：下载 .deb 包

1. 访问[Chatbox 官网](https://chatboxai.app/zh)
2. 选择 Debian/Ubuntu 版本下载
3. 文件名如：`chatbox-x.x.x.deb`

#### 第二步：安装

```bash
# 进入下载目录
cd ~/Downloads

# 安装 .deb 包
sudo dpkg -i chatbox-x.x.x.deb

# 修复可能的依赖问题
sudo apt-get install -f
```

#### 第三步：启动

从应用菜单或终端输入 `chatbox` 启动。

### 方式三：使用 .rpm 包（Fedora/CentOS）

#### 第一步：下载 .rpm 包

1. 访问[Chatbox 官网](https://chatboxai.app/zh)
2. 选择 Fedora/RHEL 版本下载
3. 文件名如：`chatbox-x.x.x.rpm`

#### 第二步：安装

```bash
# 进入下载目录
cd ~/Downloads

# 安装 .rpm 包
sudo dnf install chatbox-x.x.x.rpm

# 或使用 yum（CentOS/RHEL）
sudo yum install chatbox-x.x.x.rpm
```

#### 第三步：启动

从应用菜单或终端输入 `chatbox` 启动。


## 网页版使用指南

### 第一步：访问网页

1. 打开浏览器
2. 访问 [Chatbox 网页版地址](https://web.chatboxai.app/guide)
3. 等待页面加载完成

### 第二步：登录或注册

1. 如果已有账号，点击"登录"
2. 输入邮箱和密码
3. 点击"登录"

如果没有账号：
1. 点击"注册"
2. 填写注册信息
3. 完成邮箱验证
4. 登录账号

### 第三步：配置 API 密钥

1. 点击的"设置"图标，一般在左下角侧边栏找到设置入口
![输入图片说明](/imgs/2026-04-18/itOMAQ1a1h5n572H.png)
2. 选择模型提供方
![输入图片说明](/imgs/2026-04-18/IUX2amz95yqLAlAj.png)
3. 输入你的 API 密钥
4. 填写 API Base URL：`https://api.gpapi.com/v1`
![输入图片说明](/imgs/2026-04-18/I8WG9lYXU7VUC3y9.png)
5. 选择模型版本
6. 保存配置
### 第四步：开始聊天

1. 在输入框中输入你的问题或需求
2. 点击发送按钮或按 Enter 键
3. 查看 AI 的回复


### 常见问题解答

### 1、安装问题

**Q: Windows 安装时提示"无法运行此应用"**

1. 确保下载的是 Windows 64位版本
2. 以管理员身份运行安装程序
3. 检查系统版本是否为 Windows 10 或更高

**Q: macOS 提示"已损坏"**

这是因为应用未签名，是正常的。解决方法：
- 打开"系统设置" → "隐私与安全性"
- 找到 "Chatbox 已被阻止"
- 点击"仍要打开"

**Q: Linux AppImage 无法运行**

1. 确保已设置执行权限：`chmod +x xxx.AppImage`
2. 检查是否安装了必要的库：
   - Ubuntu/Debian: `sudo apt install libfuse2`
   - Fedora: `sudo dnf install fuse`

### 2、配置问题

**Q: API Key 无效**

1. 检查密钥格式（`sk-xxxxx`）
2. 确认 API 端点地址正确：`https://api.gpapi.com/v1`
3. 验证密钥状态是否正常
4. 检查网络连接

**Q: 如何更换 API 密钥？**

1. 打开设置
2. 进入"API 设置"
3. 删除旧密钥
4. 输入新密钥
5. 点击"保存"

**Q: 网页版和桌面版数据不同步**

网页版和桌面版是独立的，数据不会自动同步。如果需要同步：
- 导出对话历史（网页版）
- 在桌面版导入
- 或使用相同的配置重新开始

