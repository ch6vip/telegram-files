<p align="center">
    <img src="./web/public/favicon.svg" align="center" width="30%">
</p>
<p align="center"><h1 align="center">Telegram Files</h1></p>
<p align="center">
	<em><code>一个自托管的 Telegram 文件下载器，用于连续、稳定和无人值守的下载。</code></em>
</p>
<p align="center">
	<img src="https://img.shields.io/github/license/jarvis2f/telegram-files?style=default&logo=opensourceinitiative&logoColor=white&color=0080ff" alt="license">
	<img src="https://img.shields.io/github/last-commit/jarvis2f/telegram-files?style=default&logo=git&logoColor=white&color=0080ff" alt="last-commit">
	<img src="https://img.shields.io/github/v/release/jarvis2f/telegram-files?style=default&logo=git&logoColor=white&color=0080ff" alt="release">
    <a href="https://codecov.io/gh/jarvis2f/telegram-files" > 
        <img src="https://codecov.io/gh/jarvis2f/telegram-files/graph/badge.svg?token=Y4YN2W8ARV"/> 
    </a>
</p>
<br>

## 🔗 目录

- [📍 概述](#-概述)
- [🧩 截图](#-截图)
- [🚀 开始使用](#-开始使用)
- [⌨️ 开发](#️-开发)
    - [☑️ 先决条件](#-先决条件)
    - [⚙️ 安装](#-安装)
- [📌 项目路线图](#-项目路线图)
- [🔰 贡献](#-贡献)
- [🎗 许可证](#-许可证)
- [🆗 常见问题](#-常见问题)

---

## 📍 概述

*   无缝下载 Telegram 频道和群组中的文件
*   支持多个 Telegram 帐户同时管理和下载文件
*   随时暂停和恢复下载，并自动将文件传输到指定目的地
*   即时预览下载的视频和图像
*   完全响应式设计，支持移动设备访问、渐进式 Web 应用 (PWA) 和离线功能
*   轻松从 Telegram 共享链接中获取文件

---

## 🧩 截图

<div align="center">
    <img src="./misc/preview-files-pc.gif" width="70%">
    <img src="./misc/preview-files-mobile.gif" width="17.6%">
</div>

<details closed>
<summary>更多截图</summary>
<div align="center">
    <img src="./misc/screenshot-3.png" align="center" style="width: 300px; height: 500px;">
    <img src="./misc/screenshot-4.png" align="center" style="width: 300px; height: 500px;">
</div>

<div align="center">
    <img src="./misc/screenshot.png" align="center" width="40%">
    <img src="./misc/screenshot-2.png" align="center" width="40%">
</div>
</details>

## 🚀 开始使用

在开始使用 telegram-files 之前，您应该申请一个 telegram api id 和 hash。您可以在 [Telegram API](https://my.telegram.org/apps) 页面上申请。

**使用 `docker`**
&nbsp; [<img align="center" src="https://img.shields.io/badge/Docker-2CA5E0.svg?style={badge_style}&logo=docker&logoColor=white" />](https://www.docker.com/)

```shell
docker run -d \
  --name telegram-files \
  --restart always \
  -e APP_ENV=${APP_ENV:-prod} \
  -e APP_ROOT=${APP_ROOT:-/app/data} \
  -e TELEGRAM_API_ID=${TELEGRAM_API_ID} \
  -e TELEGRAM_API_HASH=${TELEGRAM_API_HASH} \
  -p 6543:80 \
  -v ./data:/app/data \
  ghcr.io/jarvis2f/telegram-files:latest
```

**使用 `docker-compose`**

将 [docker-compose.yaml](docker-compose.yaml) 和 [.env.example](.env.example) 复制到您的项目目录中，然后运行以下命令：

```sh
docker-compose up -d
```

**在 unRaid 上安装**

在 unRaid 上，通过搜索 `telegram-files` 从社区存储库中安装。

> **重要提示：** 您不应将该服务暴露于公共互联网。因为该服务不安全。

---

## ⌨️ 开发

### ☑️ 先决条件

在开始使用 telegram-files 之前，请确保您的运行时环境满足以下要求：

- **编程语言：** JDK21,TypeScript
- **包管理器：** Gradle,Npm
- **容器运行时：** Docker

### ⚙️ 安装

使用以下方法之一安装 telegram-files：

**从源代码构建：**

1.  克隆 telegram-files 存储库：

```sh
git clone https://github.com/jarvis2f/telegram-files
```

2.  导航到项目目录：

```sh
cd telegram-files
```

3.  安装项目依赖项：

**使用 `npm`**
&nbsp; [<img align="center" src="https://img.shields.io/badge/npm-CB3837.svg?style={badge_style}&logo=npm&logoColor=white" />](https://www.npmjs.com/)

```sh
cd web
npm install
```

**使用 `gradle`**
&nbsp; [<img align="center" src="https://img.shields.io/badge/Gradle-02303A.svg?style={badge_style}&logo=gradle&logoColor=white" />](https://gradle.org/)

```sh
cd api
gradle build
```

**使用 `docker`**
&nbsp; [<img align="center" src="https://img.shields.io/badge/Docker-2CA5E0.svg?style={badge_style}&logo=docker&logoColor=white" />](https://www.docker.com/)

```sh
docker build -t jarvis2f/telegram-files .
```

## 📌 项目路线图

- ✅ **`任务 1`**: 根据设定的规则自动下载文件。
- ✅ **`任务 2`**: 下载统计和报告。
- ✅ **`任务 3`**: 改进 Telegram 的登录功能。
- ✅ **`任务 4`**: 支持自动将文件传输到其他目的地。
- ✅ **`任务 5`**: 使用虚拟列表优化文件表。
- ✅ **`任务 6`**: 预加载文件信息以支持响应式搜索。

---

## 🔰 贡献

- **💬 [加入讨论](https://github.com/jarvis2f/telegram-files/discussions)**: 分享您的见解、提供反馈或提问。
- **🐛 [报告问题](https://github.com/jarvis2f/telegram-files/issues)**: 提交发现的错误或为 `telegram-files` 项目记录功能请求。
- **💡 [提交拉取请求](https://github.com/jarvis2f/telegram-files/blob/main/CONTRIBUTING.md)**: 查看开放的 PR，并提交您自己的 PR。

<details closed>
<summary>贡献指南</summary>

1.  **Fork 存储库**: 首先将项目存储库 fork 到您的 github 帐户。
2.  **本地克隆**: 使用 git 客户端将 fork 的存储库克隆到您的本地计算机。
    ```sh
    git clone https://github.com/jarvis2f/telegram-files
    ```
3.  **创建新分支**: 始终在具有描述性名称的新分支上工作。
    ```sh
    git checkout -b new-feature-x
    ```
4.  **进行更改**: 在本地开发和测试您的更改。
5.  **提交更改**: 使用清晰的消息提交，描述您的更新。
    ```sh
    git commit -m '实现了新功能 x。'
    ```
6.  **推送到 github**: 将更改推送到您的 fork 存储库。
    ```sh
    git push origin new-feature-x
    ```
7.  **提交拉取请求**: 针对原始项目存储库创建 PR。清楚地描述更改及其动机。
8.  **审查**: 一旦您的 PR 被审查和批准，它将被合并到主分支中。恭喜您的贡献！

</details>

---

## 🎗 许可证

该项目受 MIT 许可证保护。有关更多详细信息，请参阅 [LICENSE](LICENSE) 文件。

---

## 🆗 常见问题

~~**问：** 无法启动 api 服务器，错误：`java.lang.UnsatisfiedLinkError: no tdjni in java.library.path`~~

~~**答：** 可能是下载 tdlib 失败，您可以查看 [entrypoint.sh](entrypoint.sh) 文件，然后手动下载 tdlib。~~

**问：** Web 的剧透是静态的，如何解决？

**答：** 1. 因为并非所有浏览器都支持 `CSS Houdini Paint API`。 2. 它仅在 https 上受支持。
<details closed>
<summary>在 http 环境中使用，您可以使用以下方法解决</summary>

打开 `chrome://flags` 页面，搜索 `Insecure origins treated as secure`，然后将网页地址添加到列表中。
</details>

**问：** 如何使用 telegram-files 维护工具？

**答：** 您可以使用以下命令运行维护工具（**在运行命令之前，您应该停止 telegram-files 容器**）：
<details closed>
<summary>命令</summary>

```shell
docker run --rm \
  --entrypoint tfm \
  -v $(pwd)/data:/app/data \
  -e APP_ROOT=${APP_ROOT:-/app/data} \
  -e TELEGRAM_API_ID=${TELEGRAM_API_ID} \
  -e TELEGRAM_API_HASH=${TELEGRAM_API_HASH} \
  ghcr.io/jarvis2f/telegram-files:latest ${Maintenance Command}
```

**维护命令：**

- `album-caption`: 修复了 `0.1.15` 之前相册消息缺少标题的问题。
- `thumbnail`: 修复了缺少清晰缩略图的问题。
</details>
