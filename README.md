# OS-config
用于存放个人的系统配置文件

# 如何使用


1. 创建主仓库 `OS-config` 并进入目录。

```bash
git init OS-config
cd OS-config
```

2. 添加子模块。

```bash
git submodule add https://github.com/JiashuaiXu/Windows-config.git windows
git submodule add https://github.com/JiashuaiXu/MacOS-config.git macos
git submodule add https://github.com/JiashuaiXu/Gentoo-config.git gentoo
git submodule add https://github.com/JiashuaiXu/NixOS-config.git nixos
git submodule add https://github.com/JiashuaiXu/Arch-config.git archlinux
```

3. 同步子模块。

```bash
git submodule update --remote --merge
```

4. 在不同系统中使用配置文件。

```bash
git clone https://github.com/JiashuaiXu/OS-config.git
cd OS-config
git submodule init
git submodule update --remote --merge windows
```

5. 保持子模块最新。

```bash
cd windows
git pull origin main
```

这样，你可以在不同操作系统中轻松地同步和管理配置文件，既保持了配置文件的独立性，又能通过主仓库进行统一管理。
