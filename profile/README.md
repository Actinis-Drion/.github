<div align="center">

# Drion

### Android apps on Linux — without an Android VM.

Drion is an Android compatibility platform for Linux. It runs Android APKs directly on the Linux host without booting a complete Android virtual machine or requiring a full Android system image.

[Documentation](https://github.com/Actinis-Drion/docs)

</div>

---

## What is Drion?

Drion preserves the Android interfaces applications expect while replacing system-side behavior with Linux-native components.

The project is designed to make Android applications feel like part of the host system rather than applications running inside a separate Android environment.

### Project goals

- Run Android applications as first-class Linux applications
- Integrate with native Linux windows, input, notifications, clipboard, and desktop services
- Provide hardware-accelerated graphics
- Preserve Android application compatibility without running a complete Android OS
- Share the same core runtime across multiple Linux-based platforms

## How it works

At a high level, Drion combines:

- **Hosted ART** for executing Android application code
- **Linux-native system services**, primarily implemented in Rust
- **Android compatibility layers** for framework and platform contracts
- **Native host integration** for windows, input, graphics, notifications, clipboard, and other desktop functionality

## Status

Drion is under active development.

The main implementation is not public yet. Public technical documentation, architecture notes, platform information, and integration guides will be published in this organization as they become available.

## Resources

- [Public documentation](https://github.com/Actinis-Drion/docs)
- [Actinis-Drion organization](https://github.com/Actinis-Drion)
