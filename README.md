# Force Select+

A modern userscript that restores text selection on websites that try to block it.

## What it does

- Uses a style-stripper CSS override for `user-select`, vendor-prefixed selection rules, pointer events, drag behavior, touch callouts, and selection highlighting.
- Hijacks hostile event listeners for right-click, copy, cut, paste, select-start, drag-start, and common keyboard shortcuts in the capture phase.
- Adds Absolute Mode by patching protected-event `preventDefault()` calls so native browser actions stay available.
- Watches dynamically loaded content so single-page apps stay unlocked.
- Supports open Shadow DOM content created after the userscript starts.
- Includes an optional auto-copy utility: run `ForceSelectPlus.enableAutoCopy()` or set `localStorage.forceSelectPlusAutoCopy = "true"` to copy highlighted text on mouseup.
- Shows a small modern toast when the unlocker is active or auto-copy succeeds.

## Install

Install `Code for it` in a userscript manager such as Tampermonkey, Violentmonkey, or Greasemonkey.
