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

## 3. Keyboard Interaction

Power users rely on keyboards for speed.

-   **Shortcuts**: Implement standard shortcuts (`Ctrl/Cmd + C` for copy, `S` for save, `Z` for undo).
-   **Tab Order**: Logical tab order (left-to-right, top-to-bottom) is critical for form navigation.
-   **Focus Indicators**: Visible focus rings are mandatory for keyboard accessibility.

| Action | Windows/Linux | macOS |
| :--- | :--- | :--- |
| **Save** | `Ctrl + S` | `Cmd + S` |
| **Find** | `Ctrl + F` | `Cmd + F` |
| **Close Window** | `Alt + F4` or `Ctrl + W` | `Cmd + W` |
| **Preferences** | `Ctrl + ,` (app specific) | `Cmd + ,` |

## 4. Contextual Menus (Right-Click)

The right mouse button is a powerful tool for discovering actions related to a specific object.

-   **Relevance**: Show only actions relevant to the selected item (e.g., "Open," "Rename," "Delete" for a file).
-   **Consistency**: Ensure the most common actions are also available in the main UI or toolbar. Do not hide critical functionality *only* in a context menu.

## 5. Tooltips & Hover States

Since desktop users have a cursor, leverage hover states for discovery.

-   **Tooltips**: Show helpful descriptions when hovering over icon-only buttons or truncated text.
-   **Hover Effects**: Subtle background changes or borders indicate interactivity.

## 6. Drag and Drop

A core expectation on desktop.

-   **Files**: Allow dragging files from the OS file explorer into the app.
-   **Reordering**: Allow reordering of list items, tabs, or Kanban cards via drag and drop.
-   **Feedback**: Provide clear visual cues (e.g., ghost image, insertion line) during the drag operation.

---

[Back to Home](./README.md)
