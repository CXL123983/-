
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

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/ade98490-b8ae-4962-a488-b0316d0089b1.png?raw=true)
3. 双击下载后的安装包，如下所示：

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/587f4716-a332-456a-8f61-95db17e2bcb0.png?raw=true)
5. 点击以上的 Next 按钮，将出现如下界面：

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/137e5186-5c9c-4afe-993e-59c8cc39f5fc.png?raw=true)
7. 勾选接受协议选项，点击 Next 按钮 :

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/bc83db3c-c6ed-4ffe-aecd-161eb411e226.png?raw=true)
9. Node.js默认安装目录为 "C:\Program Files\nodejs\" , 你可以修改目录，并点击 Next 按钮：

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/7dee750b-9825-43da-a546-764fc9a6249a.png?raw=true)
11. 点击 Install（安装） 开始安装 Node.js，你也可以点击 Back（返回）来修改先前的配置：

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/b01de2e8-dd4f-4b00-b415-ad13bd47dc91.png?raw=true)
安装过程：

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/d13e63fe-05c7-4552-b9b2-778c12f9958a.png?raw=true)
点击 Finish（完成）按钮退出安装向导。

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/6a509d04-b21d-4b37-893d-9b46e51b050a.png?raw=true)

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

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/944e285b-56ff-4699-afad-a58f40b6b127.png?raw=true)
2. 下载 LTS 版本的 .pkg 安装包

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/944e285b-56ff-4699-afad-a58f40b6b127.png?raw=true)
3. 双击下载的 `.pkg` 文件，按照屏幕提示点击“继续”并完成安装。

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/2e4b7a50-2ae3-408b-a199-cbd1076aca7d.png?raw=true)
4. 点击继续，会提示软件的相关许可协议

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/6bdca4d8-228d-47af-9945-c92765d99545.png?raw=true)
5. 再次点击继续，会弹窗提示必须同意相关协议条款才能走下一步。

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/00ea049b-a092-4359-b0bb-1693a83477b7.png?raw=true)
6. 选择软件安装的目的盘

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/c690409d-2cde-4ec5-a8de-5def7c0f2f23.png?raw=true)
![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/5d7276ad-c7f2-43ab-b091-5c507c3635f6.png?raw=true)
7. 下一步，此时会提示让输入电脑的密码来开始安装。

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/223b711b-e384-4017-90e5-c7d5d3d3ab67.png?raw=true)
8. 安装成功，关闭安装窗口即可。

![输入图片说明](https://github.com/CXL123983/-/blob/main/Node.js/58ac0c91-3373-426b-a996-5ef7dbe75ce2.png?raw=true)

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

