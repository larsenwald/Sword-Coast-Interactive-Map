# Faerûn Interactive Map

A high-performance, responsive interactive map of Faerûn (Sword Coast) built with pure HTML, CSS, and JavaScript. No external libraries or dependencies.

![Faerûn Map Preview](https://github.com/user-attachments/assets/2e519454-37e3-47e1-a6ad-d8bcf1ea797d)

## Features

- **Tile-based rendering** for handling extremely large images (10,000+ pixels) without performance issues
- **Smooth panning and zooming** with hardware acceleration
- **Customizable markers** for cities, towns, landmarks, and points of interest
- **Responsive design** that works on all screen sizes
- **Medieval fantasy UI** theme that's immersive for D&D campaigns
- **Touchscreen support** with controlled zoom behavior

## Setup

1. Split your large map image into 256×256 pixel tiles using an image slicing tool
2. Name them in the format `tile_Y_X.png` where Y is row (0-25) and X is column (0-39)
3. Place tiles in a folder named `faerun_tiles` next to the HTML file
4. Open the HTML file in a browser

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
