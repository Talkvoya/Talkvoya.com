# Talkvoya Harness release notes

**English** · [Version 1.5.3 in Simplified Chinese](https://github.com/Talkvoya/Talkvoya.com/releases/tag/v1.5.3) · [Version 1.5.2 in Simplified Chinese](https://github.com/Talkvoya/Talkvoya.com/releases/tag/v1.5.2)

## Version 1.5.3

New chats open with a greeting and message field. The engine description and four suggested prompts were removed. The About screen uses the Talkvoya.com and Talkvoya labels, and its GitHub link opens the Talkvoya product hub.

Download the ARM64 APK for Android 8.0 or later. Allow about 1.4 GB for first-time runtime setup. The app uses the same signing certificate as 1.5.2 for in-place upgrades. [Version 1.5.3 APK](https://github.com/Talkvoya/Talkvoya.com/releases/download/v1.5.3/talkvoya-harness-1.5.3-arm64.apk) · [SHA-256 file](https://github.com/Talkvoya/Talkvoya.com/releases/download/v1.5.3/talkvoya-harness-1.5.3-arm64.apk.sha256).

APK SHA-256: `49c475b2fab3cc8283fb7e1b73d23a8bbbcb99bb164cfb6f7bda6eb49928e7a0`

The bundled runtime and native libraries match 1.5.2 byte for byte. The corresponding third-party sources and build records remain available with 1.5.2. [Source materials](SOURCE_INFO.en.md).

## Version 1.5.2

Talkvoya Harness is an independent Android client for model selection, configurable reasoning depth, multiple providers, tool use, optional phone control, and a task overlay.

- Updated the new-chat greeting to “Hi, how can I help you?”
- Rendered Markdown tables in rows and columns, with wrapping for long text and horizontal scrolling for wide tables.
- Added a WhatsApp Business contact QR code and a GitHub link in Settings.

Download the ARM64 APK for Android 8.0 or later and allow about 1.4 GB for runtime setup. The source archives are provided separately. Back up important data before upgrading. On first launch, review the use notice, install the runtime, and add your own model provider API key in Settings. Keep your key private. [Installation guide](README.md) · [Version 1.5.2 assets](https://github.com/Talkvoya/Talkvoya.com/releases/tag/v1.5.2).

APK SHA-256: `975704f8604e445d49d443b9788237709cb37135715a00f81d3514dfda57a074`

The release includes checksums and the corresponding source materials for PRoot, its dependencies, and the bundled Ubuntu packages. It also includes the upstream LibreOffice WASM patches, build materials, and license notices. [Source materials and checksums](SOURCE_INFO.en.md).

The release passed build, signature, archive, and hash checks. The relevant UI was checked on an Android 15 x86_64 emulator. Testing did not comprehensively cover physical ARM64 devices, manufacturer-specific Android builds, or live requests to OpenAI and Claude.

Models can make mistakes. Full permissions allow enabled tools to run automatically. Manage the sensitive-app list and use care with payments and important files. [Disclaimer and use notice](DISCLAIMER.en.md).

[Product page](README.md) · [Third-party license notices](THIRD_PARTY_NOTICES.en.md) · [Official channels](https://github.com/Talkvoya/Talkvoya.com#official-channels)
