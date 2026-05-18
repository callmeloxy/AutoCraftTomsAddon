# Changelog

## 1.6.0

### Summary

This update adds multi-selection support for templates, allowing multiple templates to be deleted or assigned to a group at once.

### Added

- Added multi-selection for templates using `Ctrl + Click`
- Added support for deleting multiple selected templates at once
- Added support for assigning multiple selected templates to a group at once
- Added a dedicated `Group Options` button to open group management
- Added support for deleting empty custom groups from the group options screen

### Improved

- Improved the template screen button layout
- Improved button readability by separating template actions and group actions into two rows
- Improved group management access by making `Group Options` available even when no template is selected
- Improved the group name field placeholder behavior so it disappears as soon as text is entered
- Improved safety around rename behavior: templates can only be renamed when a single template is selected

### Notes

- `Ctrl + Click` is used for multi-selection in this version
- Double-click still loads a single template as before
- Rename is disabled when multiple templates are selected
- Group assignment now supports one or multiple selected templates

## 1.5.0

### Summary

This update adds template groups, making it easier to organize saved crafting templates.

### Added

- Added template groups to the template screen
- Added a group filter with:
  - All
  - Ungrouped
  - Custom groups
- Added a group management screen
- Added support for creating custom groups
- Added support for renaming custom groups
- Added support for deleting custom groups
- Added support for assigning a template to a group
- Added a clearer group name field placeholder

### Improved

- Improved template organization when many templates are saved
- Improved template filtering by allowing templates to be shown by group
- Improved group deletion behavior: templates from a deleted group are automatically moved back to Ungrouped
- Improved group persistence after closing and reopening the world
- Improved the group workflow without changing the existing template save, load, rename, search, or preview behavior

### Notes

- Templates belong to one group at a time in this version
- Existing templates are treated as Ungrouped until assigned to a custom group
- Multi-selection and bulk deletion are not included in this version

## 1.4.0

### Summary

This update improves template management with a search bar and a rename option for saved templates.

### Added

- Added a search bar to the template screen
- Added real-time filtering for saved templates
- Added a `Rename` button for selected templates
- Added a rename screen with a simple text field
- Added automatic duplicate-name handling when renaming templates
- Added translated messages for search, empty search results, and rename actions

### Improved

- Improved template management when many templates are saved
- Improved template readability by allowing custom template names
- Improved search behavior by matching template names and item-related data
- Improved the template screen workflow without changing the existing save, load, delete, or preview behavior

### Notes

- Template loading still works by double-clicking a saved template
- Template previews from 1.3.0 remain unchanged
- Multi-selection, bulk deletion, and template groups are not included in this version

## 1.3.0

### Summary

This update adds a recipe preview for saved templates, making it easier to check a template before loading it.

### Added

- Added a visual recipe preview when hovering over a saved template
- Added a fixed preview panel next to the template list
- Added a 3x3 ingredient preview for saved crafting templates
- Added a result item preview next to the ingredient grid

### Improved

- Improved template readability before loading
- Improved the template screen by showing recipe contents without requiring the template to be loaded first
- Improved preview stability by keeping the preview panel fixed instead of following the mouse
- Kept template loading behavior unchanged: double-click still loads the selected template

### Notes

- The preview is display-only
- Templates are not loaded until the player double-clicks them
- Existing template saving, loading, deletion, and missing-ingredients feedback remain unchanged

## 1.2.0

### Summary

This update adds optional EMI integration, allowing compatible crafting recipes to be saved directly as AutoCraftTomsAddon templates.

### Added

- Added optional EMI integration
- Added a `Save as Template` button to compatible EMI crafting recipes
- Added support for saving crafting recipes from EMI into the AutoCraftTomsAddon template list
- Added a clear success message when a template is loaded correctly
- Added a clear failure message when a template cannot be loaded because the required ingredients are missing

### Improved

- Improved template loading feedback
- Improved the template workflow by making it possible to save recipes before manually placing them in the terminal
- Kept the EMI integration limited to standard crafting recipes for better stability

### Notes

- The EMI button requires EMI recipe decorators to be enabled
- This integration currently targets EMI only
- JEI, REI, and machine recipes are not supported in this version

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
