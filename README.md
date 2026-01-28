# Bitmap Editor Tools

A collection of browser-based pixel art editors for creating 1-bit bitmap graphics, designed for embedded systems and microcontrollers.

## 🎨 Editors

### [Bitmap Emote Editor](https://ixitxachitl.github.io/bitmap-editor/)
A single-image editor for creating bitmap emotes and icons.

**Features:**
- Adjustable canvas size (up to 128×128)
- Drawing tools: Draw, Erase, Line, Rect, Circle, Filled Circle, Flood Fill, Select
- Transform tools: Flip H/V, Rotate, Invert
- Selection with copy/cut/paste (Ctrl+C/X/V)
- Paste images from clipboard with threshold control
- Import/Export C arrays with configurable bit packing (LSB/MSB first)
- Undo/Redo support

### [MeshPet Animation Editor](https://ixitxachitl.github.io/bitmap-editor/animation_editor.html)
A multi-frame animation editor for creating sprite animations.

**Features:**
- Multiple animations with named frames
- Frame management: Add, duplicate, delete, reorder
- Animation preview with adjustable playback speed
- All drawing and transform tools from the Emote Editor
- Selection with copy/cut/paste across frames
- Paste images from clipboard as movable selections
- Import/Export `PetImages.h` format for Meshtastic firmware
- Preserves static icons and custom animations on import

## 🐾 MeshPet Firmware

These editors are designed to work with the MeshPet module for Meshtastic:

**[MeshPet Firmware Branch](https://github.com/Ixitxachitl/meshtastic-firmware/tree/feat/meshpet)**

MeshPet adds a virtual pet to your Meshtastic device that reacts to network activity, messages, and user interaction.

## 🎹 Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl+Z` | Undo |
| `Ctrl+Y` / `Ctrl+Shift+Z` | Redo |
| `Ctrl+C` | Copy selection |
| `Ctrl+X` | Cut selection |
| `Ctrl+V` | Paste (internal clipboard or image) |
| `Delete` / `Backspace` | Delete selection |
| `Escape` | Commit floating selection |

## 📋 Clipboard Features

- **Copy selection**: Copies pixels to internal clipboard and text representation to system clipboard
- **Paste image**: Paste any image from clipboard, adjust threshold to convert to 1-bit, position as floating selection
- **Paste Image button**: Manually trigger image paste from clipboard

## 🛠️ Usage Tips

1. **Creating animations**: Use the Animation Editor to create multi-frame animations, then export as `PetImages.h`
2. **Creating icons**: Use the Emote Editor for single images, export as C array
3. **Importing existing sprites**: Paste images directly or import C arrays
4. **Editing selections**: Select an area, then use Flip/Rotate/Invert to transform just that region

## 📄 License

MIT License - See [LICENSE](LICENSE) file for details.
