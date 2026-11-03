# R1 Remote 1.3.0 RC — Release notes

**Status:** Release Candidate (test build), not GA. No installer is available on GitHub Releases yet.

## Highlights

- Windows 11 control via Even Realities R1 Bluetooth LE connection.
- Ring gesture-based scrolling and configurable actions.
- Automatic C1/GATT reconnect after the ring goes out of Bluetooth range. After five failed connections, further attempts are spaced about 10 seconds apart; Windows control remains enabled.
- Native Windows interface with selected-ring connection flow.
- RU / EN / FR / DE interface support.
- Windows control stays disabled until explicitly enabled in the app.
- Recovery after repeated C1 role timeouts can make one C2 target write per process, only after manual confirmation. The app does not automatically restore G2 targets on exit.
- Historical connection journals no longer force a G2 restore workflow or block basic application file maintenance.
- No mandatory automatic writing of saved G2 targets during normal shutdown.
- The installer icon was adjusted to match the main R1 Remote application icon.

## Validation so far

Scrolling and reconnection after temporary Bluetooth loss work with an R1 on the Windows 11 system tested so far. Return to G2 has also worked in earlier testing, but repeated switching on this exact RC still needs checking. The Windows build passed 33 native tests, installer compilation, archive checks and independent SHA-256 verification.

**This is not a compatibility test across different rings, firmware versions or Bluetooth adapters.**

## Known limitations

- Multiple independent R1 units, firmware versions and BLE adapter combinations are not yet fully tested.
- Manual G2 addresses are not a verified copy of the device's factory target storage.
- Interrupted target writes, lost bond, invalid identity and other hardware-negative scenarios need more live testing.
- In-place upgrades and complete rollback/uninstall scenarios remain under qualification.
- No Authenticode signature; Windows SmartScreen warnings are possible.
- Some application-specific profiles and configurable actions remain experimental.

## Installer and SHA-256

Current tested candidate (not yet uploaded to GitHub):

- Installer: `R1Remote-Setup-1.3.0-Clean-RC.exe`
- Installer SHA-256: `7AEEEB5B0F5E74614B1085D32D66E7110C1632D116812C0FB06A585009594599`
- Application SHA-256: `AA2507681C296F96FACA0BFEEF70579721BDC8B77CFEF65EEF986966E1D7DDD3`

These checksums identify this specific build; they are not download links. Any newer build needs its own checksum.

## Disclaimer

R1 Remote is an independent unofficial project, not affiliated with or endorsed by Even Realities.

[Installation](INSTALLATION.md) · [Safety](SAFETY.md) · [Project page](../README.md)
