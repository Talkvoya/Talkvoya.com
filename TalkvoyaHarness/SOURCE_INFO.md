[English](SOURCE_INFO.en.md) · **简体中文**

# 第三方源码材料与构建来源

对应版本：Talkvoya Harness 1.5.2（9），Android ARM64。

## 下载

- [APK 与全部附件](https://github.com/Talkvoya/Talkvoya.com/releases/tag/v1.5.2)
- [PRoot、依赖库、Ubuntu 对应源码及构建记录](https://github.com/Talkvoya/Talkvoya.com/releases/download/v1.5.2/talkvoya-harness-1.5.2-third-party-sources.zip)
- [LibreOffice WASM 上游补丁、构建材料与许可](https://github.com/Talkvoya/Talkvoya.com/releases/download/v1.5.2/talkvoya-harness-1.5.2-libreoffice-wasm-sources.zip)
- [全部附件 SHA-256 校验值](https://github.com/Talkvoya/Talkvoya.com/releases/download/v1.5.2/SHA256SUMS-1.5.2.txt)

普通用户只需安装 APK。第三方源码附件供许可证查阅、审计及第三方组件构建使用，不需要在手机上解压安装。

## PRoot 及原生依赖

- PRoot 5.1.107.102，GPL-2.0；对应源码包 SHA-256 为 `30d12a6e2cc4147123756ff58edea262d3083bbc238c12d0ab9b39e3d1c40852`。
- Termux 构建框架固定到引入该版本的提交 [b734bc49dc0eedb2c454e1c5d3c48d35d81d4bc9](https://github.com/termux/termux-packages/commit/b734bc49dc0eedb2c454e1c5d3c48d35d81d4bc9)，完整快照随附件提供。
- libtalloc 2.5.0：库代码 LGPL-3.0-or-later，源包其他文件按其各自许可；libandroid-shmem 0.7：BSD-3-Clause。两者均提供对应源码。
- 原始 Termux 安装包、加载器及依赖库的本地构建记录已核对。打包 PRoot 时使用 `patchelf` 将 `libtalloc.so.2` 改为 `libtalloc.so`，并将 RPATH 设置为 `$ORIGIN`。附件 README 列出具体重建步骤与文件映射。
- APK 内的 PRoot 与保留的调整后构建产物完全一致；加载器、libtalloc 和 libandroid-shmem 与原始 Termux 解包文件完全一致。

## Ubuntu

原始组装脚本使用官方 Ubuntu Base 24.04.5 ARM64。直接读取 APK 内的 dpkg 清单，确认 91 个已安装二进制包，对应 65 个源码包。

附件提供全部 65 个精确版本，共 208 个源码归档、补丁及 `.dsc` 文件，并附下载 URL、包版本、大小及 SHA-256。来源为 Ubuntu 官方软件仓库和 `20260909T000000Z` 日期快照，每个文件均按官方源码索引校验。

解压附件后，使用 `dpkg-source -x ubuntu/<包名>/<版本>.dsc` 展开 Debian/Ubuntu 源包，按其 `debian/control`、`debian/rules` 和补丁构建。本次使用官方已构建组件；没有声称完成逐位一致的源码重编译。

## LibreOffice WASM

DSH 内置的 `@deepseek-ai/libreoffice-kit-wasm` 0.1.5 使用 MPL-2.0，并带有其他组件许可。附件包含该上游包提供的 `sources/`、补丁、构建配置和 `licenses/`，已对照其 `prebuilds.json` 校验。

其记录的 LibreOffice Core 精确提交为 [bce0998afefdbc355585ca324285661a2170ba77](https://github.com/LibreOffice/core/tree/bce0998afefdbc355585ca324285661a2170ba77)，上游构建指定的[完整源码归档为 26.8.0.3](https://download.documentfoundation.org/libreoffice/src/26.8.0/libreoffice-26.8.0.3.tar.xz)。

## 许可与公开范围

这些是第三方开源组件材料，适用各自原始许可证，不统一改为 MIT。仓库 MIT 许可适用于发布文档；不改变第三方组件的许可，也不表示公开了 Talkvoya Harness 自有应用源码。

发布附件不包含本项目 Kotlin/Compose 源码、项目工程、签名私钥、API 密钥、用户凭据或聊天数据。APK SHA-256：`975704f8604e445d49d443b9788237709cb37135715a00f81d3514dfda57a074`。
