# VS Code环境安装教程

## 📋 目录
[Windows](#windows)
[macOS](#macos)
[Linux](#linux)
[验证安装](#验证安装)
[下一步](#下一步)


## Windows

### 第一步：安装 VS Code

1. 访问 [VS Code 官网](https://code.visualstudio.com/)

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/0efbb48e-2963-4be3-a967-1336659f0de7.png?raw=true)

2. 下载 Windows 版本安装包

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/f439ee24-6e05-4022-b942-72a7911d6498.png?raw=true)

3. 双击运行安装程序

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/54ef9a6f-dd96-4477-b192-17d4e3a83dce.png?raw=true)

4. 选择安装位置，默认情况下 VS Code 会安装在以下目录：
   `C:\Users\{Username}\AppData\Local\Programs\Microsoft VS Code`
   （`Username` 为你的用户名）
   - 如果没有特殊要求，建议使用默认路径
   - 点击"Next（下一步）"继续

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/2a051dbd-ca21-4bfb-b71c-342505e7e32b.png?raw=true)

5. 接下来是设置开始菜单快捷方式，建议使用默认设置
   - 点击"Next（下一步）"继续

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/c7eacc99-cc12-4f5a-afb1-a60680aef7dc.png?raw=true)

6. 接下来，可以勾选以下选项（推荐）：

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/708f2901-d3d8-4ee5-96d5-f304cf034b37.png?raw=true)

7. 点击"Install"按钮，等待安装完成后启动 VS Code。

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/aedce91d-0eff-4ea3-bb05-691114dd6a96.png?raw=true)

8. 点击"Finish"按钮完成安装：

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/c4486550-578b-4785-92a5-207d1861bc2b.png?raw=true)

### 第二步：启动 VS Code

1. 重启电脑
2. 启动 VS Code，界面如下所示：

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/63533a34-a679-4be6-88b0-b07d5ff20b95.png?raw=true)

## macOS
Mac 用户注意选择正确的芯片架构：

-   **ARM64**：M1 / M2 / M3 / M4 芯片
-   **x64**：Intel 芯
### 第一步：安装 VS Code

1. 访问 [VS Code 官网](https://code.visualstudio.com/)

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/0efbb48e-2963-4be3-a967-1336659f0de7.png?raw=true)

2. 下载 macOS 版本（文件名：`VSCode-darwin-universal.dmg`）

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/d60c57f9-1010-435c-b5ac-43db4818b429.png?raw=true)

3. 将 VS Code 拖拽到"应用程序"文件夹，使其在 macOS Launchpad（启动台）中可用。
![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/ec204ce9-dc04-495f-9903-05909585bc6c.png?raw=true)

### 第二步：启动 VS Code

**方式一：通过Spotlight搜索**
1. 按下 `Command ⌘` + `Space` 打开Spotlight搜索
2. 在搜索框中输入"Visual Studio Code"
3. 按回车键打开

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/e04dae90-ebef-4674-9d33-1cd9cf1e39df.png?raw=true)

**方式二：通过启动台**
1. 打开启动台（Launchpad）
2. 找到并单击 Visual Studio Code 图标

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/8e17bd07-ae2d-4f2e-b166-a0c9a2ac647e.png?raw=true)

### 第三步：安全提示

1. macOS 将提示是否确认打开从互联网下载的程序
- 单击"Open（打开）"按钮即可：

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/e3c8014c-d03a-4e2f-ae77-b33ecc987d60.png?raw=true)

2. 启动 Visual Studio Code，界面如下：

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/32974c08-8a13-4944-817b-5a44455d0a81.png?raw=true)

## Linux

