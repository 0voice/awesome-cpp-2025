# C++ 环境搭建指南
以下是 **Windows、Mac、Linux 三大系统的 C++ 环境搭建详细指南**，包含编译器（GCC/Clang/MSVC）、IDE（VS Code 为主，兼顾 Xcode/Qt Creator）、工具链（Git/CMake）的完整流程，适合零基础入门，步骤清晰且附问题排查
## 核心说明
C++ 环境核心依赖 **编译器**（将代码转为可执行文件）+ **IDE/编辑器**（写代码）+ 可选工具（Git/CMake 用于项目管理）。本文优先推荐 **VS Code + GCC/Clang**（跨平台、轻量、通用），同时提供各系统专属方案。


## 一、Windows 系统（最常用）
### 方案 1：VS Code + MinGW-w64（推荐，免费跨平台）
#### 步骤 1：安装 MinGW-w64（编译器）
1. 下载安装包：  
   官网：https://sourceforge.net/projects/mingw-w64/files/  
   快速链接：直接下载 `mingw-w64-install.exe`（32/64 位通用）。
2. 安装配置：  
   - 安装路径建议默认（如 `C:\Program Files\MinGW-w64\mingw64`），避免中文路径；  
   - 架构选择 `x86_64`（64 位系统），线程选 `posix`，异常处理选 `seh`（兼容性更好）；  
   - 安装完成后，**配置环境变量**：  
     右键「此电脑」→ 属性 → 高级系统设置 → 环境变量 → 系统变量 → 找到 `Path` → 新增 MinGW-w64 的 `bin` 路径（如 `C:\Program Files\MinGW-w64\mingw64\bin`）。
3. 验证编译器：  
   打开 CMD 或 PowerShell，输入 `g++ --version`，若显示版本号（如 `g++ (x86_64-posix-seh-rev0, Built by MinGW-W64 project) 13.2.0`），则安装成功。

#### 步骤 2：安装 VS Code（编辑器）
1. 下载：https://code.visualstudio.com/（默认安装，勾选“添加到 PATH”）。
2. 安装 C++ 插件：  
   打开 VS Code → 左侧扩展栏 → 搜索安装以下插件：  
   - C/C++（微软官方，核心插件）；  
   - C/C++ Extension Pack（插件集合，含调试、格式化工具）；  
   - Code Runner（一键运行代码，可选）。

#### 步骤 3：测试第一个 C++ 程序
1. 新建文件夹（如 `C++_HelloWorld`），用 VS Code 打开；  
2. 新建文件 `main.cpp`，写入代码：
   ```cpp
   #include <iostream>
   int main() {
       std::cout << "Hello, C++!" << std::endl;
       return 0;
   }
   ```
