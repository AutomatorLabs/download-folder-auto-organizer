# Download Folder Auto Organizer

Download Folder Auto Organizer is a clean, offline-first Mac desktop utility for turning a messy Downloads folder into clear, predictable subfolders.

It scans the selected folder, previews every planned move, and only organizes files after you click **Organize Files**.

## Main Features

- Select any folder, with `~/Downloads` as the default.
- Preview planned moves before anything changes.
- Sort files into PDFs, Images, Screenshots, Videos, Audio, Documents, Spreadsheets, Archives, Installers, Code, Old Files, and Other.
- Detect screenshots using common filename patterns.
- Move files that have not been modified for a configurable number of days.
- Never delete files.
- Never overwrite files.
- Undo the latest cleanup session.
- Keep a local activity history in `data/history.json`.
- Dark, focused desktop UI built with PySide6.

## Run Locally

```bash
cd "/Users/tim/Desktop/MICRO SAAS/Download Folder Auto Organizer"
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python main.py
```

## Safety Notes

- The app does not move anything on launch.
- The app only scans after you click **Scan**, and only moves files after you click **Organize Files**.
- The app only scans files directly inside the selected folder.
- The app does not recursively scan subfolders in V1.
- The app does not move folders.
- Existing destination files are protected by safe unique names such as `file (1).pdf`.
- Undo restores files from the latest cleanup session when possible.

## Current V1 Limitations

- Only direct files in the selected folder are scanned.
- Undo only applies to the latest cleanup session that has not already been undone.
- Empty category folders are not removed.
- The app is not packaged or notarized yet.

## Future Roadmap

- Packaging as a signed macOS app.
- More file categories and editable rules.
- Recursive cleanup mode with strong safeguards.
- Before-and-after cleanup reports.
- Scheduled reminders.
- Safer handling for very large files and external drives.
- In-app license activation when payment integration is added.
