# Third-party source materials and build provenance

**English** · [Simplified Chinese](SOURCE_INFO.md)

These materials correspond to Talkvoya Harness 1.5.2 (build 9) for Android ARM64. Version 1.5.3 bundles the same runtime and native libraries.

## Downloads

- [Original runtime release and all assets](https://github.com/Talkvoya/Talkvoya.com/releases/tag/v1.5.2)
- [PRoot, dependency and Ubuntu sources, plus build records](https://github.com/Talkvoya/Talkvoya.com/releases/download/v1.5.2/talkvoya-harness-1.5.2-third-party-sources.zip)
- [LibreOffice WASM upstream patches, build materials, and licenses](https://github.com/Talkvoya/Talkvoya.com/releases/download/v1.5.2/talkvoya-harness-1.5.2-libreoffice-wasm-sources.zip)
- [SHA-256 checksums for all release assets](https://github.com/Talkvoya/Talkvoya.com/releases/download/v1.5.2/SHA256SUMS-1.5.2.txt)

Install the APK to use the app. The archives are provided for license review, auditing, and building the third-party components.

## PRoot and native dependencies

- PRoot 5.1.107.102 is licensed under GPL-2.0. The corresponding source archive's SHA-256 is `30d12a6e2cc4147123756ff58edea262d3083bbc238c12d0ab9b39e3d1c40852`.
- The archive includes a complete snapshot of the Termux build framework at the commit that introduced this version. [Termux build commit](https://github.com/termux/termux-packages/commit/b734bc49dc0eedb2c454e1c5d3c48d35d81d4bc9).
- The libtalloc 2.5.0 library is licensed under LGPL-3.0-or-later, and other files in its source package carry their respective licenses. libandroid-shmem 0.7 is licensed under BSD-3-Clause. The archive includes the corresponding source for both.
- We checked the original Termux packages, loader, and dependency build records. Packaging uses `patchelf` to change `libtalloc.so.2` to `libtalloc.so` and set RPATH to `$ORIGIN`. The archive README documents the build steps and file mapping.
- The PRoot binary in the APK matches the retained packaging output byte for byte. The loader, libtalloc, and libandroid-shmem match the files extracted from the original Termux packages.

## Ubuntu

The original assembly script used official Ubuntu Base 24.04.5 ARM64. The APK's `dpkg` inventory lists 91 installed binary packages corresponding to 65 source packages.

The archive contains all 65 exact source package versions, with 208 source archives, patches, and `.dsc` files. Its inventory records each download URL, version, size, and SHA-256 checksum. Sources came from the official Ubuntu archive and the `20260909T000000Z` snapshot. Each file was verified against the official source indexes.

To extract a Debian or Ubuntu source package, run `dpkg-source -x ubuntu/<package>/<version>.dsc`. Follow its `debian/control`, `debian/rules`, and patches to build it. The APK uses the official prebuilt components, and this verification did not reproduce their builds bit for bit.

## LibreOffice WASM

The runtime bundles `@deepseek-ai/libreoffice-kit-wasm` 0.1.5 under MPL-2.0 and other bundled component licenses. The archive includes the upstream package's `sources/`, patches, build configuration, and `licenses/`, checked against its `prebuilds.json`.

The upstream build identifies LibreOffice Core commit `bce0998afefdbc355585ca324285661a2170ba77` and the complete 26.8.0.3 source archive. [LibreOffice Core commit](https://github.com/LibreOffice/core/tree/bce0998afefdbc355585ca324285661a2170ba77) · [Upstream source archive](https://download.documentfoundation.org/libreoffice/src/26.8.0/libreoffice-26.8.0.3.tar.xz).

## Licenses and publication scope

Each third-party component keeps its original license. The repository's MIT license covers its release documentation. Talkvoya Harness's proprietary application source and project files, signing keys, API keys, credentials, and chat records remain outside the published assets.

The SHA-256 checksum of the 1.5.2 APK is `975704f8604e445d49d443b9788237709cb37135715a00f81d3514dfda57a074`.
