
# Node.js 环境安装教程
在 Windows、macOS、Linux 安装 Node.js LTS，并验证 node/npm 命令可用。


后续的CodexCLI工具依赖 Node.js 运行环境。先完成本教程，再继续各自工具配置。

## 📋 目录
[Windows ](#windows)
[macOS](#macOS)
[Linux ](#Linux)
[常见问题](#常见问题)
[下一步](#下一步)

##  Windows
**方法一：官方下载（推荐）**  
1. 访问 [Node.js 官网](https://nodejs.org)
2. 下载最新的 LTS 版本（推荐 22.x）
![输入图片说明](/imgs/2026-04-16/gOsL2CfJisXLRAzo.png)
3. 双击下载后的安装包，如下所示：
![输入图片说明](/imgs/2026-04-16/n3PPMOjmulFvjeTm.png)
4. 点击以上的 Next 按钮，将出现如下界面：
![输入图片说明](/imgs/2026-04-16/23umqWmvnekywHwL.png)
5. 勾选接受协议选项，点击 Next 按钮 :
![输入图片说明](/imgs/2026-04-16/hYlIYcRtitBH2ijd.png)
6. Node.js默认安装目录为 "C:\Program Files\nodejs\" , 你可以修改目录，并点击 Next 按钮：
![输入图片说明](/imgs/2026-04-16/s7yi7SyVo0OPpsjK.png)
7. 点击 Install（安装） 开始安装 Node.js，你也可以点击 Back（返回）来修改先前的配置：

![输入图片说明](/imgs/2026-04-16/XptPguYInXC8dmCq.png)
安装过程：
![输入图片说明](/imgs/2026-04-16/uwHEkoFhDFlbb1h9.png)
点击 Finish（完成）按钮退出安装向导。
![输入图片说明](/imgs/2026-04-16/6oLelSgMeRehZk3W.png).png)
 下载以后，一直下一步直到安装完成
**方法二：包管理器安装**

**使用Winget**
Windows 11 或 Windows 10 最新版：
```
winget install OpenJS.NodeJS.LTS
```
 **使用 Chocolatey**
 需先安装 Chocolatey：
 ```
choco install nodejs-lts
```
**使用 Scoop**
```
scoop install nodejs-lts
```
## 验证安装
打开命令提示符或 PowerShell，执行：
```
node --version
npm --version
```
如果显示版本号（如 v18.x.x 或更高），说明安装成功。
## macOS
**方法一：官方下载（推荐新手）**
1. 前往 [Node.js 官网](https://nodejs.org/) 
![输入图片说明](/imgs/2026-04-17/FtTHW4sWFWyUXyBE.png)
2. 下载 LTS 版本的 .pkg 安装包
![输入图片说明](/imgs/2026-04-16/DArDcg2TmGP77qbt.png)
3. 双击下载的 `.pkg` 文件，按照屏幕提示点击“继续”并完成安装。
![输入图片说明](/imgs/2026-04-16/OQaMHPU5Cgfc22tZ.png)
4. 点击继续，会提示软件的相关许可协议
![输入图片说明](/imgs/2026-04-16/j1HAH94hG7pyYxfT.png)
5. 再次点击继续，会弹窗提示必须同意相关协议条款才能走下一步。
![输入图片说明](/imgs/2026-04-16/9n9kI3elk1D6BJql.png)
6. 选择软件安装的目的盘
![输入图片说明](/imgs/2026-04-16/3bAbxk6NiXNLoHg9.png)
![输入图片说明](/imgs/2026-04-16/cXYSv6npTpLZgrUi.png)
7. 下一步，此时会提示让输入电脑的密码来开始安装。
![输入图片说明](/imgs/2026-04-16/ysFiPhxFkAMFYzlp.png)
8. 安装成功，关闭安装窗口即可。
![输入图片说明](/imgs/2026-04-16/fomFnjCxhSvAiOgz.png)

**方法二：使用 Homebrew（推荐开发者）**

如果已安装 Homebrew：
```bash
brew install node
```
如果未安装 Homebrew：
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install node
```
## 验证安装
打开终端，执行：
```
node --version
npm --version
```
如果显示版本号（如 v18.x.x 或更高），说明安装成功。
## Linux
 **Ubuntu/Debian 发行版：**
 
**使用 NodeSource 仓库（推荐）**
```
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install -y nodejs

# 验证安装
node --version
npm --version
```
**CentOS/RHEL 发行版：**
```bash
curl -fsSL https://rpm.nodesource.com/setup_lts.x | sudo bash -
sudo yum install -y nodejs

# 验证安装
node --version
npm --version
```

**Fedora 发行版：**

```bash
sudo dnf install -y nodejs npm

# 验证安装
node --version
npm --version
```

**Arch Linux：**

```bash
sudo pacman -S nodejs npm

# 验证安装
node --version
npm --version
```
**使用 nvm（推荐进阶用户）**
nvm 允许您管理多个 Node.js 版本：
```
# 安装 nvm
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash

# 重新加载 shell 配置
source ~/.bashrc

# 安装 Node.js LTS
nvm install --lts

# 设置默认版本
nvm use --lts
nvm alias default node
```
## 常见问题
#### Windows
**提示"不是内部或外部命令"**

-   重新打开终端窗口
-   检查 PATH 环境变量是否包含 Node.js 路径
-   重启电脑后再试

**安装失败**

-   以管理员身份运行安装程序
-   关闭杀毒软件后重试
-   检查系统盘空间是否充足

#### macOS
**Homebrew 安装慢**
可以使用国内镜像：
```
export HOMEBREW_BREW_GIT_REMOTE="https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git"
```
**权限问题**
如果遇到权限问题，不要使用 `sudo`，而是修复 Homebrew 权限：
```
sudo chown -R $(whoami) /usr/local/bin /usr/local/lib
```

#### Linux
**权限问题**
如果遇到权限问题，可以配置 npm 使用用户目录：
```
mkdir ~/.npm-global
npm config set prefix '~/.npm-global'
echo 'export PATH=~/.npm-global/bin:$PATH' >> ~/.bashrc
source ~/.bashrc
```
**版本过旧**
如果系统自带的 Node.js 版本过旧，建议使用 NodeSource 仓库或 nvm 安装最新 LTS 版本。
## 下一步
 - [Chatbox配置教程](/Chatbox%E9%85%8D%E7%BD%AE%E6%95%99%E7%A8%8B.md.md)
 - [Codex-CLI配置教程](/Codex-CLI%E9%85%8D%E7%BD%AE%E6%95%99%E7%A8%8B.md.md)
 - [Codex桌面应用配置教程](/Codex%E6%A1%8C%E9%9D%A2%E5%BA%94%E7%94%A8%E9%85%8D%E7%BD%AE%E6%95%99%E7%A8%8B.md.md)
 - [VS-Code-Codex配置教程](/VS-Code-Codex%E9%85%8D%E7%BD%AE%E6%95%99%E7%A8%8B.md.md)

