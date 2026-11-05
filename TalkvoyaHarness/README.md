# Talkvoya Harness

Talkvoya Harness 是独立开发的 Android 客户端。它在手机上运行 DeepSeek Harness 环境，使用你配置的模型供应商和 API 密钥，支持聊天、工具调用和可选的手机操控。Talkvoya Harness 与 DeepSeek 官方无关联。

## 获取与安装

本目录是发布说明。APK 的实际发布状态以 [GitHub Releases](https://github.com/Talkvoya/Talkvoya.com/releases) 中是否存在对应版本和 APK 附件为准。

1. 下载 ARM64 APK 和同版本的 SHA-256 校验文件。支持 Android 8.0 及以上的 arm64-v8a 设备。
2. 校验 APK。Windows 可运行 `Get-FileHash -Algorithm SHA256 <APK文件>`，将结果与发布的校验值比较。
3. 在 Android 上打开 APK，按系统提示授权当前安装来源。首次打开时阅读并勾选使用告知，然后安装内置运行环境。请预留约 1.4 GB 空间。
4. 打开设置，选择模型供应商并填写自己的 API 密钥。密钥保存在设备上，由对应供应商处理模型请求和计费。
5. 如需手机操控，在设置中开启手机操控与 Android 无障碍权限。敏感应用限制由你在设置中管理。

## 1.5.2 更新

- 新对话使用新的欢迎语。
- 对话中 Markdown 表格按行列显示，长文字会换行，宽表格可横向滚动。旧对话可直接使用更新后的显示方式。
- 在「设置 → 关于」可查看 WhatsApp Business 联系二维码和打开本页面。

## 使用告知与许可

- [免责声明与使用告知](DISCLAIMER.md)
- [内置第三方组件及许可](THIRD_PARTY_NOTICES.md)
- 本目录的发布文档采用仓库的 [MIT 许可证](../LICENSE)。APK 内置组件适用各自许可证。应用代码和凭据属于本地项目。
