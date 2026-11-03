# Installation / Установка R1 Remote

**Version:** 1.3.0 RC1 (pre-release). Download the installer from the [official GitHub release](https://github.com/AllCrumb/R1-Remote/releases/tag/v1.3.0-rc.1).

## Before installing

- Windows 11 (64-bit), with a working Bluetooth Low Energy adapter.
- Even Realities R1 ring.
- Review [Safety and limitations](SAFETY.md) before changing connection settings.

## Download and integrity

Download `R1Remote-Setup-1.3.0-RC.exe` from the [1.3.0 RC1 release](https://github.com/AllCrumb/R1-Remote/releases/tag/v1.3.0-rc.1). Compare its SHA-256 with the value in the [release notes](RELEASE_NOTES_1.3.0_RC.md).

PowerShell:

```powershell
Get-FileHash -LiteralPath "$HOME\Downloads\R1Remote-Setup-1.3.0-RC.exe" -Algorithm SHA256
```

Expected SHA-256: `7AEEEB5B0F5E74614B1085D32D66E7110C1632D116812C0FB06A585009594599`. Verify the name in `SHA256SUMS.txt` matches the actual downloaded asset; a matching hash with a different filename is not a valid filename-based verification.

## Finding the two G2 Bluetooth MAC addresses

Use the **official Even mobile app**, not a Bluetooth scanner or the R1 ring's MAC address:

1. Open Even on the phone and select your **Even G2** glasses.
2. Open **Glasses info** (the glasses information screen).
3. Locate **Bluetooth MAC**. The app shows **two separate addresses**, one above the other.
4. In R1 Remote's **Configure G2** form, enter the **upper address in G2 #1** and the **lower address in G2 #2**. Copy all six hexadecimal byte pairs, including the colons; do not swap the lines.
5. Double-check both values before saving. Do not copy the model number, serial number, phone address or R1 ring address.

The Even screen does **not** label these values as left/right. Their display order is not proof of the order of the ring's original NVM target slots. R1 Remote saves the manually supplied pair for the selected ring, but it cannot authenticate that pair as the ring's factory configuration. Incorrect values can prevent reconnecting to G2 if a target-restoration operation is needed.

Keep screenshots containing real Bluetooth addresses or serial numbers private. Interface labels may differ slightly with the language/version of the Even app.

## First launch

1. Install on Windows 11 x64. The installer only upgrades a small set of known builds and refuses to overwrite an unrecognized version. Full upgrade and rollback tests are still in progress.
2. Open R1 Remote. Windows control should be **Disabled** until explicitly enabled.
3. Select the intended R1 device. Do not assume another ring with a similar Bluetooth name is yours.
4. If asked for two G2 addresses, copy them from **Even → Glasses info → Bluetooth MAC** as described above. Keep the displayed order (upper → G2 #1; lower → G2 #2). The addresses are not a confirmed copy of the ring's original NVM targets.
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
