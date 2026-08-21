# Coolstead Releases

This repository contains the official, signed release artifacts for
[Coolstead](https://coolstead.santi020k.com), a native macOS thermal monitor
and conservative fan controller.

The application source is maintained privately. This repository intentionally
contains release binaries and update metadata only.

## Install

Download the latest notarized DMG from
[Releases](https://github.com/santi020k/coolstead-releases/releases/latest), or
install with Homebrew:

```bash
brew install --cask santi020k/tap/coolstead
```

Direct-download installations can receive signed in-app updates. Homebrew
installations remain managed by `brew upgrade --cask coolstead`.

## Release integrity

New releases are immutable after publication. GitHub displays a SHA-256 digest
for each asset on the release page, and the versioned and stable-name DMGs are
required to contain identical bytes. You can compare a downloaded file with
the displayed digest:

```bash
shasum -a 256 Coolstead-<version>.dmg
```

macOS also verifies the Developer ID signature and notarization when the app
opens. Advanced users can verify a copied installation:

```bash
spctl --assess --type execute --verbose=4 /Applications/Coolstead.app
xcrun stapler validate /Applications/Coolstead.app
```

## Safety

Monitoring works without fan-control access. Fan control is optional and
requires administrator approval. Before uninstalling Coolstead, disable
cooling and quit the app so every fan returns to macOS automatic control.

Coolstead is not affiliated with or endorsed by Apple. Hardware support varies
by Mac model.

## Security

Do not install an asset whose digest or macOS signature verification fails.
Follow the repository's security policy and contact the maintainer privately
with suspected release, signature, or update-channel issues.
