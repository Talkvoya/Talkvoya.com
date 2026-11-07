# Install and get help

[Product](README.md) · [Download](DOWNLOAD.en.md) · [简体中文](HELP.md)

## First launch

1. Get the signed APK from the [download center](DOWNLOAD.en.md). Use Android 8.0 or later on ARM64, with about 1.4 GB available for runtime setup.
2. Open the downloaded APK. If Android prompts you to allow installation from your current source, review the prompt and allow that source to install the APK.
3. Open Harness, review the notice of use, and wait for local runtime setup.
4. In **Settings**, add a model API key you control and choose a supported model. Open a new chat and send a short message.
5. Phone control and the progress overlay have separate Android permissions. Enable the ones you want to use from Settings.

## Common questions

| What you see | What to check |
| --- | --- |
| Android cannot install the APK | Check Android version, ARM64 compatibility, available space, and whether your organization or device restricts sideloading. |
| Android reports a signature conflict | Use a Talkvoya-signed build matching the installed app. Export or back up important content before uninstalling. Uninstalling removes local app data. |
| Local runtime setup stalls | Check free space and engine logs. Try restarting the engine from Settings. |
| The model rejects a request | Check the selected provider, model, network connection, API key status, and provider balance or quota. Keep the key private. |
| Phone control does not work | Check the optional Accessibility service, screen state, sensitive-app list, and device restrictions. For background progress, check the relevant Android permissions. |
| I want to change the language | In **Settings → Experience → Language**, choose English or Simplified Chinese. |

[Report an issue or contact Talkvoya](../SUPPORT.md) · [Data and permissions](TRUST.en.md)
