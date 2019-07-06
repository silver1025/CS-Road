# Go 安装

> 参考地址：<https://go-zh.org/doc/install>

## 安装Go工具

### Windows

对于Windows用户，Go项目提供两种安装选项（[从源码安装](https://go-zh.org/doc/install/source)除外）： zip压缩包需要你设置一些环境变量，而实验性MSI安装程序则会自动配置你的安装。

##### MSI安装程序

打开此[MSI文件](http://code.google.com/p/go/downloads/list?q=OpSys-Windows+Type%3DInstaller) 并跟随提示来安装Go工具。默认情况下，该安装程序会将Go发行版放到 `c:\Go` 中。

此安装程序应该会将 `c:\Go\bin` 目录放到你的 `PATH` 环境变量中。 要使此更改生效，你需要重启所有打开的命令行。

##### Zip压缩包

[下载此zip文件](http://code.google.com/p/go/downloads/list?q=OpSys-Windows+Type%3DArchive) 并提取到你的自选目录（我们的建议是`c:\Go`）：

若你选择了 `c:\Go` 之外的目录，你必须为你所选的路径设置 `GOROOT` 环境变量。

将你的Go根目录中的 `bin` 子目录（例如 `c:\Go\bin`）添加到你的 `PATH` 环境变量中。

##### 在Windows下设置环境变量

在Windows下，你可以通过在系统“控制面板”中，“高级”标签上的“环境变量”按钮来设置环境变量。 Windows的一些版本通过系统“控制面板”中的“高级系统设置”选项提供此控制板。

### Mac OS X安装包

打开此[包文件](http://code.google.com/p/go/downloads/list?q=OpSys-Darwin+AND+Type-Installer) 并跟随提示来安装Go工具。该包会将Go发行版安装到 `/usr/local/go` 中。

此包应该会将 `/usr/local/go/bin` 目录放到你的 `PATH` 环境变量中。 要使此更改生效，你需要重启所有打开的终端回话。

手动配置环境变量：要将 `/usr/local/go/bin` 添加到 `PATH` 环境变量， 你需要将此行添加到你的 `/etc/profile`（全系统安装）或 `$HOME/.profile` 文件中：

```
export PATH=$PATH:/usr/local/go/bin
```

## 卸载 Go

要从你的系统中移除既有的Go安装，需删除 `go` 目录。 在 Linux、Mac OS X、和 FreeBSD 系统下通常为 `/usr/local/go`， 在 Windows 下则为 `c:\Go`。

你也应当从你的 `PATH` 环境变量中移除 Go 的 `bin` 目录。 在 Linux 和 FreeBSD 下你应当编辑 `/etc/profile` 或 `$HOME/.profile`。 若你是通过[Mac OS X 包](https://go-zh.org/doc/install#osx)安装的 Go，那么你应当移除 `/etc/paths.d/go` 文件。 Windows 用户请阅读[在 Windows 下设置环境变量](https://go-zh.org/doc/install#%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F)一节。

---

export goproxy=https://goproxy.io

$env:GOPROXY = "https://goproxy.io"

在调试之前需要先执行下面的命令，安装go程序调试包。

go get [github.com/derekparker/delve/cmd/dlv](http://github.com/derekparker/delve/cmd/dlv)