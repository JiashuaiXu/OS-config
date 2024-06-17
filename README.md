# OS-config
用于存放个人的系统配置文件

# 如何使用

了解了你的仓库新名字后，这里是更新后的命令，以适应你新的仓库名称：

### 创建主仓库

```bash
# 创建主仓库
git init OS-config

# 进入主仓库目录
cd OS-config
```

### 添加子模块

```bash
# 克隆主仓库
git clone https://github.com/JiashuaiXu/OS-config.git
cd OS-config

# 添加子模块
git submodule add https://github.com/JiashuaiXu/Windows-config.git windows
git submodule add https://github.com/JiashuaiXu/MacOS-config.git macos
git submodule add https://github.com/JiashuaiXu/Gentoo-config.git gentoo
git submodule add https://github.com/JiashuaiXu/NixOS-config.git nixos
git submodule add https://github.com/JiashuaiXu/Arch-config.git archlinux
```

### 同步子模块

```bash
# 更新所有子模块
git submodule update --remote --merge
```

### 在不同系统中使用配置文件

你可以在每个系统中克隆主仓库，然后根据需要同步相应的子模块。例如，在 Windows 中同步 Windows 配置文件：

```bash
# 克隆主仓库
git clone https://github.com/JiashuaiXu/OS-config.git
cd OS-config

# 初始化并更新子模块
git submodule init
git submodule update --remote --merge windows
```

### 保持子模块最新

定期更新子模块以保持所有配置文件的最新状态。

```bash
# 更新某个子模块
cd windows
git pull origin main
```

### 完整步骤总结

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
