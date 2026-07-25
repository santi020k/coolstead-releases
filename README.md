# Coolstead Releases

This repository contains the official, signed release artifacts for [Coolstead](https://coolstead.santi020k.com), a native macOS thermal monitor and conservative fan controller.

The application source is maintained privately. This repository intentionally contains release binaries and update metadata only.

## Install

Download the latest notarized DMG from [Releases](https://github.com/santi020k/coolstead-releases/releases/latest), or install with Homebrew:

```bash
brew install --cask santi020k/tap/coolstead
```

Direct-download installations can receive signed in-app updates. Homebrew installations remain managed by `brew upgrade --cask coolstead`.

## Safety

Monitoring works without fan-control access. Fan control is optional and requires administrator approval. Before uninstalling Coolstead, disable cooling and quit the app so every fan returns to macOS automatic control.

Coolstead is not affiliated with or endorsed by Apple. Hardware support varies by Mac model.
