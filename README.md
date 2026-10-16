# Xget Now

***[English](README.en.md)***

一个适用于 Chromium 和 Firefox 的跨浏览器扩展，通过将文件下载无缝转交给 [Xget](https://github.com/xixu-me/Xget) 实例来加速下载。

> ✨ **下载素材之后，继续把它做成作品。** 参考图片、视频或其他素材准备好后，可以用 [Renoise](https://renoise.ai/plugin) 在 AI 对话里继续生成视频、图片和音乐；[官方插件仓库](https://github.com/ArcoCodes/renoise-plugins-official)提供 MCP 与 Agent Skill 的接入方式。

> [!TIP]
> 欢迎加入“Xget 开源与 AI 交流群”，一起交流开源项目、AI 应用、工程实践、效率工具和独立开发；如果你也在做产品、写代码、折腾项目或者对开源和 AI 感兴趣，欢迎[**进群**](https://file.xi-xu.me/QR%20Codes/%E7%BE%A4%E4%BA%8C%E7%BB%B4%E7%A0%81.png)认识更多认真做事、乐于分享的朋友。

> [!NOTE]
> 想快速开始：安装商店版本，填入你的 Xget 域名，例如 `xget.xi-xu.me`，保持目标平台开关开启即可。

## 概览

Xget Now 会在受支持的平台上识别真实下载链接，把请求重写到你的 Xget 域名，并继续使用浏览器原生下载流程。你不需要改动原始站点，也不需要手动复制链接。

## 功能特性

- 自动下载加速：无缝重定向下载，通过 Xget 获得更快速度。
- 可配置设置：自定义你的 Xget 域名和平台偏好。
- 智能通知：下载重定向时提供可视化反馈。
- 隐私优先：所有处理都在你的浏览器本地进行。
- 按平台控制：为特定平台启用或禁用加速。
- 跨浏览器支持：同时支持 Chromium 和 Firefox 浏览器。

## 支持的平台

- 代码托管平台：GitHub、GitLab、Gitea、Codeberg、SourceForge、AOSP。
- AI / ML 平台：Hugging Face。
- 包管理与分发平台：npm、PyPI、PyPI Files、Conda、Conda Community、Maven Central、Apache Downloads、Gradle Plugin Portal、RubyGems、CRAN、CPAN、CTAN、Go Modules、NuGet、Crates.io、Packagist。
- 其他平台：arXiv、F-Droid。

## 安装

### 商店安装

- [Chrome 应用商店](https://chromewebstore.google.com/detail/ajiejgobfcifcikbahpijopolfjoodgf?hl=zh-CN)
- [Chrome 应用商店镜像](https://chromewebstore.xi-xu.me/detail/ajiejgobfcifcikbahpijopolfjoodgf)
- [Firefox 附加组件](https://addons.mozilla.org/zh-CN/firefox/addon/xget-now/)
- [Edge 加载项](https://microsoftedge.microsoft.com/addons/detail/jigpfhbegabdenhihpplcjhpfdcgnalc?hl=zh-CN&gl=CN)

### 手动安装

如果你更喜欢手动安装扩展，或者应用商店版本不可用，可以直接下载发布包或从源码加载。

#### 方式 1：从 GitHub Releases 安装

1. 前往 [Releases 页面](https://github.com/xixu-me/Xget-Now/releases/latest)。
2. 下载对应浏览器的扩展文件：
   - `Xget-Now_x.x.x.chromium.zip`：适用于所有基于 Chromium 的浏览器，例如 Chrome、Edge、Opera。
   - `Xget-Now_x.x.x.firefox.xpi`：适用于 Firefox 浏览器。
3. 在 Chrome 中安装：
   - 解压 Chromium 版本 `.zip` 文件。
   - 打开 `chrome://extensions/`。
   - 启用右上角的“开发者模式”。
   - 点击“加载已解压的扩展程序”，选择解压后的文件夹。
4. 在 Firefox 中安装：
   - 打开 `about:debugging`。
   - 点击“此 Firefox”。
   - 点击“临时载入附加组件”。
   - 选择下载的 Firefox `.xpi` 文件，或解压后目录中的 `manifest.json` 文件。
5. 在 Edge 中安装：
   - 解压 Chromium 版本 `.zip` 文件。
   - 打开 `edge://extensions/`。
   - 启用左侧边栏中的“开发人员模式”。
   - 点击“加载解压缩的扩展”，选择解压后的文件夹。
6. 在其他基于 Chromium 的浏览器中安装：
   - 使用 Chromium 版本的扩展包。
   - 先启用浏览器的“开发者模式”。
   - 按照对应浏览器的扩展安装指南完成加载。

#### 方式 2：从源码安装

1. 克隆仓库：

   ```bash
   git clone https://github.com/xixu-me/Xget-Now.git
   cd Xget-Now
   ```

2. 可选构建：

   `build.py` 仅依赖 Python 标准库，安装 Python 3.7+ 后即可运行。

   ```bash
   python build.py --platform chrome
   python build.py --platform firefox
   python build.py --platform all
   python build.py --platform all --package
   ```

3. 在浏览器中加载：
   - Chromium 浏览器：
     - 打开 `chrome://extensions/` 或 `edge://extensions/`。
     - 启用“开发者模式”。
     - 点击“加载已解压的扩展程序”，选择源码根目录，或选择构建后的 `build/chrome/` 目录。
   - Firefox 浏览器：
     - 打开 `about:debugging`。
     - 点击“此 Firefox”。
     - 点击“临时载入附加组件”。
     - 选择源码根目录中的 `manifest-firefox.json`，或构建后的 `build/firefox/manifest.json`。

#### 验证安装

安装后，你应该能在浏览器工具栏中看到 Xget Now 图标。点击图标，配置你的 Xget 域名并开始加速下载。

## 上手配置

1. 点击工具栏中的扩展图标。
2. 输入你的 Xget 域名，例如 `xget.xi-xu.me`。
3. 启用扩展，并按需打开或关闭各个平台的开关。
4. 访问任何受支持的平台，像往常一样点击下载链接。
5. 下载会自动通过 Xget 转发和加速。

## 工作原理

1. 检测：扩展监控受支持平台上的下载链接。
2. 转换：URL 自动转换为 Xget 兼容格式。
3. 重定向：下载通过你配置的 Xget 域名路由。
4. 加速：Xget 的全球 CDN 和优化能力提供更快的下载速度。

## 运行要求

### 浏览器支持

- Chrome：88+。
- Edge：88+。
- Opera：74+。
- 其他基于 Chromium 的浏览器：支持 Manifest V3 的版本。
- Firefox：109+。
- Firefox ESR：109+。

### Xget 实例

你可以直接使用预部署实例 `xget.xi-xu.me`，也可以参考 [Xget 部署文档](https://github.com/xixu-me/Xget#-%E9%83%A8%E7%BD%B2) 自行部署。

## 隐私与安全

- 本地处理：所有 URL 转换都在你的浏览器中进行。
- 无数据收集：扩展不收集或传输个人数据。
- 最小权限：仅请求功能所需的必要权限。
- 开源可审计：完整源码可供检查。

查看 [隐私政策](PRIVACY_POLICY.md) 了解完整细节。

## 故障排除

### 常见问题

**扩展不工作？**

- 确保你已配置有效的 Xget 域名。
- 检查扩展在弹出窗口中是否已启用。
- 验证目标平台是否已启用。
- 更改设置后尝试刷新页面。

**下载没有被重定向？**

- 更改设置后刷新页面。
- 检查浏览器控制台的错误消息（`F12` -> “控制台”）。
- 确保链接是被识别的下载类型。
- 验证你点击的是实际下载链接，而不是导航链接。

**Xget 域名问题？**

- 域名应该不带 `https://` 协议。
- 示例：`xget.xi-xu.me`，而不是 `https://xget.xi-xu.me`。
- 检查域名在浏览器中是否可访问。
- 可以先尝试默认的预部署实例：`xget.xi-xu.me`。

**性能问题？**

- 检查你的网络连接。
- 如果可用，尝试其他 Xget 域名。
- 验证目标平台的服务器是否响应。
- 清除浏览器缓存并重新加载扩展。

**Firefox 特定问题？**

- 确保 Firefox 版本为 109+。
- 在 `about:debugging` 中检查扩展是否正确加载。
- Firefox 可能需要重启浏览器才能完全应用扩展设置。
- 检查 Firefox 的“隐私和安全”设置是否阻止了扩展功能。

### 调试模式

Chromium 浏览器中，打开开发者工具并查看 Console 选项卡。Firefox 中，打开 `about:debugging`，点击“此 Firefox”，找到 Xget Now 扩展并点击“检查”，然后查看控制台消息。

常见调试消息：

- 扩展加载：`Xget Now: Content script loaded`
- 下载重定向：`Redirecting download: [original] -> [Xget]`
- 设置更改：`Settings updated! Click to refresh page`

## 常见问题

### 这个扩展是免费的吗？

是的，扩展完全免费，并且以 GPL-3.0 许可证开源。

### 我可以使用自己的 Xget 服务器吗？

当然可以。你可以使用 [Xget 存储库](https://github.com/xixu-me/Xget) 部署自己的 Xget 实例，并配置扩展使用你的域名。

### 为什么有些下载仍然通过原始服务器？

扩展只重定向被识别的下载链接。导航链接、预览链接和一些动态内容可能不会被重定向。

### 我的浏览数据会被收集吗？

不会。扩展完全在本地运行，不收集或传输浏览数据。更多说明见 [隐私政策](PRIVACY_POLICY.md)。

### 下载能快多少？

速度提升取决于你的地理位置、网络状况和文件大小。典型改进范围约为 2 倍到 10 倍。

### 我可以为特定网站禁用扩展吗？

可以。使用扩展弹出窗口中的按平台开关，即可为特定平台禁用加速。

### 为什么 Chrome 和 Firefox 版本不同？

由于浏览器架构差异，我们分别做了适配：

- Chrome 版本：使用 Manifest V3，支持较新的扩展 API 和安全特性。
- Firefox 版本：使用 Manifest V2，以确保与 Firefox 扩展系统的兼容性。

两者的核心功能保持一致，差异主要在底层实现。

### 可以同时在 Chrome 和 Firefox 中使用吗？

可以。你可以在多个浏览器中同时安装和使用 Xget Now，它们会独立工作，并分别保存各自的设置。

## 支持与反馈

如果你觉得这个扩展有用，可以：

- 为仓库点个 Star。
- 在应用商店留下评价：
  - [Chrome 应用商店](https://chromewebstore.google.com/detail/ajiejgobfcifcikbahpijopolfjoodgf?hl=zh-CN)
  - [Firefox 附加组件](https://addons.mozilla.org/zh-CN/firefox/addon/xget-now/)
  - [Edge 加载项](https://microsoftedge.microsoft.com/addons/detail/jigpfhbegabdenhihpplcjhpfdcgnalc?hl=zh-CN&gl=CN)
- 通过 [GitHub Issues](https://github.com/xixu-me/Xget-Now/issues) 报告错误或建议功能。
- 分享给其他可能受益于更快下载的人。

> [!NOTE]
> 本仓库采用 GPL-3.0 许可证。完整条款见 [LICENSE](LICENSE)。
