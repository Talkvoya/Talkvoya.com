# Release maintenance / 发布维护

1. Build and sign the APK in the private app project. Check its version, package, signing certificate and SHA-256. Use a new version tag for changed binaries.
2. Prepare a GitHub Release draft with the signed ARM64 APK, checksum and bilingual notes. Keep a local copy of the outgoing APK for support before publishing.
3. Set the new stable release as **Latest**. The [release workflow](https://github.com/Talkvoya/Talkvoya.com/actions/workflows/harness-releases.yml) downloads and verifies the new APK before retiring older public APK and checksum attachments. It can also be run manually. Archive notes and third-party source materials stay available for provenance.
4. Update `docs/release.json`, both download and release-note pages, and the matching static site pages from the same release metadata. GitHub Pages deploys from `main:/docs`. Sync the same static files to the official release center. Verify both languages, the APK digest, and anonymous access.
5. Keep release immutability disabled while the public download policy allows only the latest APK. Immutable historical assets cannot be retired individually.

1. 在私有应用工程构建并签名，核对版本、包名、签名证书和 SHA-256。安装包变化时使用新的版本标签。
2. 在 GitHub 发布草稿中添加签名 ARM64 APK、校验文件和双语说明，发布前保留被替换安装包的本地备份。
3. 将新版设为 **Latest**。[发布流程](https://github.com/Talkvoya/Talkvoya.com/actions/workflows/harness-releases.yml) 会完整下载并校验新版，然后下架旧 APK 和对应校验文件。必要时可手动运行。历史发布记录和第三方源码材料继续保留。
4. 按同一份发布数据同步更新 `docs/release.json`、双语下载与版本说明、对应静态页。GitHub Pages 从 `main:/docs` 部署，官网发布中心同步同一套静态文件。校验中英文页面、APK 哈希和匿名访问。
5. 最新版独占下载策略实施期间，保持 Release 不可变设置关闭，以便下架旧安装包。
