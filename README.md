# AnimeFlow Updates

Public distribution-only repository for the Android app **AnimeFlow**.

- Latest version metadata: [latest.json](https://raw.githubusercontent.com/Chronaux/AnimeFlow-Updates/main/latest.json)
- Installers: [Releases](https://github.com/Chronaux/AnimeFlow-Updates/releases)

Only signed release APK files are published here. Application source code stays in the private `Chronaux/AnimeFlow` repository.

## Release metadata

`latest.json` is updated by the private repository's **Publish Android Update** workflow after a signed APK is successfully uploaded. The Android app checks `versionCode`, downloads the release APK, verifies its SHA-256 checksum, and launches the system installer with user confirmation.

**Important:** no installer is published yet. The initial manifest has `versionCode: 0` and is intentionally ignored by the app. Do not manually upload debug APKs: a new signing key cannot update an existing installation signed by a different certificate.

For releases, open the private source repository's workflow after its signing and publishing secrets have been configured. The release signing key must be backed up securely.