### 基于Ubuntu和Debian的发行版：
1、安装基于Debian/Ubuntu发行版的Visual Studio Code最简单的方法是下载并安装[.deb包（64位），](https://go.microsoft.com/fwlink/?LinkID=760868)如果有图形软件中心，也可以通过命令行安装：
```
sudo apt install ./<file>.deb

# If you're on an older Linux distribution, you will need to run this instead:
# sudo dpkg -i <file>.deb
# sudo apt-get install -f # Install dependencies

```

> 注释
> 其他二进制文件也可在[VS Code下载页面](https://code.visualstudio.com/Download)获取。

安装.deb包后，系统会提示安装apt仓库和签名密钥，以启用系统包管理器自动更新。
2、要自动安装apt仓库和签名密钥，例如在非交互式终端上，首先执行以下命令：
```
echo "code code/add-microsoft-repo boolean true" | sudo debconf-set-selections

```
3、要手动安装apt仓库：

 - [ ] 运行以下脚本安装签名密钥：

 ```
sudo apt-get install wget gpg &&
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg &&
sudo install -D -o root -g root -m 644 microsoft.gpg /usr/share/keyrings/microsoft.gpg &&
rm -f microsoft.gpg

```

 - [ ] 创建一个包含以下内容的文件，以添加对上游包仓库的引用：

`/etc/apt/sources.list.d/vscode.sources`
```
Types: deb
URIs: https://packages.microsoft.com/repos/code
Suites: stable
Components: main
Architectures: amd64,arm64,armhf
Signed-By: /usr/share/keyrings/microsoft.gpg

```

 - [ ] 最后，更新包缓存并安装包

```
sudo apt install apt-transport-https &&
sudo apt update &&
sudo apt install code # or code-insiders

```

> 注释
> 
> 由于手动签名流程和我们使用的发布系统，Debian 仓库可能会延迟多达三小时，且无法立即获得最新版本的 VS Code。

### 基于RHEL、Fedora和CentOS的发行版
我们目前在一个 yum 仓库中发布了稳定的 64 位 VS Code，适用于基于 RHEL、Fedora 或 CentOS 的发行版。
1、通过运行以下脚本安装密钥和 yum 仓库：
```
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc &&
echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\nautorefresh=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" | sudo tee /etc/yum.repos.d/vscode.repo > /dev/null
```
2、然后更新包缓存，并用（Fedora 22及以上版本）安装包：`dnf`
```
dnf check-update &&
sudo dnf install code # or code-insiders
```
或者在旧版本上使用：`yum`
```
yum check-update &&
sudo yum install code # or code-insiders
```

> 注释
由于手动签名流程和我们使用的发布系统，yum repo 可能会延迟最多三小时，且无法立即获得最新版本的 VS Code。

VS Code 作为 Snap 包正式在 [Snap 商店](https://snapcraft.io/store)中分发

![输入图片说明](https://github.com/CXL123983/-/blob/main/VS-Code/cc704a49-dc1c-497d-926b-98efdbd83637.png?raw=true)

你可以通过运行以下程序来安装：
```
sudo snap install --classic code # or code-insiders
```
安装后，Snap 守护进程会自动在后台更新 VS Code。每当有新更新可用时，你会收到产品内更新通知。

> 注释
如果你的Linux发行版里没有，可以查看[安装snapd指南](https://docs.snapcraft.io/installing-snapd)，这能帮你设置`snap`

想了解更多关于_Snap的信息_，请访问[官方Snap文档](https://docs.snapcraft.io/)。
### 基于 openSUSE 和 SLE 的发行版
前面提到的 yum 仓库同样适用于 openSUSE 和基于 SLE 的系统。
1、通过运行以下脚本安装密钥和 yum 仓库：
```
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc &&
echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\nautorefresh=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" | sudo tee /etc/zypp/repos.d/vscode.repo > /dev/null
```
2、然后更新包缓存并用以下方法安装包：
```
sudo zypper install code
```
### Arch Linux 的 AUR 包
有一个由社区维护的 [VS Code Arch 用户仓库包](https://aur.archlinux.org/packages/visual-studio-code-bin)。

如需获取AUR安装的更多信息，请参阅以下维基条目：[安装AUR套件](https://wiki.archlinux.org/index.php/Arch_User_Repository)。

### NixOS 的 Nix 包（或任何使用 Nix 包管理器的 Linux 发行版）
nixpkgs 仓库中有一个由社区维护的 [VS Code Nix 包](https://github.com/NixOS/nixpkgs/blob/master/pkgs/applications/editors/vscode/vscode.nix)。
使用 Nix 安装：
1、 在你的`allowUnfree``config.nix`
2、执行以下命令：
```
nix-env -i vscode
```
### 手动安装.rpm软件包
你可以手动下载并安装[VS Code .rpm包（64位），](https://go.microsoft.com/fwlink/?LinkID=760867)但如果没有安装上述仓库，自动更新是无法实现的。
下载后，可以通过你的包管理器安装该包，例如：`.rpm``dnf`
```
sudo dnf install <file>.rpm
```

> 注释
> 其他二进制文件也可在[VS Code下载页面](https://code.visualstudio.com/Download)获取。
### 更新
VS Code每周发售，你可以通过查看[发布说明](https://code.visualstudio.com/updates)来查看新版本。如果VS Code仓库安装正确，那么你的系统包管理器应该像系统上其他包一样处理自动更新。
> ==注释== 
[Snap 包](https://code.visualstudio.com/docs/setup/linux#_snap)的更新是自动的，并在后台运行

## 验证安装

打开 VS Code 的终端：

- **Windows/Linux**：按 `Ctrl + `` ``
- **macOS**：按 `Cmd + `` ``

执行以下命令查看版本：

```bash
code --version
```
## 常见问题
### 1. 安装失败？
-   Windows：关闭杀毒软件/防火墙，以管理员身份运行安装程序。
-   所有系统：检查网络连接，确保下载包完整。

### 2. 无法打开终端？
-   Windows：安装时勾选 Add to PATH。
-   macOS/Linux：按 `Ctrl+Shift+` (`~`) 调出集成终端。
## 下一步
 - [VS-Code-Codex配置教程](https://github.com/CXL123983/-/blob/main/VS-Code-Codex%E6%8F%92%E4%BB%B6%E9%85%8D%E7%BD%AE%E6%95%99%E7%A8%8B%20.md)
