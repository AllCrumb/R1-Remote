# Installation / Установка R1 Remote

**Status:** Guidance for a future public **1.3.0 RC pre-release**, not an announcement that a public installer exists.

## Before installing

- Windows 11 (64-bit), with a working Bluetooth Low Energy adapter.
- Even Realities R1 ring.
- Review [Safety and limitations](SAFETY.md) before changing connection settings.

## Download and integrity

When an **official pre-release is approved**, download its installer only from the [GitHub Releases page](https://github.com/AllCrumb/R1-Remote/releases). Verify the installer SHA-256 against the value published for **that exact release asset**.

PowerShell:

```powershell
Get-FileHash -LiteralPath "$HOME\Downloads\R1Remote-Setup-1.3.0-Clean-RC.exe" -Algorithm SHA256
```

The filename above is illustrative. Do not use an old checksum for a newer file. **There is no approved public asset attached yet.**

## First launch

1. Install only on a supported clean Windows 11 setup. **In-place upgrade from older native builds is not qualified yet.**
2. Open R1 Remote. Windows control should be **Disabled** until explicitly enabled.
3. Select the intended R1 device. Do not assume another ring with a similar Bluetooth name is yours.
4. If the program requests connection information for G2, verify it carefully. Manually entered addresses are **not confirmed factory NVM values**.
5. Follow the application's prompt before enabling Windows control. Verify scrolling in both directions.
6. Disable Windows control and verify that the ring reconnects to G2. **Do not force a restore while G2 is already working.**

## Troubleshooting

- If the ring is connected to G2 and cannot be used by Windows, release the previous connection first; do not bypass safety checks.
- If the application reports an ambiguous state, stop and gather a sanitized diagnostic record. Do **not** delete target journals or DPAPI files or substitute addresses.
- If the ring fails to reconnect to G2, stop retrying writes and seek device-specific support.
- Do not forcibly terminate the process during device writes, installation or removal.

**For this Release Candidate, installation, upgrades and rollback have not been broadly validated on unrelated Windows hosts.**

[Back to project page](../README.md)
