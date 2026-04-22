# TopoClaw Third-Party Builds

Unofficial prebuilt packages for TopoClaw.

## Disclaimer

- This folder is maintained by an independent third party.
- These packages are NOT official TopoClaw releases.
- They are not affiliated with or endorsed by the official maintainers.

## Included Files

- `TopoClaw-2.1.0.apk` (mobile/Android package)
- `TopoClaw-2.1.0.exe` (desktop/Windows installer)
- `SHA256SUMS.txt` (checksum list for integrity verification)

## Download

Download package files from the Release assets:

- `TopoClaw-2.1.0.apk`
- `TopoClaw-2.1.0.exe`

## Verification (Optional but Recommended)

Checksum verification is optional, but recommended for integrity checks.

1. Download `SHA256SUMS.txt`.
2. Compute local SHA-256 hash.
3. Compare local hashes with the published checksums.

### Verify on Windows (PowerShell)

```powershell
Get-FileHash ".\TopoClaw-2.1.0.exe" -Algorithm SHA256
Get-FileHash ".\TopoClaw-2.1.0.apk" -Algorithm SHA256
```

### Verify on macOS/Linux

```bash
sha256sum TopoClaw-2.1.0.exe
sha256sum TopoClaw-2.1.0.apk
```

## Why checksums matter

Checksums do not block downloads. They help users verify that:

- the file is complete (not corrupted), and
- the file was not modified after release.

