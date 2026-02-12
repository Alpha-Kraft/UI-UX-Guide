# Lists

Lists display a collection of related items vertically.

## Anatomy

1.  **Item**: A single row.
2.  **Avatar/Icon (Optional)**: Left-aligned visual.
3.  **Primary Text**: Main label.
4.  **Secondary Text**: Description or metadata.
5.  **Action (Optional)**: Right-aligned button or chevron.
6.  **Divider**: Line separating items.

## Usage Guidelines

-   **Density**:
    -   *Compact*: Single-line text, 40px height.
    -   *Standard*: Two-line text, 60px height.
    -   *Spacious*: Cards or complex items.
-   **Interactivity**:
    -   *Selection*: Checkboxes on the left.
    -   *Navigation*: Chevron (>) on the right indicates tapping opens a detail view.

## Code Example

```html
<ul class="list-group">
  <li class="list-item">
    <div class="list-content">
      <div class="list-title">Inbox</div>
      <div class="list-subtitle">5 unread messages</div>
    </div>
    <span class="badge">5</span>
  </li>

  <li class="list-item actionable">
    <div class="list-content">
      <div class="list-title">Settings</div>
    </div>
    <span class="icon-chevron">›</span>
  </li>
</ul>
```

```css
.list-group {
  list-style: none;
  padding: 0;
  border: 1px solid #e9ecef;
  border-radius: 8px;
}

.list-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 12px 16px;
  border-bottom: 1px solid #e9ecef;
  background-color: white;
}

.list-item:last-child {
  border-bottom: none;
}

.list-item.actionable {
  cursor: pointer;
}

.list-item.actionable:hover {
  background-color: #f8f9fa;
}

.list-title {
  font-weight: 500;
  color: #212529;
}

.list-subtitle {
  font-size: 14px;
  color: #6c757d;
}

.icon-chevron {
  color: #adb5bd;
  font-size: 20px;
}
```

## Accessibility (ARIA)
-   `role="list"`: Standard list role.
-   `role="listitem"`: Standard item role.
-   Ensure list items are actionable via keyboard if they are interactive.

---

[Back to Component Library](../README.md#3-component-library)
