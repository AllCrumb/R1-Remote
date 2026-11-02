# R1 Remote

**[Русская версия](docs/README.ru.md)** · [Installation](docs/INSTALLATION.md) · [Safety and limitations](docs/SAFETY.md) · [1.3.0 RC release notes](docs/RELEASE_NOTES_1.3.0_RC.md)

**Unofficial Windows 11 controller for the Even Realities R1 smart ring.**

R1 Remote connects the ring directly to Windows using Bluetooth Low Energy. It supports ring-gesture scrolling and experimental configurable controls. A phone or Even G2 glasses are not required during Windows control.

## Project status

**1.3.0 Release Candidate / Preview — not a GA release.**

The primary Windows control and return-to-G2 workflow has been tested by the project operator on one hardware setup. Broad compatibility, safe updates and recovery scenarios have not yet completed release qualification.

**No approved public installer or source-code release is published here yet.** Do not install binaries from unofficial mirrors.

## Requirements

- Windows 11, 64-bit
- Bluetooth Low Energy adapter
- Even Realities R1 ring

## Important limitations

- The ring may need to disconnect from G2 while Windows control is active.
- Device-specific pairing details may need to be configured. Unverified G2 addresses must not be treated as factory configuration.
- Safe startup disables Windows controls until explicitly enabled.
- The current RC has not completed multi-device hardware or upgrade/rollback certification.
- The unsigned installer may trigger Windows security warnings.

## Feedback

Please report reproducible problems in [Issues](https://github.com/AllCrumb/R1-Remote/issues), including Windows build, ring firmware and Bluetooth adapter. Remove MAC addresses, device IDs and personal information from diagnostic logs.

## Disclaimer

This is an independent, unofficial project not affiliated with or endorsed by Even Realities.

This repository currently contains public project documentation only. No open-source license has been granted.
