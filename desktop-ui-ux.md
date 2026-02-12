# Desktop UI/UX Guidelines

Desktop applications offer the highest potential for productivity and complexity. Users have precise input devices (mouse/keyboard), large screens, and the ability to multitask.

## 1. Information Density

Desktop users can process more information simultaneously.

-   **Scale**: Use smaller font sizes (13-14px base) compared to mobile (16px base) to fit more data.
-   **Tables & Lists**: Essential for data-heavy applications. Include sortable columns, filtering, and bulk actions.
-   **Panels**: Utilize split views and sidebars (e.g., file explorers, email clients) to show hierarchy and detail simultaneously.

## 2. Window Management

Desktop apps exist within a windowed environment.

-   **Resizability**: Interfaces must fluidly adapt to any window size, from a small floating tool to a full-screen workspace.
-   **Multiple Windows**: Allow users to open multiple instances (e.g., multiple document tabs or separate windows) for multitasking.
-   **Modals**: Use sparingly. Prefer non-blocking panels or inline editing to keep the user in context.

## 3. Keyboard Interaction & Strategy

Power users rely on keyboards for speed.

-   **Shortcuts**: Implement standard shortcuts (`Ctrl/Cmd + C` for copy, `S` for save, `Z` for undo).
-   **Mnemonics**: Underlined letters in menus (e.g., **F**ile) accessible via `Alt` key (Windows/Linux).
-   **Global Shortcuts**: If applicable, allow users to trigger actions even when the app is minimized (e.g., media keys).

| Action | Windows/Linux | macOS |
| :--- | :--- | :--- |
| **Save** | `Ctrl + S` | `Cmd + S` |
| **Find** | `Ctrl + F` | `Cmd + F` |
| **Close Window** | `Alt + F4` or `Ctrl + W` | `Cmd + W` |
| **Preferences** | `Ctrl + ,` (app specific) | `Cmd + ,` |

## 4. Data Tables

A cornerstone of desktop productivity software.

-   **Sorting**: Clickable column headers with arrows indicating sort direction.
-   **Filtering**: Advanced filters above the table or in a sidebar.
-   **Density**: Allow users to toggle between "Compact" and "Comfortable" row heights.
-   **Pagination**: Use pagination for datasets > 100 items. Provide "Rows per page" control.

## 5. Dashboard Design

Dashboards provide an at-a-glance view of key metrics.

-   **Widgets**: Use cards to group related data. Allow users to resize or rearrange widgets if possible.
-   **Customization**: Let users choose *what* metrics matter to them (e.g., "Add Widget" button).
-   **Visualization**: Use charts (Line, Bar, Pie) appropriately.
    -   *Line Chart*: Trends over time.
    -   *Bar Chart*: Comparing categories.
    -   *Pie Chart*: Showing parts of a whole (use sparingly, < 5 slices).

## 6. Multi-Select & Bulk Actions

Power users need to perform actions on multiple items at once.

-   **Selection**: Checkboxes in lists/tables.
    -   *Shift + Click*: Select a range of items.
    -   *Ctrl/Cmd + Click*: Toggle selection of individual items.
-   **Action Bar**: When items are selected, show a contextual toolbar (floating or fixed) with actions like "Delete", "Move", or "Archive".
-   **"Select All"**: Include a master checkbox to select all visible items (or all items across pages).

## 7. File Management

Desktop apps often deal with files.

-   **Drag and Drop Zones**: Large, clear areas to drop files. Highlight the area on drag over.
-   **Progress Tracking**: Show a progress bar for uploads/downloads. Don't block the UI; allow background processing.
-   **Previews**: Allow users to preview files (images, PDFs) without opening external applications.

## 8. Contextual Menus (Right-Click)

The right mouse button is a powerful tool for discovering actions related to a specific object.

-   **Relevance**: Show only actions relevant to the selected item (e.g., "Open," "Rename," "Delete" for a file).
-   **Consistency**: Ensure the most common actions are also available in the main UI or toolbar. Do not hide critical functionality *only* in a context menu.

---

[Back to Home](./README.md)
