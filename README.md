# Force Select+

A modern, iOS-ready userscript that restores text selection on websites that try to block it.

## What it does

- Uses an iOS-friendly style-stripper CSS override for `user-select`, vendor-prefixed selection rules, pointer events, drag behavior, tap highlighting, touch callouts, and selection highlighting.
- Hijacks hostile event listeners for right-click, copy, cut, paste, select-start, drag-start, touch, pointer, and common keyboard shortcuts in the capture phase.
- Adds Absolute Mode by patching protected-event `preventDefault()` calls so native browser actions stay available.
- Re-boots during page lifecycle events and watches dynamically loaded content so iOS Safari, restored tabs, and single-page apps stay unlocked.
- Supports open Shadow DOM content created after the userscript starts.
- Includes an optional auto-copy utility with a Clipboard API path and an `execCommand` fallback: run `ForceSelectPlus.enableAutoCopy()` or set `localStorage.forceSelectPlusAutoCopy = "true"` to copy highlighted text on mouseup or touchend.
- Shows a small modern toast when the unlocker is active or auto-copy succeeds.

## Install

Install `Code for it` in a userscript manager such as Tampermonkey, Violentmonkey, or Greasemonkey.
