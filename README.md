# Folio

**A free Windows app for reading, editing and signing PDFs, editing Word, Excel and PowerPoint files, and writing LaTeX.**
Everything runs on your own computer: no account, no uploads, no subscription.

### ⬇️ [Download the latest version](https://github.com/Sunless19/folio-releases/releases/latest)

This repository only hosts the downloads. The source code is not public.

---

## Install

From the [latest release](https://github.com/Sunless19/folio-releases/releases/latest) download **one** of:

- **`Folio-<version>-Setup.exe` — recommended.** Run it and click *Install*. Installs Folio for your user (no admin
  rights needed), adds Desktop and Start-menu shortcuts, and appears in *Settings → Apps* so you can uninstall it like
  any other app. **Folio updates itself**: when a new version is out it offers *Update now* (your settings and signatures
  are kept).
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
- **Word** (.docx): type straight on the page, bold/italic/underline, font size, colour, highlight, headings, pictures, page breaks, find & replace, word count
- **PowerPoint** (.pptx): a PowerPoint-style canvas — move and resize anything, insert text boxes, shapes, pictures and new slides, format text and shapes, slideshow (F5)
- Start a blank Word document, Excel workbook or PowerPoint presentation straight from the home screen
- Only what you change is touched — formatting, images and charts elsewhere stay exactly as they were
- Unsaved changes survive a crash: reopen the file and click *Restore them*
- "Save as PDF" via print

**LaTeX**
- Editor with highlighting, snippets, maths symbols and templates (article, report, letter, slides, CV)
- Instant built-in preview — works offline with nothing to install
- Full LaTeX (TikZ, any package) with MiKTeX / TeX Live, or one click to install the Tectonic engine
- Errors listed by line, export PDF

**Comfort**
- Reopens your files where you left off, and recovers unsaved edits after a crash
- Command palette (Ctrl+K), keyboard shortcuts (press **?**), tabs, dark mode, night-reading mode, presentation mode (F5)
- Optional auto-save, and a reload prompt when another program changes a file you have open
- Recent files with thumbnails; pin favourites to the top
- PDF outline (bookmarks) panel; export PDF pages as PNG/JPG

## Use Folio from Claude

Folio includes an **MCP server**, so Claude (Claude Code or Claude Desktop) can work with your documents through
Folio — like it does with LibreOffice: read PDFs, Word, Excel and PowerPoint files, look at pages, convert to PDF or
images, fill forms, add text, check marks or your saved signature, merge/split, change Excel cells or replace text in
Word/PowerPoint, check digital signatures, compile LaTeX, and open a file in Folio for you to review.

In Folio open Settings (⚙) → *Use Folio from Claude* → **Copy command** and paste it in a terminal (Claude Code), or
**Copy config** and paste it into Claude Desktop's `claude_desktop_config.json`. For Claude Code that is:

```
claude mcp add --scope user folio -- "%LOCALAPPDATA%\Programs\Folio\Folio.exe" --mcp
```

Everything still runs on your computer; Folio only reads and writes the files Claude names.

## Privacy

Folio never sends your documents anywhere. It runs a private server on `127.0.0.1` that only the Folio window can use.
The only thing it asks the internet for is whether a newer version exists on this page (you can turn that off in Settings).

## Licenses

Folio is built on open-source components (PDF.js, pdf-lib, SheetJS, docx-preview, pywebview and others).
Their licenses are in `THIRD_PARTY_NOTICES.txt`, included in every download and in this repository.
