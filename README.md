# 我的 Scoop Bucket

[![Excavator](https://github.com/bobo2334/scoop-bucket/actions/workflows/schedule.yml/badge.svg)](https://github.com/bobo2334/scoop-bucket/actions/workflows/schedule.yml)

## 这是啥

这是一个 [Scoop](https://github.com/lukesampson/scoop) 的 Bucket，主要用来存放一些我需要的但是不在 Scoop 官方仓库里存在的软件安装脚本。

## Scoop 是啥

Scoop 是一个在 Windows 系统中运行的包管理器，可以通过命令行对你常用的软件进行管理操作，如搜索、安装、更新和卸载等。

Scoop 的优点是方便、灵活度高。安装的软件大多都是绿色版，不污染系统注册表。Scoop 还会对已安装的软件统一管理，如可执行文件统一注册在 PATH 变量中，统一创建快捷方式，对软件的持久化数据统一存储。

总之，Scoop 是一款优雅的运行在 Windows 中的包管理器。

## 怎么用

```bash
scoop bucket add bobo2334 https://github.com/bobo2334/scoop-bucket.git
```

## manifest 自动更新

```bash
npm run checkver
```

```bash
.\bin\checkver -a * -d .\bucket -u
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
- [chawyehsu/dorado: 🐟 Yet Another bucket for lovely Scoop](https://github.com/chawyehsu/dorado)
