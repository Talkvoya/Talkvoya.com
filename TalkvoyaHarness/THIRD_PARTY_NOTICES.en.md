# Third-party components and license notices

**English** · [Simplified Chinese](THIRD_PARTY_NOTICES.md)

The Talkvoya Harness APK and runtime include the third-party software listed below. Keep this notice with any distribution of the APK.

| Component | Version | License | Source |
| --- | --- | --- | --- |
| Ubuntu Base | 24.04.5 | Ubuntu licenses, including GPL and LGPL components | [Ubuntu Base](https://cdimage.ubuntu.com/ubuntu-base/) |
| Node.js | 22.23.2 (LTS) | MIT | [Node.js](https://nodejs.org/) |
| PRoot | 5.1.107.102 | GPL-2.0 | [Termux build](https://github.com/termux/proot) |
| libtalloc | 2.5.0 | LGPL-3.0-or-later | [talloc](https://talloc.samba.org/) |
| libandroid-shmem | 0.7 | BSD-3-Clause | [libandroid-shmem](https://github.com/termux/libandroid-shmem) |
| LibreOffice WASM (@deepseek-ai/libreoffice-kit-wasm) | 0.1.5 | MPL-2.0 and bundled component licenses | [LibreOffice Kit](https://github.com/deepseek-ai/dsh-libreoffice-kit) |
| DeepSeek Harness (@deepseek-ai/dsh and dependencies) | 0.2.1-rc.4 | MIT, with separate licenses for dependencies | [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) and npm |
| Apache Commons Compress | 1.27.1 | Apache-2.0 | [Commons Compress](https://commons.apache.org/proper/commons-compress/) |
| XZ for Java | 1.10 | Public domain | [XZ for Java](https://tukaani.org/xz/java.html) |
| Kotlin, kotlinx.coroutines, and kotlinx.serialization | — | Apache-2.0 | [Kotlin](https://kotlinlang.org/) |
| Jetpack Compose and AndroidX | — | Apache-2.0 | [Android Jetpack](https://developer.android.com/jetpack) |

## GPL component notice for PRoot

PRoot is distributed under GPL-2.0. The APK bundles the official Termux binary. Packaging uses `patchelf` to change `DT_NEEDED` from `libtalloc.so.2` to `libtalloc.so` and set RPATH to `$ORIGIN` for use in Android's `nativeLibraryDir`.

The corresponding source for PRoot, libtalloc, libandroid-shmem, and the bundled Ubuntu packages is available alongside the original runtime release, together with the Termux build framework and provenance records. Source files retain their licenses and copyright notices. [Exact versions, downloads, and checksums](SOURCE_INFO.en.md).

## Trademarks

- Talkvoya and Talkvoya Harness are the project's names and marks.
- DeepSeek, DeepSeek Harness, and related marks belong to their respective owners. Talkvoya Harness is an independent third-party client.
