# R1 Remote 1.3.0 RC — Release Notes (Draft)

**Status:** Preview / Release Candidate — **not GA**.

**Publication status:** Documentation draft only. **No public release asset or tag has been published from this repository.**

## Highlights

- Windows 11 control via Even Realities R1 Bluetooth LE connection.
- Ring gesture-based scrolling and experimental customizable actions.
- Native Windows interface with selected-ring connection flow.
- RU / EN / FR / DE interface support.
- Safer first launch: control starts Disabled until user action.
- Historical connection journals no longer force a G2 restore workflow or block basic application file maintenance.
- No mandatory automatic writing of saved G2 targets during normal shutdown.
- The installer icon was adjusted to match the main R1 Remote application icon.

## Validation so far

The project operator reported successful Windows scrolling and return to Even G2 without forced recovery on one physical setup. Windows CI builds and isolated source/self-tests passed for the installer candidate, including icon resource checks.

**These tests do not establish general device compatibility, full installer update/rollback acceptance or signed release provenance.**

## Known limitations

- Multiple independent R1 units, firmware versions and BLE adapter combinations are not yet fully tested.
- Manual G2 addresses are not a verified copy of the device's factory target storage.
- Interrupted target writes, lost bond, invalid identity and other hardware-negative scenarios need more live testing.
- In-place upgrades and complete rollback/uninstall scenarios remain under qualification.
- No Authenticode signature; Windows SmartScreen warnings are possible.
- Some application-specific profiles and configurable actions remain experimental.

## Installer and SHA-256

The final public asset must be attached **only after a separate release approval**. Its exact version, immutable source revision, size and SHA-256 must be independently verified and listed here when released.

**Do not treat development CI artifacts as an official public release.**

## Disclaimer

R1 Remote is an independent unofficial project, not affiliated with or endorsed by Even Realities.

[Installation](INSTALLATION.md) · [Safety](SAFETY.md) · [Project page](../README.md)
