# Core Charge Tracker — User Guide

**Version 1.0**

Stop losing money on forgotten core returns. This guide walks you through every feature of Core Charge Tracker.

---

## Table of Contents

1. [Getting Started](#1-getting-started)
2. [The Dashboard](#2-the-dashboard)
3. [Adding a Core](#3-adding-a-core)
4. [The Three-Stage Workflow](#4-the-three-stage-workflow)
5. [Barcode Scanner Support](#5-barcode-scanner-support)
6. [Printing Core Tags](#6-printing-core-tags)
7. [Driver Manifests](#7-driver-manifests)
8. [Credit Reconciliation](#8-credit-reconciliation)
9. [Warranty Tracking](#9-warranty-tracking)
10. [Archive and Exports](#10-archive-and-exports)
11. [Reports and Charts](#11-reports-and-charts)
12. [Photo Gallery](#12-photo-gallery)
13. [Shelf Audit Mode](#13-shelf-audit-mode)
14. [Settings](#14-settings)
15. [Manager PIN Security](#15-manager-pin-security)
16. [Multi-Station Setup](#16-multi-station-setup)
17. [Cloud Backups](#17-cloud-backups)
18. [Licensing and Upgrades](#18-licensing-and-upgrades)
19. [Troubleshooting](#19-troubleshooting)

---

## 1. Getting Started

Run the installer and launch Core Charge Tracker from your Desktop shortcut. On first launch, the app creates a local database file (`cores.db`) next to the application. No internet connection is required.

You get a **30-day free trial** with all features unlocked. After the trial, the app continues to work with basic features. Professional and Enterprise features can be unlocked with a license key.

> **Tip:** The trial countdown appears in a colored bar at the top of the app. Blue = plenty of time, orange = winding down, red = last few days.

---

## 2. The Dashboard

The dashboard shows three panels:

- **Pending on Shelf** (green) — Total dollar value of cores sitting in your shop. This is money you are owed.
- **Out for Credit** (cyan) — Cores dispatched to vendors where you haven't received credit yet.
- **Warranty Claims** (purple) — Defective parts being tracked separately from normal core returns.

Below the panels you'll see alerts for overdue cores and any lost value from partial credits.

---

## 3. Adding a Core

Click the **Add** tab and fill in:

| Field | Required? | Description |
|-------|-----------|-------------|
| Part Name | Yes | What the part is (Alternator, Caliper, Battery, etc.) |
| RO # | No | Repair order or invoice number |
| Part # | No | Manufacturer part number (or scan with barcode reader) |
| Technician | No | Which tech pulled the part |
| Vendor | Yes | Where the part came from (AutoZone, NAPA, etc.) |
| Core Value ($) | Yes | The dollar amount of the core charge |
| Notes | No | Any extra details (vehicle info, location, etc.) |

Check the **Warranty Claim** box if this is a defective part return rather than a standard core.

Click **Add Core** and it appears on the Pending tab.

---

## 4. The Three-Stage Workflow

Every core follows this path:

**Stage 1: Pending** — The core is on your shelf. The aging clock starts. Yellow warning at the vendor's warning threshold, red alert at the critical threshold.

**Stage 2: Out for Credit** — Click the 🚚 truck icon to dispatch the core. It moves to the OFC tab. The dispatch date is recorded.

**Stage 3: Completed** — Click the 💰 dollar icon when the vendor confirms the credit. Enter the credit memo number and actual amount received. The core moves to the Archive.

**Rejected** — If a vendor refuses a core, click the ❌ icon. It records $0 credit and the full amount as lost value.

---

## 5. Barcode Scanner Support

The **Quick Scan** box in the header works with any USB barcode scanner. Scanners act like keyboards — they type the barcode and press Enter.

- **On the Add tab:** Scanning fills the Part Number field and moves the cursor to Core Value.
- **On Pending, OFC, or Archive tabs:** Scanning filters the list to show matching parts.
- **On the Audit tab:** Scanning records the barcode for the shelf count.

---

## 6. Printing Core Tags

Every core card has a 🖨️ printer icon. Click it to generate a **2x1 inch PDF label** containing:
- Part name
- Vendor
- RO number
- Core value
- Date added
- Technician
- Scannable Code128 barcode

Print it on a thermal label printer (like a Dymo) and stick it on the box.

> **Tip:** Label every core the moment it comes off the car. This makes shelf audits and driver loading much faster.

---

## 7. Driver Manifests

On the Pending tab, check the boxes next to the cores you want to send out. A blue bulk action bar appears. Click **Manifest** to generate a professional PDF with:
- Your shop name, address, and phone
- Numbered list of all selected parts
- Total value
- Signature lines for driver and shop manager

> **Note:** The manifest uses your shop details from Settings. Make sure you've entered your shop name, address, and phone number.

---

## 8. Credit Reconciliation

When you click the 💰 credit button on an Out for Credit core, a popup asks for:

- **Credit Memo #** — The reference number from the vendor's credit statement.
- **Actual Amount Received** — Pre-filled with the expected value. Change it if the vendor paid less.

The app calculates and stores the difference as **Lost Value**. The Archive shows actual credit received and any loss. A **Recovery %** progress bar on each card shows how much of the expected value you got back (green = 95%+, orange = 50-95%, red = below 50%).

---

## 9. Warranty Tracking

Warranty claims follow the same three-stage workflow as cores but are visually distinct with **purple borders** and a **WARRANTY** status pill. They appear in their own dashboard panel and are tracked separately in the Reports charts.

To add a warranty claim, check the **Warranty Claim** checkbox on the Add form.

---

## 10. Archive and Exports

The Archive tab shows all completed and rejected cores. You can:

- **Search** — Filter by part name, vendor, tech, or RO number.
- **Filter by Month** — Use the date dropdown for specific months (useful for tax reporting).
- **Export CSV** — Downloads a spreadsheet with Expected, Actual, and Lost columns.
- **Export PDF** — Branded report with your shop info. Rejected rows highlighted in red, warranty rows in purple.

---

## 11. Reports and Charts

The Reports tab shows three charts:

- **Money by Status** — Bar chart showing Completed, Out for Credit, Pending, Warranty, and Lost values.
- **OFC by Vendor** — Pie chart showing which vendors have the most outstanding credits.
- **Tech Leaderboard** — Horizontal bar chart showing completed and pending value by technician.

Below the charts, you can **email vendor reps** directly with a pre-filled list of outstanding cores.

---

## 12. Photo Gallery

Attach photos when adding or editing a core (receipt photos, part condition, etc.). The **Photos** tab shows all stored images in a grid. Click any photo to open it full-size.

---

## 13. Shelf Audit Mode

The Audit tab lets you verify that every core in the database is actually on the shelf.

1. Click **New Audit** to start a fresh count.
2. Walk to the shelf and scan every box with the barcode scanner (or type part numbers manually).
3. Click **Results** to see which cores are confirmed (✅) and which are missing (❌).

> **Tip:** Run an audit at least once a month. Missing cores are money lost.

---

## 14. Settings

Click the **⚙ Settings** button (top right). Available sections:

- **Shop Details** — Your shop name, address, phone, and email. Appears on all PDF exports.
- **Theme** — Dark or Light mode.
- **Manager PIN** — 4-digit PIN to protect sensitive actions. Set a recovery passphrase.
- **Database Location** — Move the database to a shared network drive.
- **Cloud Backup** — Point to a synced folder for automatic backups.
- **Vendors** — Add, remove, and configure vendors. Set aging thresholds and rep emails.

---

## 15. Manager PIN Security

The PIN protects: deleting cores, confirming credits, rejecting cores, and opening Settings. The PIN is **SHA-256 hashed** and never stored in plaintext.

If you forget your PIN, click **Forgot PIN?** on the prompt and enter your recovery passphrase to set a new one.

---

## 16. Multi-Station Setup

To share the database across multiple computers:

1. Put the database on a shared network drive.
2. On each computer, open Settings → Database → Change. Navigate to the shared file.
3. All stations now read and write to the same database.

SQLite handles concurrent access with WAL mode and a 5-second busy timeout.

---

## 17. Cloud Backups

In Settings, set a **Cloud Backup** folder. Every time the app closes, it silently copies the database with a timestamp. It keeps the last 10 backups automatically.

> **Tip:** Point this to your OneDrive, Dropbox, or Google Drive sync folder. Zero-effort cloud backup.

---

## 18. Licensing and Upgrades

| Tier | Price | Key Features |
|------|-------|--------------|
| **Essentials** | Free | Core tracking, search, scan, labels, aging warnings |
| **Professional** | $99 | PIN security, branded PDFs, photos, tech board, email reps, CSV, manifests |
| **Enterprise** | $249 | Reconciler, warranty, cloud backup, audit, financial charts |

To activate: click **Activate Key** on the trial bar or in Settings. Enter your key and select your tier.

Purchase links:
- [Professional — $99](https://bonziwork.gumroad.com/l/finmtd)
- [Enterprise — $249](https://bonziwork.gumroad.com/l/upbrvw)

---

## 19. Troubleshooting

**App won't start:** Make sure you're running Windows 10 or later. Try Run as Administrator.

**Database locked:** Another station may be writing. Wait a moment and try again.

**Charts not showing:** Complete at least one core so there's data to display.

**Barcode scanner not working:** Ensure the scanner is in USB HID (keyboard) mode. Click inside the Quick Scan box first.

**Photos not in Gallery:** Photos are stored next to the database. If you moved the database, photos need to be in the same location.

**Trial expired unexpectedly:** Don't edit tracker_config.json manually. The trial date is tamper-protected.

**Lost PIN and recovery phrase:** Delete tracker_config.json. This resets the PIN and trial but your core data in cores.db is safe.

---

*Core Charge Tracker — Version 1.0 — 2026*
