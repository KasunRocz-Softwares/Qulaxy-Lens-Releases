# Qulaxy Lens — releases

Qulaxy Lens explains what uses storage and system resources on Windows 11, with evidence,
and never claims more than it measured. This repository holds **only release files**; the
source code is private.

## Download

Get the newest `QulaxyLens_<version>_x64-setup.exe` from
[Releases](https://github.com/KasunRocz-Softwares/Qulaxy-Lens-Releases/releases/latest).
It installs per user (no administrator rights).

Each release contains:

| File | Purpose |
|---|---|
| `QulaxyLens_<version>_x64-setup.exe` | Installer |
| `QulaxyLens_<version>_x64-setup.exe.sig` | Update signature (minisign), checked by the app before an update runs |
| `latest.json` | Update manifest read by the app |
| `SHA256SUMS.txt` | Checksums |

Check a download in PowerShell:

```powershell
Get-FileHash .\QulaxyLens_0.5.1_x64-setup.exe -Algorithm SHA256
```

and compare with `SHA256SUMS.txt`.

## Updates

From 0.5.1 the app can update itself (Settings → Updates). It contacts this repository only
when you click *Check now* or turn on the automatic check. An installer whose signature does
not match the key built into the app is refused. The installer is not yet Authenticode-signed,
so Windows SmartScreen may ask for confirmation on first install.
