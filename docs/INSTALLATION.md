# Installation / Установка R1 Remote

**Version:** 1.3.0 RC. The installer is not yet available as a public GitHub download.

## Before installing

- Windows 11 (64-bit), with a working Bluetooth Low Energy adapter.
- Even Realities R1 ring.
- Review [Safety and limitations](SAFETY.md) before changing connection settings.

## Download and integrity

When the RC is published, download it from [GitHub Releases](https://github.com/AllCrumb/R1-Remote/releases). Check the SHA-256 against the checksum listed for that exact file.

PowerShell:

```powershell
Get-FileHash -LiteralPath "$HOME\Downloads\R1Remote-Setup-1.3.0-Clean-RC.exe" -Algorithm SHA256
```

This is the current RC installer filename. Use the checksum shown for the published file, not one from an older build. **No installer is attached to this repository yet.**

## First launch

1. Install on Windows 11 x64. The installer only upgrades a small set of known builds and refuses to overwrite an unrecognized version. Full upgrade and rollback tests are still in progress.
2. Open R1 Remote. Windows control should be **Disabled** until explicitly enabled.
3. Select the intended R1 device. Do not assume another ring with a similar Bluetooth name is yours.
4. If the program requests connection information for G2, verify it carefully. Manually entered addresses are **not confirmed factory NVM values**.
5. Follow the application's prompt before enabling Windows control. Verify scrolling in both directions.
6. Disable Windows control and verify that the ring reconnects to G2. **Do not force a restore while G2 is already working.**

## Troubleshooting

- If the ring is connected to G2 and cannot be used by Windows, disconnect it from G2 first; do not bypass safety checks.
- If the ring goes out of range, leave R1 Remote running. It should reconnect after the ring returns; after repeated connection failures, retry attempts are spaced about 10 seconds apart.
- If the application reports an ambiguous state, stop and gather a sanitized diagnostic record. Do **not** delete target journals or DPAPI files or substitute addresses.
- If the ring fails to reconnect to G2, stop retrying writes and seek device-specific support.
- Do not forcibly terminate the process during device writes, installation or removal.

**This Release Candidate has not completed installation, upgrade and rollback testing across different Windows PCs.**

[Back to project page](../README.md)
