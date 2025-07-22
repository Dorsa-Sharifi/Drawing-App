# Drawing App
A simple React application for drag-and-drop drawing with basic shapes. Users can import/export their drawings as JSON files and see real-time shape statistics.
## Features
- **Editable Painting Name**: Change the name of your drawing in the header.
- **Import/Export**: Save and load drawings with all metadata as `.json` files.
- **Sidebar**: Drag shapes (circle, square, triangle) from the left sidebar.
- **Canvas**: Drop shapes on a central canvas and position them freely.
- **Shape Removal**: Double-click a shape to remove it from the canvas.
- **Shape Counter**: Bottom bar displays shape types and how many of each are used.
---


---

## Component Overview

### `App.tsx`
All the componenets, functions and handlers that we used in the App.tsx file are written below: 
- **State Management**:
  - `paintingName`: Title of the drawing.
  - `shapes`: Array of placed shapes.
  - `draggingShape`: Tracks the shape type being dragged.
- **Handlers**:
  - `addShape()`: Adds a shape to canvas.
  - `handleDrop()`: Calculates drop position and adds shape.
  - `handleExport()`: Saves drawing as JSON.
  - `handleImport()`: Loads drawing from JSON file.
  - `removeShape()`: Deletes a shape on double click.

### `ShapeIcon`
- A helper component to render shape previews (`circle`, `square`, `triangle`).

---

## JSON Structure (Import/Export)
This is how we save our drawing.
```json
{
  "name": "My Painting",
  "shapes": [
    {
      "id": "uuid",
      "type": "circle",
      "x": 100,
      "y": 150
    },
    ...
  ]
}


