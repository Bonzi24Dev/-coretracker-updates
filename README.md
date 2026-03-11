# -coretracker-updates
# Core Charge Tracker

A desktop application for auto repair shops to track unreturned part cores (alternators, batteries, brake calipers) and stop losing money to forgotten returns.

## What It Does

- Track cores from shelf to vendor to credit received
- Three-stage workflow: Pending → Out for Credit → Completed
- Giant dashboard showing exactly how much money is sitting on your shelf
- Per-vendor aging warnings (yellow at 14 days, red at 30)
- USB barcode scanner support for fast part lookups
- Thermal label printing (2x1 Dymo tags with barcodes)
- Photo attachments for receipts and part condition
- Driver manifests with signature lines
- Vendor statement reconciliation (CSV upload)
- Warranty claim tracking (purple-coded)
- Technician leaderboard
- One-click email to vendor reps
- CSV and branded PDF exports
- Manager PIN security with recovery passphrase
- Multi-station support (shared network database)
- Automated local and cloud backups
- Shelf audit / cycle count mode
- Dark and light mode

## Tech Stack

- Python + CustomTkinter
- SQLite (local, no internet required)
- Matplotlib (charts)
- ReportLab (PDF generation)
- PyInstaller (standalone .exe)

## Download

Get the latest version from the [Releases](https://github.com/Bonzi24Dev/-coretracker-updates/releases) page.

## Version

Current release: 1.0
