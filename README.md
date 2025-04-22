# Faerûn Interactive Map

A high-performance, responsive interactive map of Faerûn (Sword Coast) built with pure HTML, CSS, and JavaScript. No external libraries or dependencies.

![Faerûn Map Preview](https://github.com/user-attachments/assets/2e519454-37e3-47e1-a6ad-d8bcf1ea797d)

## Features

- **Tile-based rendering** for handling extremely large images (10,000+ pixels) *without performance issues*
- **Smooth panning and zooming** with, drumroll please, hardware acceleration!
- **Customizable markers** for cities, towns, landmarks, and points of interest
- **Responsive design** naturally :)
- **Touchscreen support** with controlled zoom behavior

## Reverse engineering for your own map

The software can actually work with any map, if you wish to reverse engineer it.

### Tile System Setup

1. Slice your map into 256x256px tiles named `tile_y_x.png`. There are many python scripts out there that can do this for you using Pillow, or you could write one yourself.
2. Update these variables:
   - `tilesX` and `tilesY` to match your grid dimensions
   - `originalWidth` and `originalHeight` to your map's full resolution
   - `tileSize` if using different tile dimensions

## Customization

### Map Markers

Edit the `locations` array to add your own points of interest:

```javascript
{
    id: 1,
    name: "Location Name",
    type: "city", // Options: city, town, landmark, poi
    description: "Description of the location",
    x: originalWidth * 0.45,  // X coordinate as percentage of map width
    y: originalHeight * 0.75  // Y coordinate as percentage of map height
}
```

### Initial View

Adjust these values to change the starting position and zoom level:

```javascript
const initialScale = 0.6; // Initial zoom level
const initialX = 0.42;    // X position to center on (0-1)
const initialY = 0.24;    // Y position to center on (0-1)
```

## Credits

Created for a D&D character in the Forgotten Realms setting. Faerûn and Sword Coast are © Wizards of the Coast.

Map implementation by Larsenwald - 2025.
