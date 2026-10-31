# Folio

**A free Windows app for reading, editing and signing PDFs — and for editing Word, Excel and PowerPoint files.**
Everything runs on your own computer: no account, no uploads, no subscription.

### ⬇️ [Download the latest version](https://github.com/Sunless19/folio-releases/releases/latest)

This repository only hosts the downloads. The source code is not public.

---

## Install

From the [latest release](https://github.com/Sunless19/folio-releases/releases/latest) download **one** of:

- **`Folio-<version>-Setup.exe` — recommended.** Run it and click *Install*. Installs Folio for your user (no admin
  rights needed), adds Desktop and Start-menu shortcuts, and appears in *Settings → Apps* so you can uninstall it like
  any other app. To update later, run the new Setup — your settings and signatures are kept.
- **`Folio-<version>-win-x64.exe`** — a single portable file: just double-click it, nothing gets installed.
- **`Folio-<version>-win-x64.zip`** — a portable folder: extract it and run `Folio.exe`.

> **"Windows protected your PC"?** Folio isn't code-signed yet, so SmartScreen warns about any new download.
> Click **More info → Run anyway**. You can check the download against the SHA-256 shown in the release notes.

**Requirements:** Windows 10 or 11 (64-bit). Folio uses the Microsoft Edge WebView2 runtime, which ships with Windows 11 and current Windows 10.

**To open files with Folio by double-clicking:** in Folio open Settings (⚙) → *Open files with Folio* → **Add**. Windows' *Default apps* page opens on Folio — pick the file types (PDF, Word, Excel, PowerPoint, CSV, images) you want it to open.

**Uninstall:** *Settings → Apps → Folio → Uninstall* (if you used Setup), or just delete the portable file/folder. Settings and the signature library live in `%APPDATA%\Folio`; the uninstaller asks whether to delete them.

## What it does

**PDF editing**
- Change existing text on the page, add text (with full Unicode, e.g. ă â î ș ț), highlight, underline, strikethrough
- Draw, shapes and arrows, check marks, dates, sticky-note comments, images
- White-out that matches the paper colour of scans — great for hiding scanner watermarks — with **Apply to all pages**
- Fill in PDF forms
- Reorder, rotate, delete, duplicate, insert and extract pages; combine several PDFs/images into one
- **Ctrl+S saves straight back into the original file**

**Signatures**
- Draw, type, or photograph your signature; it's kept in your own signature library
- Lift a handwritten signature off any scanned document and save it as a transparent PNG
- Check digital signatures: who signed, when, and whether the document was changed afterwards — with a green ✓ / red ✗ on the signature, like Adobe Reader

**Office files**
- **Excel** (.xlsx, .xls, .csv): edit cells and formulas with live results, AutoSum, fill down/right, number formats, Sum/Average/Count of selections
- **Word** (.docx): type straight on the page, bold/italic/underline, size, colour, highlight, headings, page breaks, find & replace, word count
- **PowerPoint** (.pptx): a PowerPoint-style canvas — move and resize anything, insert text boxes, shapes, pictures and new slides, format text and shapes, slideshow (F5)
- Only what you change is touched — formatting, images and charts elsewhere stay exactly as they were
- Unsaved changes survive a crash: reopen the file and click *Restore them*
- "Save as PDF" via print

**Comfort**
- Reopens your files where you left off, and recovers unsaved edits after a crash
- Command palette (Ctrl+K), keyboard shortcuts (press **?**), tabs, dark mode, night-reading mode, presentation mode (F5)

## Privacy

Folio never sends your documents anywhere. It runs a private server on `127.0.0.1` that only the Folio window can use.

## Licenses

Folio is built on open-source components (PDF.js, pdf-lib, SheetJS, docx-preview, pywebview and others).
Their licenses are in `THIRD_PARTY_NOTICES.txt`, included in every download and in this repository.
