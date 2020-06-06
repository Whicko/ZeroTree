# Homebrew

> macOS（或 Linux）缺失的软件包的管理器. [Homebrew官网](https://brew.sh/index_zh-cn)

`homebrew` 使安装管理软件变得干净方便.

默认情况下使用 `homebrew` 安装的软件会统一安装在 `/usr/local/Cellar` 目录下.  
并且会在 `/usr/local` 中自动创建软连接.

## 安装

* 简单的一键安装

```text
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

* 如果想要在安装时设置高级参数, 可以在官网查询

### 关于 `Homebrew cask` 的安装

在最新的 `Homebrew` 中已经集成了 `Homebrew Cask`, 可以直接使用, 如果 `Homebrew` 检测到没有安装, 则会自动安装 `Homebrew Cask`

## 常用命令

### 显示信息

* 显示所有安装软件的统计信息。

```text
$ brew info
```

* 显示指定已安装的软件信息

```text
$ brew info [package]
```

### 显示包依赖

```text
$ brew deps
```

### 查看已安装软件列表

```text
$ brew list [ | --versions ]
```

### 搜索软件

```text
$ brew search [name]
```

使用搜索命令可以同时搜索 `Homebrew` 和 `Homebrew Cask` 中的软件, 搜索名称同时支持文本和正则.

### 安装软件

```text
$ brew install [package]
```

### 卸载软件

```text
$ brew uninstall [package]
```

### 更新软件

* 查看你的软件中哪些有新版本可用

```text
$ brew outdated
```

* 更新指定软件

```text
$ brew upgrade [package]
```

* 从服务器上拉取，并更新本地 brew 的包目录

```text
$ brew update
```

* 清理老版本。使用 `-n` 参数，不会真正执行，只是打印出真正运行时会做什么。

```text
$ brew cleanup
```

### 创建软连接

* 将软件的当前最新版本软链到`/usr/local`目

```text
$ brew link <package_name>
```

* 将软件在`/usr/local`目录下的软链接删除

```text
$ brew unlink <package_name>
```

## Homebrew cask

### 安装软件

```text
$ brew cask install [package]
```

### 列出已安装软件

```text
$ brew cask list
```

### Homebrew cask 安装的软件更新

使用 [homebrew cask upgrade](https://github.com/buo/homebrew-cask-upgrade) 进行软件更新

* 安装 `homebrew cask upgrade`

```text
brew tap buo/cask-upgrade
```

* 更新软件

```text
brew cu
```