3. 运行代码：  
   - 方法 1：用 Code Runner 插件（右上角三角形图标），直接运行；  
   - 方法 2：手动编译运行：  
     打开终端（VS Code 内置终端，Ctrl+`），输入 `g++ main.cpp -o main.exe`，编译生成 `main.exe`，再输入 `./main.exe` 执行，输出 `Hello, C++!` 则成功。

### 方案 2：Visual Studio（MSVC 编译器，适合 Windows 开发）
若需开发 Windows 专属程序（如 Win32 应用），可安装 Visual Studio 2022：
1. 下载：https://visualstudio.microsoft.com/zh-hans/vs/  
2. 安装时勾选「使用 C++ 的桌面开发」（默认包含 MSVC 编译器、调试工具）；  
3. 新建项目：选择「控制台应用」→ 命名项目 → 自动生成模板代码，直接运行（Ctrl+F5）即可。


## 二、Mac 系统
### 方案 1：VS Code + Clang（推荐，原生编译器）
#### 步骤 1：安装 Clang（编译器，Mac 自带，需激活）
1. 打开「终端」（Terminal），输入 `xcode-select --install`；  
2. 弹出提示框，点击「安装」，等待 Command Line Tools 下载完成（包含 Clang 编译器）；  
3. 验证：终端输入 `clang --version`，显示版本号则成功。

#### 步骤 2：安装 VS Code 及插件
1. 下载 VS Code：https://code.visualstudio.com/（Mac 版 `.dmg` 安装包）；  
2. 安装插件：同 Windows 方案 1（C/C++、C/C++ Extension Pack、Code Runner）。

#### 步骤 3：测试程序
1. 新建 `main.cpp`，写入 Hello World 代码；  
2. 终端编译：`clang++ main.cpp -o main`，执行：`./main`，输出结果即成功。

### 方案 2：Xcode（苹果官方 IDE，适合 macOS/iOS 开发）
1. 下载：在 App Store 搜索「Xcode」（免费），安装完成后打开；  
2. 新建项目：选择「Command Line Tool」→ 语言选「C++」→ 命名项目；  
3. 自动生成 `main.cpp`，点击左上角运行按钮（▶️），即可编译运行。


## 三、Linux 系统（Ubuntu/Debian 为例）
### 方案：VS Code + GCC（原生支持，无需复杂配置）
#### 步骤 1：安装 GCC 编译器
1. 打开终端，更新软件源：`sudo apt update`；  
2. 安装 GCC 和 G++：`sudo apt install gcc g++`；  
3. 验证：`g++ --version`，显示版本号则成功。

#### 步骤 2：安装 VS Code
1. 下载：https://code.visualstudio.com/，选择 Linux 版（`.deb` 或 `.rpm`）；  
2. 安装：终端进入下载目录，执行 `sudo dpkg -i code_xxx.deb`（xxx 为版本号）；  
3. 安装插件：同 Windows/Mac 方案（C/C++、C/C++ Extension Pack）。

#### 步骤 3：测试程序
1. 新建 `main.cpp`，写入代码；  
2. 终端编译：`g++ main.cpp -o main`，执行：`./main`，输出结果即成功。


## 四、可选工具安装（Git + CMake，项目开发必备）
### 1. Git（版本控制工具）
- Windows：下载 https://git-scm.com/，默认安装（勾选“添加到 PATH”）；  
- Mac：终端输入 `brew install git`（需先安装 Homebrew：`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`）；  
- Linux：`sudo apt install git`；  
- 验证：`git --version`。

### 2. CMake（跨平台项目构建工具）
- Windows：下载 https://cmake.org/download/，安装时勾选“Add CMake to system PATH”；  
- Mac：`brew install cmake`；  
- Linux：`sudo apt install cmake`；  
- 验证：`cmake --version`。


## 五、常见问题排查
1. **“g++/clang: 不是内部或外部命令”**：  
   原因：编译器未配置环境变量。解决方案：重新检查 MinGW-w64 的 `bin` 路径是否添加到系统 `Path`，重启终端/VS Code 重试。

2. **VS Code 运行代码无输出**：  
   原因：插件未正确配置。解决方案：打开 `main.cpp` → 按 `Ctrl+Shift+P` → 输入 `C/C++: Edit Configurations (UI)` → 编译器路径选择安装的 `g++` 或 `clang++` 路径。

3. **Mac 安装 Clang 提示“无法连接服务器”**：  
   原因：网络问题。解决方案：切换网络，或手动下载 Command Line Tools（https://developer.apple.com/download/all/，需苹果账号）。

4. **Linux 安装 VS Code 提示“依赖缺失”**：  
   解决方案：执行 `sudo apt -f install`，自动修复依赖后重新安装。


## 总结
- 零基础/跨平台开发：优先选 **VS Code + GCC/Clang**（Windows 用 MinGW-w64，Mac/Linux 原生支持）；  
- Windows 桌面开发：选 **Visual Studio 2022**（MSVC 编译器，对 Windows API 支持更好）；  
- Mac/iOS 开发：选 **Xcode**（苹果官方生态，无缝适配）。

搭建完成后，可直接开始学习基础语法（变量、循环、函数等），后续通过 Git 管理代码、CMake 构建多文件项目，逐步过渡到实战开发
