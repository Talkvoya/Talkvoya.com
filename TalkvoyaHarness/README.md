# Talkvoya Harness

Talkvoya Harness 是独立开发的 Android 客户端。它在手机上运行 DeepSeek Harness 环境，使用你配置的模型供应商和 API 密钥，支持聊天、工具调用和可选的手机操控。Talkvoya Harness 与 DeepSeek 官方无关联。

## 获取与安装

**[下载 Talkvoya Harness 1.5.2 ARM64 APK](https://github.com/Talkvoya/Talkvoya.com/releases/download/v1.5.2/talkvoya-harness-1.5.2-arm64.apk)** · [版本发布页与校验文件](https://github.com/Talkvoya/Talkvoya.com/releases/tag/v1.5.2)

APK 约 133.69 MiB，Android 8.0 及以上，ARM64（arm64-v8a）。本目录仅提供发行文档，不公开应用项目源码、API 密钥或签名密钥。

1. 下载 ARM64 APK 和同版本的 SHA-256 校验文件。支持 Android 8.0 及以上的 arm64-v8a 设备。
2. 校验 APK。Windows 可运行 `Get-FileHash -Algorithm SHA256 <APK文件>`，将结果与发布的校验值比较。
3. 在 Android 上打开 APK，按系统提示授权当前安装来源。首次打开时阅读并勾选使用告知，然后安装内置运行环境。请预留约 1.4 GB 空间。
4. 打开设置，选择模型供应商并填写自己的 API 密钥。密钥保存在设备上，由对应供应商处理模型请求和计费。
5. 如需手机操控，在设置中开启手机操控与 Android 无障碍权限。敏感应用限制由你在设置中管理。

升级时可直接覆盖安装，1.5.2 延续原签名。重要内容请先备份；卸载会删除本地运行环境、对话、设置和密钥。

## 可以做什么

- 使用 DeepSeek、OpenAI、Claude 等已配置供应商的模型；保存多把密钥并选择，按模型能力选择思考深度。
- 流式对话、可复制文字、折叠思考与工具详情、Markdown 表格、最近会话置顶，中英文界面。
- 可选无障碍手机操控、顶部任务进度悬浮窗，以及执行过程中发送插话。
- 运行环境在手机本地；调用模型仍需要网络，由模型供应商处理请求并计费。

## 使用前须知

请先阅读[免责声明与使用告知](DISCLAIMER.md)。完全权限会自动执行已经启用的工具，可能修改文件和应用状态。金融支付、敏感文件等操作请自行设置限制，并把相关应用加入敏感应用名单。模型可能误判，不能保证操作结果或收益。不要将 API 密钥放在聊天记录、截图或公开问题中。

本版本已完成构建、签名和归档校验，并在 Android 15 x86_64 模拟器验证界面与相关回归。**ARM64 真机、不同厂商后台限制及 OpenAI/Claude 在线请求尚未全面验证**。请先用非敏感任务试用。

如果引擎无法启动，请检查存储空间、设备架构及「运行日志」；如确需重装运行环境，请先备份重要工作文件。没有 Key 或余额不足时，应在对应模型供应商处配置，不需要向开发者提供 Key。

## 1.5.2 更新

- 新对话使用新的欢迎语。
- 对话中 Markdown 表格按行列显示，长文字会换行，宽表格可横向滚动。旧对话可直接使用更新后的显示方式。
- 在「设置 → 关于」可查看 WhatsApp Business 联系二维码和打开本页面。

## 使用告知与许可

- [免责声明与使用告知](DISCLAIMER.md)
- [内置第三方组件及许可](THIRD_PARTY_NOTICES.md)
- [第三方源码材料与构建来源](SOURCE_INFO.md)（与 APK 同一 Release 提供下载）
- 本目录的发布文档采用仓库的 [MIT 许可证](../LICENSE)。APK 内置组件适用各自许可证。应用代码和凭据属于本地项目。

## 联系

[Talkvoya 官网](https://talkvoya.com/)；也可在应用的「设置 → 关于 → 联系我们」查看 WhatsApp Business 二维码。
