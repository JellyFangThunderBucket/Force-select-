# Force Select+

A modern, iOS-ready userscript that restores text selection on websites that try to block it and adds a touch-friendly Command Center.

## What it does

- Uses an iOS-friendly style-stripper CSS override for `user-select`, vendor-prefixed selection rules, pointer events, drag behavior, tap highlighting, touch callouts, and selection highlighting.
- Hijacks hostile event listeners for right-click, copy, cut, paste, select-start, drag-start, touch, pointer, and common keyboard shortcuts in the capture phase, including Cmd/Ctrl+F search.
- Adds Absolute Mode by patching protected-event `preventDefault()` calls so native browser actions stay available.
- Re-boots during page lifecycle events and watches dynamically loaded content so iOS Safari, restored tabs, and single-page apps stay unlocked.
- Supports open Shadow DOM content created after the userscript starts.
- Adds a floating **FS+ Command Center** with buttons for Unlock Page, Copy Selection, Copy Article Text, Copy Image Text, Nuke Overlays, Auto-Copy On/Off, Hide/Show Toasts, Pause This Tab, and Disable On This Site.
- Includes an optional auto-copy utility with a Clipboard API path and an `execCommand` fallback: run `ForceSelectPlus.enableAutoCopy()` or use the Command Center to copy highlighted text on mouseup or touchend.
- Adds reader-mode extraction to copy article-like page text from `article`, `main`, paragraphs, headings, and list items.
- Adds overlay softening for full-page fixed overlays that block selection with high z-index layers.
- Adds image text-hint copying from image `alt`, `title`, and `aria-label` attributes.
- Adds per-site disable using `localStorage.forceSelectPlusDisabledSites` for sites that do not behave well with forced pointer/selection behavior.
- Shows a small modern toast when the unlocker is active, commands run, or auto-copy succeeds.

## Install

Install `Code for it` in a userscript manager such as Tampermonkey, Violentmonkey, Greasemonkey, or an iOS Safari userscript extension.
