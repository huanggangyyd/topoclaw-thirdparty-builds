# TopoClaw Third-Party Builds

Unofficial prebuilt packages for TopoClaw.

## Disclaimer

- This folder is maintained by an independent third party.
- These packages are NOT official TopoClaw releases.
- They are not affiliated with or endorsed by the official maintainers.

## Included Files

- `TopoMobile-2.1.0.apk` (mobile/Android package)
- `TopoDesktop-2.1.0.exe` (desktop/Windows installer)
- `SHA256SUMS.txt` (checksum list for integrity verification)

## Download

Download package files from the Release assets:

- `TopoMobile-2.1.0.apk`
- `TopoDesktop-2.1.0.exe`

## Verification (Optional but Recommended)

Checksum verification is optional, but recommended for integrity checks.

1. Download `SHA256SUMS.txt`.
2. Compute local SHA-256 hash.
3. Compare local hashes with the published checksums.

### Verify on Windows (PowerShell)

```powershell
Get-FileHash ".\TopoDesktop-2.1.0.exe" -Algorithm SHA256
Get-FileHash ".\TopoMobile-2.1.0.apk" -Algorithm SHA256
```

### Verify on macOS/Linux

```bash
sha256sum TopoDesktop-2.1.0.exe
sha256sum TopoMobile-2.1.0.apk
```

## Why checksums matter

Checksums do not block downloads. They help users verify that:

- the file is complete (not corrupted), and
- the file was not modified after release.

## Upgrade and Re-Authentication Guidance

In most cases, if you upgrade in place with the same signing identity and package/install identity, re-authentication is not required.
However, for a safer and more predictable rollout, it is reasonable to re-authenticate once after upgrade.

### When re-authentication is recommended

- Connection fails after upgrade (service link, scan binding, or session issues)
- Android signing key has changed
- Windows app data context changed (new user profile, OS reinstall, or app data cleanup)
- `customer_service` auth policy or related configuration has changed

### Conservative workflow (recommended)

1. Back up key settings (service URL, model settings, and other important options).
2. Upgrade Android and Windows apps in place.
3. Sign out on desktop and remove old device binding if your UI supports unbind.
4. Re-bind by scanning the desktop QR code from the mobile app.
5. Re-enter and verify relay service URL connectivity.
6. Run one end-to-end task to confirm request and response are both healthy.

