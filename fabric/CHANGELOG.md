# Changelog

## 1.1.0

### Summary

This update fixes bulk crafting so it stays strictly locked to the item currently selected in the crafting terminal.

### Fixed

- Fixed bulk crafting continuing into other items when the terminal result changed after the requested craft
- Fixed cases where `x64` could unintentionally craft follow-up items, such as vanilla chests or planks, after crafting a modded chest
- Fixed bulk craft buttons so they now stop as soon as the displayed result is no longer the same item

### Notes

- `x1`, `x4`, `x8`, and `x64` now only craft the currently selected result
- If the terminal result changes after crafting, the player must press the button again intentionally

## 1.0.0

### Summary

This update adds a first crafting template system directly into Tom's Storage crafting terminal, with a simple and clean interface designed to stay stable.

### Added

- Added a dedicated button in the crafting terminal to open the template list
- Added a template screen showing saved crafts
- Added saving of the current craft as a template
- Added template loading by double-click
- Added template deletion with confirmation
- Added client-side JSON persistence for templates

### Improved

- Improved visual integration of the templates button into the terminal button column
- Improved the templates UI by keeping it simplified for stability and readability
- Improved focus on the essentials with result icon + template name display
- Improved screen closing with a discreet X button instead of a heavier visible button

### Notes

- This V1 of the template system is considered validated
- A future small update may add multi-selection for bulk deletion
- A future template grouping system may also be explored if the interface stays simple
