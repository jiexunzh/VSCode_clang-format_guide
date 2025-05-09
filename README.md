# VSCode_clang-format_guide
在VSCode中安装和使用clang-format格式化C/C++代码

### 1. 安装C/C++插件

在VSCode扩展中搜索 `C/C++` ，安装C/C++插件。最新的C/C++插件里集成了 clang-format，所以不用再下载clang-format插件。

### 2. 配置C/C++插件

在VSCode `设置` 中，依次点击：`拓展` -> `C/C++` -> `格式设置`。

#### 2.1 C_Cpp: Clang_format_path

`clang-format.exe` 的绝对路径。在 `C_Cpp:Clang_format_path` 中填入 `clang-format.exe` 的绝对路径。 `clang-format.exe` 一般在安装C/C++插件时就已经附带了，路径为：`C:\Users\$用户名\.vscode\extensions\ms-vscode.cpptools-1.25.3-win32-x64\LLVM\bin\clang-format.exe`。

如果上面路径不存在，也可以使用本项目提供的 `clang-format.exe` 。

#### 2.2 C_Cpp: Clang_format_style

`.clang-format` 文件的绝对路径。在 `C_Cpp: Clang_format_style` 中填入 `.clang-format` 的绝对路径 ，对所有工程都有效，比如：`file:C:\Users\$用户名\.vscode\extensions\ms-vscode.cpptools-1.25.3-win32-x64\LLVM\bin\.clang-format`。

如果希望只对当前的工程生效，可以将 `.clang-format` 添加到当前的工作目录中，但对于使用VSCode插件的Keil项目，配置文件放在工作目录中**无法生效**。

#### 2.3 C_Cpp: Formatting

选择 `clang-format`，设置 clang-format 为C/C++代码的格式化引擎。

#### 2.4 C_Cpp: Clang_format_fallback Style（可选）

当设置了clang-format且没有.clang-format文件时，会使用这里选择的默认设置来设置格式，比如：`LLVM`。

### 3. .clang-format 样例

本人个人项目中所使用的编码风格，主要源于《华为技术有限公司C语言编程规范》。



