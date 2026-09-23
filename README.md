# FolderColorer for Windows 10 / 11

A fast, lightweight application for customizing Windows Explorer folder icons via `desktop.ini` and the right-click context menu.

GitHub Repository: [https://github.com/fhkapusta/folder-colorer](https://github.com/fhkapusta/folder-colorer)

---

## 🚀 Key Features

- **Instant 1-Click Folder Coloring**: Right-click any folder -> **"Folder Color"** -> click your desired color. The icon updates immediately without showing extra windows!
- **Floating Icon Palette**: Click **"Palette / More packs..."** (or run `FolderColorer.exe "<folder>"`) to open a modern floating palette with large icon tiles and pack selection directly near your cursor.
- **⭐ Set as Default Palette**: Switch between different packs right inside the palette window and click **"Set as default palette"** to immediately update the Explorer right-click cascading menu to show icons from that palette!
- **Inside Folder Background Support**: Right-clicking the empty background inside any open folder also includes the **"Folder Color"** menu.
- **Instant Explorer Refresh**: Writes `desktop.ini` and automatically triggers `Refresh` on all open Explorer windows and the Desktop.
- **Reset to Default**: Easily revert any customized folder back to Windows default with 1 click.
- **Icon Packs**: Packs are stored in `Icons/`. Default pack is `Icons/Default/`. Additional packs can be added at any time.
---

## 🖥 How to Use

### 1. Integration into Windows Explorer
- Run `FolderColorer.exe`.
- Click **"⚡ Install Context Menu"**.
- That's it! Integration is active.

### 2. Changing Folder Icons
- **Windows 10**: Right-click any folder -> hover over **"Folder Color"** -> pick a color.
- **Windows 11**: Right-click any folder -> click **"Show more options"** (or press **Shift + F10**) -> hover over **"Folder Color"** -> pick a color.
- Or click **"Palette / More packs..."** for the visual grid.

### 3. Setting a Palette as Default
- Open the palette via **"Palette / More packs..."** or by opening `FolderColorer.exe "<folder>"`.
- Pick any pack from the **Icon pack** dropdown.
- Click **"⭐ Set as default palette"**. The right-click Explorer context menu is immediately updated to use this pack!

### 4. Resetting to Default
- In the same right-click menu, select **"Reset to default icon"**.

---

## 🎨 Adding Custom Icon Packs

1. Create a new subfolder in `Icons/`, e.g. `Icons/Pastel/`.
2. Place `.ico` files inside.
3. *(Optional)* Add a `pack.json` file for custom names:
   ```json
   {
     "name": "Pastel Colors",
     "icons": {
       "01.ico": "Pastel Blue",
       "02.ico": "Pastel Pink"
     }
   }
   ```
4. In `FolderColorer.exe` or the palette window, select your new pack and click **"Set as default palette"**.

---

## ⚙ Command Line Interface (CLI)

| Command | Description |
|---|---|
| `FolderColorer.exe set "<folder>" "<icon.ico>"` | Sets custom folder icon via `desktop.ini` and refreshes Explorer |
| `FolderColorer.exe reset "<folder>"` | Resets folder icon to Windows default |
| `FolderColorer.exe "<folder>"` | Opens floating palette for the folder |
| `FolderColorer.exe --install [PackName]` | Installs context menu to Explorer registry |
| `FolderColorer.exe --uninstall` | Removes context menu from Explorer registry |
| `FolderColorer.exe` | Opens settings GUI |