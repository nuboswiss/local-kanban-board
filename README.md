# Local Kanban Board

A lightweight, browser-based task management application that runs entirely in a single HTML file. No server, no installation, no dependencies.

## Features

- **Column Management** - Create, rename, reorder, and delete workflow columns
- **Task Cards** - Add, edit, and delete task cards with drag-and-drop support
- **External Links** - Attach links to cards (e.g., Jira tickets, GitHub issues)
- **Color Labels** - Organize tasks with color-coded labels (Red, Orange, Green, Blue, Purple)
- **Drag and Drop** - Move cards between columns with native HTML5 drag-and-drop
- **Local Storage** - Your board persists automatically in browser localStorage
- **Import/Export** - Save your board as JSON and restore it anytime
- **Zero Dependencies** - Pure HTML, CSS, and JavaScript with no frameworks

## Getting Started

### Option 1: Open Directly
Simply open `kanban.html` in any modern web browser.

### Option 2: Local Server
```bash
# Python 3
python -m http.server 8000

# Node.js (with http-server installed)
npx http-server
```
Then visit `http://localhost:8000/kanban.html`

## Usage

### Columns
| Action | How To |
|--------|--------|
| Add column | Click "Add Column" button in header |
| Rename column | Click on column title to edit inline |
| Reorder columns | Use left/right arrow buttons on column header |
| Delete column | Click the trash icon on column header |

### Cards
| Action | How To |
|--------|--------|
| Add card | Click "Add a card" at bottom of any column |
| Edit card | Click on card text to edit inline |
| Move card | Drag and drop to another column |
| Delete card | Hover over card, click trash icon |
| Add label | Hover over card, click label icon |
| Remove label | Click on an existing label to remove it |
| Add/edit link | Hover over card, click link icon (🔗) |
| Open link | Click the link displayed on the card |

### Data Management
| Action | How To |
|--------|--------|
| Export board | Click "Export" to download as JSON |
| Import board | Click "Import" to load a saved JSON file |
| Clear board | Click "Clear" to reset (with confirmation) |

## Technical Details

| Aspect | Details |
|--------|---------|
| File Size | Single HTML file (~1,175 lines) |
| Technologies | HTML5, CSS3, Vanilla JavaScript |
| Storage | Browser localStorage |
| External Resources | Google Fonts (Inter) |
| Browser Support | All modern browsers |

### Data Structure
```javascript
{
  "columns": [
    {
      "id": "unique-id",
      "title": "Column Name",
      "cards": [
        {
          "id": "unique-id",
          "content": "Task description",
          "labels": ["red", "blue"],
          "link": "https://jira.example.com/browse/PROJ-123"
        }
      ]
    }
  ]
}
```

## Storage

All data is stored locally in your browser using the localStorage API with the key `kanbanBoard`. This means:

- Data persists between browser sessions
- Data is private to your browser
- Clearing browser data will remove your board
- Use Export to backup your data

## Design

- Dark theme with glass-morphism effects
- Responsive layout for mobile and desktop
- Smooth transitions and animations
- Accessible keyboard navigation (Enter to confirm, Escape to cancel)

## License

This project is open source and available for personal and commercial use.
