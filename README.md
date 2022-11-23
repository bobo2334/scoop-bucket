# 我的 Scoop Bucket

[![Excavator](https://github.com/bobo2334/scoop-bucket/actions/workflows/schedule.yml/badge.svg)](https://github.com/bobo2334/scoop-bucket/actions/workflows/schedule.yml)

## 这是啥

这是一个 [Scoop](https://github.com/lukesampson/scoop) 的 Bucket，主要用来存放一些我需要的但是不在 Scoop 官方仓库里存在的软件安装脚本。

## Scoop 是啥

Scoop 是一个在 Windows 系统中运行的包管理器，可以通过命令行对你常用的软件进行管理操作，如搜索、安装、更新和卸载等。

Scoop 的优点是方便、灵活度高。安装的软件大多都是绿色版，不污染系统注册表。Scoop 还会对已安装的软件统一管理，如可执行文件统一注册在 PATH 变量中，统一创建快捷方式，对软件的持久化数据统一存储。

总之，Scoop 是一款优雅的 Windows 包管理器。

## 怎么用

通过下面的命令来添加这个 Bucket。

```bash
scoop bucket add bobo2334 https://github.com/bobo2334/scoop-bucket.git
```

## 维护命令

### 更新软件

```bash
# 更新全部软件
pwsh .\bin\checkver.ps1 -a * -u

# 更新某个软件
pwsh .\bin\checkver.ps1 -a apk-info -u
```

### 格式化 JSON 文件

```bash
pwsh .\bin\formatjson.ps1
```

### 检查下载链接

```bash
pwsh .\bin\checkurls.ps1
```

### 检查文件 Hash 是否匹配

```bash
pwsh .\bin\checkhashes.ps1
```

## checkver.ps1 的参数说明

- `App` (`-a APP`)
    Manifest name to search.
    Placeholders (*) are supported.
- `Dir` (`-d DIR`)
    Where to search for manifest(s).
- `Update` (`-u`)
    Update given manifest.
- `ForceUpdate` (`-f`)
    Check manifest(s) and update, even if there is no new version.
- `SkipUpdated` (`-s`)
    Check given manifest(s), and list only outdated manifest(s).
- `Version` (`-v VER`)
    Check given manifest(s) using a given version VER.
    Usually used with -u to update to a certain version.

## 致谢

从这些仓库中抄了一些作业，非常感谢。

- [lukesampson/scoop: A command-line installer for Windows.](https://github.com/lukesampson/scoop)
- [ScoopInstaller/Extras: 📦 The Extras bucket for Scoop.](https://github.com/ScoopInstaller/Extras)
- [chawyehsu/dorado: 🐟 Yet Another bucket for lovely Scoop](https://github.com/chawyehsu/dorado)
