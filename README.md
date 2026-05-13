# OpenClaw Portable Build

自动从 [openclaw/openclaw](https://github.com/openclaw/openclaw) 上游 release 构建便携版安装包。

## 工作原理

1. **每 2 小时**自动检查上游 release
2. 发现新版本后自动构建 Windows / Linux 便携版
3. 构建产物自动发布到 [Releases](https://github.com/hllshiro/openclaw-portable/releases)
4. 也支持手动触发，指定任意上游 tag

## 下载

前往 [Releases](https://github.com/hllshiro/openclaw-portable/releases) 页面下载最新版本。

---

## 使用说明

### Windows

1. 下载 `openclaw-portable-win-x64-v*.zip`
2. 解压到任意目录
3. 打开命令提示符，进入解压目录

```cmd
# 首次设置（交互式向导）
openclaw.bat onboard --install-daemon

# 启动网关
scripts\gateway.bat
```

### Linux

1. 下载 `openclaw-portable-linux-x64-v*.tar.gz`
2. 解压并进入目录

```bash
tar -xzf openclaw-portable-linux-x64-v*.tar.gz
cd openclaw-portable-linux

# 首次设置
./openclaw.sh onboard --install-daemon

# 启动网关
./scripts/gateway.sh
```

### 更多用法

请参考 OpenClaw 官方文档：https://docs.openclaw.ai/start/getting-started

---

## 便携版特点

- 无需安装 Node.js / Python / Docker
- 内含 Node.js 运行时 + 预编译原生模块
- 解压即用

## 致谢

本项目不修改 OpenClaw 源码，仅提供构建打包服务。OpenClaw 由 [openclaw/openclaw](https://github.com/openclaw/openclaw) 团队开发。
