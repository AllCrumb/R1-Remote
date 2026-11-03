# R1 Remote

**[Русская версия](docs/README.ru.md)** · [Installation](docs/INSTALLATION.md) · [Safety and limitations](docs/SAFETY.md) · [1.3.0 RC release notes](docs/RELEASE_NOTES_1.3.0_RC.md)

**Control Windows 11 with an Even Realities R1 ring.**

R1 Remote connects the R1 ring to a Windows PC over Bluetooth Low Energy. Swipe gestures scroll pages and lists; other gestures can trigger configurable actions. Neither a phone nor Even G2 glasses are needed during a Windows session.

## Current version

**1.3.0 RC — test build, not a general-availability release.**

Scrolling and reconnecting after a temporary loss of Bluetooth range work on the Windows 11/R1 setup tested so far. The application keeps trying to reconnect instead of turning off control after several timeouts. Testing with other rings and adapters, plus installation and rollback checks, is still in progress.

This GitHub repository currently contains documentation only. **The RC installer is not available on GitHub Releases yet.** Avoid third-party downloads.

## Requirements

- Windows 11, 64-bit
- Bluetooth Low Energy adapter
- Even Realities R1 ring

## Important limitations

- The ring may need to disconnect from G2 while Windows control is active.
- Device-specific pairing details may need to be configured. Unverified G2 addresses must not be treated as factory configuration.
- Windows control remains off until you enable it in the application.
- After manual confirmation, a recovery operation may change the ring's connection targets and interrupt its G2 connection. There is no automatic target restore on exit.
- Out-of-range reconnection uses C1/GATT retries without additional target writes.
- Upgrade, rollback and multi-device testing are still in progress.
- The unsigned installer may trigger Windows security warnings.

## Feedback

Please report reproducible problems in [Issues](https://github.com/AllCrumb/R1-Remote/issues), including Windows build, ring firmware and Bluetooth adapter. Remove MAC addresses, device IDs and personal information from diagnostic logs.

## Disclaimer

This is an independent, unofficial project not affiliated with or endorsed by Even Realities.

This repository contains public documentation, not source code. No open-source license is provided.
