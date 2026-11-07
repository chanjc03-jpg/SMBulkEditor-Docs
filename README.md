# SM Bulk Editor – Batch Edit Static Mesh Settings
*Bulk editor for Static Mesh settings in Unreal Engine 5*

Publisher: Haishan · Author: Christon Chan · Supported engines: UE 5.0–5.8 · Platform: Win64 editor

SM Bulk Editor shows the settings of many Static Meshes in one table, so you can change them together and preview every change before anything is written.

## Install
1. Install the plugin from Fab.
2. Enable **SM Bulk Editor** in **Edit > Plugins**, then restart the editor.

Windows (Win64), Unreal Editor only (one Editor module).

## Open the editor
- **Tools > SM Bulk Editor**, or
- Right-click one or more Static Meshes in the Content Browser > **Edit in SM Bulk Editor**, or
- In the SM Bulk Editor tab, select meshes in the Content Browser and click **Use Content Browser Selection**.

Assets that are not Static Meshes are skipped; the status bar reports how many were loaded and how many failed.

## Columns
| Column | Control |
|---|---|
| Asset | Read-only (optional thumbnail) |
| Nanite | Checkbox |
| Collision Complexity | Value |
| Collision Preset | Value |
| LOD Count, LODn Screen Size, LODn % Triangles | Numeric. **LOD Count can only be increased.** Any reduction is blocked with `BLOCKED: LOD reduction is not reversible`. |
| Lightmap Coordinate Index | Integer |
| Generate Distance Field | Checkbox |
| DF Resolution Scale | Numeric |

Rules:
- While Nanite is on (including a pending change to Nanite), the LOD fields are disabled.
- DF Resolution Scale is disabled while Generate Distance Field is off.

## Editing many meshes
Select rows (Ctrl/Shift-click, **Select All**, or Ctrl+A), then edit one cell. The value is applied as a *pending edit* to every selected row. The header checkboxes on **Nanite** and **Generate Distance Field** set all selected rows. **Clear Selection** deselects all rows.

## Dry Run
**Dry Run** lists every pending change as `old → new` for each mesh, with warnings for invalid values. It writes nothing.

**Discard Pending** clears all pending edits. This cannot be undone.

## Thumbnails
Use the **Thumbnails** toggle in the toolbar to show or hide asset thumbnails.

## Scope
- Static Mesh settings only: Nanite, collision, LOD parameters, lightmap coordinate index, distance field.
- LOD Count can be increased but never reduced.
- Not included: Texture settings, remeshing, generating LOD geometry.

## Requirements
- Windows 64-bit Unreal Editor, UE 5.0–5.8.
- Editor-only plugin.

## Support
- Fab listing: com.epicgames.launcher://ue/Fab/product/240d370c-fc09-4850-8bf0-189e096afe91
- Support: [chanjc03@gmail.com](mailto:chanjc03@gmail.com)
