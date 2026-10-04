<div align="center">

# Drion

### Android apps, Linux-shaped.

A Wine-like Android compatibility platform. Drion preserves the contracts Android apps expect and replaces system-side behavior with Rust and hosted ART — so Android apps run on Linux with real host integration, not beside it.

[Website](https://actinis.io/drion) · [Documentation](https://github.com/Actinis-Drion/docs)

</div>

---

## What is Drion?

Drion is a compatibility platform for running Android applications directly on Linux.

Apps see familiar Android contracts — Binder, Activity, Service, ContentProvider, package metadata, intents, notifications, and more — while Drion replaces the system-side implementation behind those contracts.

App-process behavior stays close to real Android: hosted ART executes the APK, bionic-linker behavior is preserved, and framework client-side code remains Android-shaped. A shared system server owns lifecycle, policy, package state, permissions, and other platform services.

## Design principles

- **Wine-like compatibility boundary** — apps see Android; the operating system underneath is Linux
- **Containerless by default** — applications run as per-app sandboxed Linux processes using user and mount namespaces, with no guest kernel or Android system image
- **Real host integration** — audio devices, webcams, sensors, location, clipboard, and notifications pass through to the host
- **Linux-native system services** — Android-facing contracts are preserved while system-side behavior is reimplemented primarily in Rust
- **Pluggable deployment boundaries** — desktop, headless, and Docker Compose profiles share the same compatibility core
- **arm64 on x86_64** — Drion is not tied to a specific translator and can use any compatible Android NativeBridge implementation. Current x86_64 builds use [DigitalisX64](https://github.com/DigitalisX64); Actinis is also developing [Chimera](https://actinis.io/chimera) as its own NativeBridge implementation

## Where Drion fits

Drion is being designed for:

- **Steam Deck, Steam Machine, and other SteamOS devices**
- **Linux phones**
- **Linux desktops** including GNOME, KDE, and Sway environments
- **Embedded and automotive Linux systems**
- **CI and Android instrumented testing**
- **Research, tracing, sandboxing, and forensics** using standard Linux tooling

## Development status

Drion is in **closed alpha** and under active development.

There is no public release yet. The implementation, documentation, supported platforms, and integration paths are evolving as the project moves toward broader availability.

For the current project overview and release updates, see **[actinis.io/drion](https://actinis.io/drion)**.
