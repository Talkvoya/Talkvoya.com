# 第三方组件与许可证声明

Talkvoya Harness 的 APK 与运行时中包含以下第三方软件。分发本 APK 时请一并保留本文件。

| 组件 | 版本 | 许可证 | 来源 |
|---|---|---|---|
| Ubuntu Base | 24.04.5 | Ubuntu 许可证（含 GPL/LGPL 组件） | https://cdimage.ubuntu.com/ubuntu-base/ |
| Node.js | 22.23.2 (LTS) | MIT | https://nodejs.org/ |
| PRoot | 5.1.107.102 | GPL-2.0 | https://github.com/termux/proot （Termux 构建） |
| libtalloc | 2.5.0 | LGPL-3.0-or-later | https://talloc.samba.org/ |
| libandroid-shmem | 0.7 | BSD-2-Clause | https://github.com/termux/libandroid-shmem |
| DeepSeek Harness (@deepseek-ai/dsh 及其依赖) | 0.2.1-rc.4 | MIT（依赖各自许可证） | https://github.com/deepseek-ai/deepseek-harness / npm |
| Apache Commons Compress | 1.27.1 | Apache-2.0 | https://commons.apache.org/proper/commons-compress/ |
| XZ for Java | 1.10 | Public Domain | https://tukaani.org/xz/java.html |
| Kotlin / kotlinx.coroutines / kotlinx.serialization | — | Apache-2.0 | https://kotlinlang.org/ |
| Jetpack Compose / AndroidX | — | Apache-2.0 | https://developer.android.com/jetpack |

## GPL 组件说明（PRoot）

PRoot 以 GPL-2.0 分发。APK 中内置的是 Termux 官方构建的二进制（使用 `patchelf` 把 `DT_NEEDED` 的 `libtalloc.so.2` 改为 `libtalloc.so`，以便放入 Android `nativeLibraryDir`）。对应源码可从 <https://github.com/termux/proot> 获取。

## 商标

- Talkvoya / Talkvoya Harness 为本项目名称与标识。
- DeepSeek、DeepSeek Harness 相关名称与标识归其所有者。本应用为第三方客户端，与 DeepSeek 官方无关联。
