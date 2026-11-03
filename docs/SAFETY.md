# Safety and limitations / Безопасность и ограничения

R1 Remote uses an unofficial, reverse-engineered Bluetooth LE integration with the Even Realities R1 ring. This is an experimental integration, **not an official Even Realities feature**.

## Connection safety

- The ring can have an active connection to G2. A Windows control session may require leaving that connection.
- Historical application journals such as `targets=open` do **not** prove the ring is currently disconnected from G2.
- The application does not automatically restore G2 targets on exit. Reconnecting to G2 worked during testing with one ring, but it has not been checked with every firmware version.
- After you confirm enabling control, a recovery attempt may write connection targets once if C1 role setup times out twice. This can break the G2 connection.
- When the ring is out of range, Windows reconnection retries use C1/GATT; they do not require another target write.
- Manual G2 Bluetooth addresses are supplied by the user; their format can be checked, but they are not a verified readout of original device NVM.
- An incorrect address, wrong order or wrong ring/device binding can prevent a successful reconnection.

## Do not

- Rewrite saved MAC addresses simply because a historical journal says `open`.
- Delete or edit per-device journals, saved DPAPI state or target ledgers to force a connection.
- Run multiple BLE control/probe applications against the same ring during troubleshooting.
- Assume that a green CI test means a particular physical ring/firmware was tested.

## Release Candidate limitations

- Testing so far covers one R1/Windows setup, not a representative range of rings and firmware versions.
- Negative cases such as lost pairing, an interrupted connection or interrupted target writes are not fully qualified.
- Installation, in-place updates, rollback and uninstall across a range of existing builds remain under qualification.
- The RC installer is not Authenticode-signed; Windows may show a security warning.
- Advanced application-specific profiles and input mapping may be experimental.

## Security and diagnostics

Logs and support packages can contain sensitive device identifiers, Bluetooth addresses, Windows account paths and configuration context. **Remove those values before filing a public GitHub issue.** Do not upload DPAPI blobs or private keys.

If G2 connectivity is lost, do not repeatedly attempt recovery writes. Preserve logs and stop until the specific hardware state is understood.

[Back to project page](../README.md)
