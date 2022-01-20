# sample

A project to demonstrate the use of quickapp, including demos of components and apis. https://www.quickapp.cn/

## 分支说明

master 分支：最新内容，需在快应用平台最新版本上使用。

版本分支：例如 v1000 分支内容需在快应用平台 v1000+版本上使用。

## 使用方法说明

### 配置快应用开发环境

#### 安装 Node.jS

需安装 6.0 以上版本的 Node.jS，请从[Node.js 官网](https://nodejs.org/en/)下载

#### 安装 hap-toolkit

通过 npm 仓库安装，在命令行中执行以下命令：

> npm install -g hap-toolkit

在命令行中执行 hap -V 会输出版本信息表示 hap-toolkit 安装成功，如下命令所示：

> hap -V

#### 手机安装调试器

调试器是一个 Android 应用程序，下载[调试器 APK](https://statres.quickapp.cn/quickapp/quickapp/201806/file/quickapp_debugger.apk)

在手机上安装并打开调试器，按钮功能如下：

- 扫码安装：配置 HTTP 服务器地址，下载 rpk 包，并唤起平台运行 rpk 包
- 本地安装：选择手机文件系统中的 rpk 包，并唤起平台运行 rpk 包
- 在线更新：重新发送 HTTP 请求，更新 rpk 包，并唤起平台运行 rpk 包
- 开始调试：唤起平台运行 rpk 包，并启动远程调试

**注意**：若打开调试器无法点击按钮，请升级手机系统到最新版本或安装平台预览版

安装成功后如下图所示：

![](https://doc.quickapp.cn/tutorial/getting-started/build-environment.png)

### 运行项目

#### 安装依赖

在项目根目录下，运行如下命令安装模块到 node_modules 目录

> npm install

#### 编译

1、手动编译项目

在项目的根目录下，运行如下命令进行编译打包，生成 rpk 包

> npm run build

编译打包成功后，项目根目录下会生成文件夹：**build、dist**

- build：临时产出，包含编译后的页面 js，图片等
- dist：最终产出，包含 rpk 文件。其实是将 build 目录下的资源打包压缩为一个文件，后缀名为 rpk，这个 rpk 文件就是项目编译后的最终产出

2、自动编译项目

如果希望每次修改源代码文件后，都自动编译项目，请使用如下命令：

> npm run watch

#### 安装 rpk 包

编译项目产出了 rpk 包后，请打开手机调试器。

若打开调试器无法点击按钮，请升级手机系统到最新版本或安装平台预览版。

调试器可使用后，就可以在调试器上安装 rpk 包了。支持以下两种安装方式，开发者可根据场景选择其一

##### 扫码安装

1、启动 HTTP 服务器

在终端中新建一个窗口，进入项目的根目录运行如下命令，启动本地服务器（默认端口为 12306）

> npm run server

自定义端口（如：8080）

> npm run server -- --port 8080

2、在手机上预览运行效果
配置 HTTP 服务器地址有两种方式，以下两者选其一即可：

- 打开调试器 --> 点击"扫码安装"，扫描终端窗口中的二维码即可完成配置（若扫描不成功，可在浏览器中打开页面：http://localhost:<your port>，扫描页面中的二维码）
- 打开调试器 --> 点击右上角 menu --> 设置，输入终端窗口中提示的 HTTP 服务器地址

配置完成后，可点击在线更新唤起平台运行 rpk 包

若提示安装失败，请检查执行 npm run server 的终端窗口是否正常运行

##### 本地安装

1、复制 rpk 包到手机中

将<ProjectName>/dist 目录下编译产出的 rpk 包通过 USB 数据线或其他方式，复制到手机文件系统中

2、本地安装 rpk 包

打开调试器 --> 点击"本地安装"，选择手机文件系统中的 rpk 包，并自动唤起平台运行 rpk 包，查看效果

#### 预览效果

安装成功后，效果如下：

![](http://statres.quickapp.cn/quickapp/quickapp/201809/file/index-snapshot.png)
