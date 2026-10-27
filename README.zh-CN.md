# TDevTools

**面向开发者的免费桌面工具集：47 款 JSON、XML、架构、API、编码和证书工具，支持 macOS、Windows 和 Linux。**

由 [transposal.app](https://transposal.app) 提供

**切换语言：** [English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Türkçe](README.tr.md) · [日本語](README.ja.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md)

> **🔒 所有处理均在本地完成，数据不会离开你的电脑。** TDevTools 在你的设备上处理所有内容。JSON、XML 文件、令牌、密钥和证书不会上传或发送到分析服务。无需账户，也不会跟踪用户。只有在你主动操作时，应用才会连接互联网，例如加载 URL、向你的 API 发送测试请求或获取服务器证书。其他工具均可离线使用。

## 屏幕截图

**JSON → JSON Schema：** 根据示例数据推断架构。

![JSON 转 JSON Schema](screenshots/json-to-schema.png)

**API 测试器：** 发送请求，并以树形、表格或文本查看响应。

![API 测试器](screenshots/api-tester.png)

**证书检查器：** 查看证书链并验证证书和签名。

![证书检查器](screenshots/certificate-inspector.png)

## 下载

请从[发布页面](https://github.com/siddiquin/TDevTools-releases/releases/latest)下载最新版本。

| 系统 | 下载文件 |
| --- | --- |
| macOS，Apple Silicon (M1–M4) | `TDevTools-<version>-arm64.dmg` |
| macOS，Intel | `TDevTools-<version>-x64.dmg` |
| Windows 10/11，64 位 | `TDevTools-Setup-<version>-x64.exe` |
| Windows 10/11，ARM | `TDevTools-Setup-<version>-arm64.exe` |
| Windows，便携版 | `TDevTools-Portable-<version>.exe` |
| Linux，64 位 (x86_64) | `TDevTools-<version>-x86_64.AppImage` |
| Linux，ARM64 | `TDevTools-<version>-arm64.AppImage` |

**系统要求：** macOS 12 Monterey 或更高版本；Windows 10/11（64 位或 ARM64）；或较新的 64 位 Linux 发行版（Ubuntu 20.04+、Debian 11+、Fedora 36+ 等）。需要约 300 MB 磁盘空间。

## 安装

### macOS

1. 下载适用于你的 Mac 的 `.dmg` 文件，打开并接受许可协议。
2. 将 **TDevTools** 拖到**应用程序**文件夹，然后推出磁盘映像。
3. 首次打开时，macOS 可能提示无法验证该应用，因为它未使用付费 Apple 开发者证书签名。这是预期情况，只需授权一次。
   - **macOS 14 及更早版本：** 在 Finder 中右键点击 TDevTools，选择**打开**并再次确认。
   - **macOS 15 及更高版本：** 尝试打开应用，在警告中点击**完成**。进入**系统设置 → 隐私与安全性**，点击 TDevTools 被阻止提示旁的**仍要打开**并确认。
4. 如果 macOS 提示「TDevTools 已损坏，无法打开」，请先确认文件来自官方[发布页面](https://github.com/siddiquin/TDevTools-releases/releases/latest)。然后在终端运行 `xattr -dr com.apple.quarantine /Applications/TDevTools.app`，仅移除此应用的下载隔离标记。

### Windows

- **安装程序：** 运行 `TDevTools-Setup-<version>-x64.exe`（ARM 电脑使用 `arm64` 文件），接受许可协议并点击**安装**。如果 SmartScreen 显示「Windows 已保护你的电脑」，请选择**更多信息 → 仍要运行**。应用仅安装到你的用户账户，无需管理员权限。
- **便携版：** 运行 `TDevTools-Portable-<version>.exe`。如果出现 SmartScreen 提示，请选择**更多信息 → 仍要运行**。

### Linux (AppImage)

下载对应文件，在**属性 → 权限**中允许执行，或运行 `chmod +x TDevTools-*.AppImage`，然后双击或从终端启动。如果无法启动，某些发行版需要 FUSE 2（Ubuntu/Debian：`sudo apt install libfuse2`；Ubuntu 24.04：`sudo apt install libfuse2t64`；Fedora：`sudo dnf install fuse-libs`）。可使用 Gear Lever 或 AppImageLauncher 将其添加到应用菜单。

## 更新与卸载

下载新版本并按相同方式安装即可，偏好设置会保留。macOS 上替换「应用程序」中的旧版本；Windows 上运行新安装程序；Linux 上替换 AppImage 文件。

- **macOS：** 将 TDevTools 移到废纸篓。若要同时删除偏好设置，请删除 `~/Library/Application Support/TDevTools`。
- **Windows：** 在**设置 → 应用 → 已安装的应用**中卸载 TDevTools。若要同时删除偏好设置，请删除 `%APPDATA%\TDevTools`。便携版只需删除 `.exe`。
- **Linux：** 删除 AppImage。若要同时删除偏好设置，请删除 `~/.config/TDevTools`。

应用只保存主题、语言等偏好设置，不会保存你的数据、密码或密钥副本。

## 功能

- **格式化与验证：** JSON 格式化、验证、修复和可视化编辑；JSON、XML、CSV、Excel、YAML、TOON、JSONL 转换；Markdown、JSON/XML 架构（XSD）和 TypeScript 类型生成。
- **安全：** JWT 解码、验证和签名；Base64/URL/SAML 编码；MD5、SHA-1、SHA-256 哈希；生成自签名证书和 mTLS 套件；检查证书、公钥和 JKS 密钥库。
- **查看与 API：** JSON 树形、表格、网格、图形和原始视图；OpenAPI/Swagger 浏览器、支持 OAuth2 和 mTLS 的 HTTP 客户端、SOAP/WSDL 查看器、文件查看器和 Markdown 预览。
- **查询与转换：** JSONPath 测试器、正则表达式搜索与替换、可导出为 JavaScript、TypeScript、Python 或 C# 的 JSON 映射器；可选云服务 Transposal Mapper。
- **比较：** JSON/XML 结构差异比较，以及显示逐行错误的 JSON Schema 验证。
- **应用内体验：** 8 种语言、6 种主题、强调色、密度和缩放设置、一键复制、右键菜单、拖放文件，以及状态栏中的 CPU 和内存使用情况。

## 隐私与安全

- 所有处理均在本地完成；粘贴或打开的内容不会上传。
- 无账户、遥测或广告。
- 仅在你主动要求时联网，例如加载 URL、测试 API 或获取证书。
- 密码、令牌和私钥仅在应用运行期间保存在内存中；只会保存偏好设置。
- 使用隔离窗口和严格的内容安全策略；HTML 预览不会运行脚本；打开程序或脚本前会征求确认；登录信息只会发送到你选择的服务器。
- 内置示例使用公共演示服务器，每 2 分钟最多请求一次。你自己的 URL 和文件不受限制。

## 常见问题

**TDevTools 免费吗？** 是的，开发者可免费使用。请参阅[许可协议](LICENSE.md)。

**可以离线使用吗？** 可以。只有需要与所选服务器通信的功能（加载 URL、API/SOAP 测试、获取证书链）需要联网。

**源代码是否公开？** TDevTools 为闭源软件。请发送主题为「TDevTools」的邮件至 **<support@transposal.app>** 申请源代码。

**为什么安装时会出现安全警告？** 应用未使用付费 Apple 或 Microsoft 开发者证书签名，因此 Gatekeeper 和 SmartScreen 会在首次打开时发出警告。请按安装说明操作，并且只从官方[发布页面](https://github.com/siddiquin/TDevTools-releases/releases/latest)下载。

## 许可与支持

- [最终用户许可协议](LICENSE.md)：可免费使用，不提供担保。应用内**帮助 → 许可协议**提供完整的 8 种语言版本。
- [第三方声明](THIRD_PARTY_NOTICES.md)
- 支持：**<support@transposal.app>**
- 网站：[transposal.app](https://transposal.app)

© 2026 Transposal。保留所有权利。