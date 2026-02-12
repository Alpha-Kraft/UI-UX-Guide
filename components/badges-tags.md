# Badges & Tags

Badges and Tags are compact elements that represent status, category, or count.

## Anatomy

1.  **Badge**: Small circle/pill, usually with a number (e.g., notification count).
2.  **Tag**: Pill shape with text (e.g., "Pending", "Design").
3.  **Color**: Semantic meaning (Green = Success, Red = Alert).
4.  **Dismiss Button (Optional)**: "x" icon to remove the tag (e.g., filter chips).

## Usage Guidelines

-   **Badges**:
    -   Use for counts (Notifications: 5).
    -   Use for status dots (Online/Offline).
-   **Tags**:
    -   Use for categories (Blog Post: "Tech", "News").
    -   Use for filters (Applied Filter: "Size: M x").
    -   Keep text short (1-2 words).

## Code Example

```html
<div class="tags-container">
  <span class="badge primary">New</span>
  <span class="badge success">Active</span>
  <span class="badge warning">Pending</span>
  <span class="badge danger">Expired</span>

  <span class="tag">
    Design
    <button class="close-btn" aria-label="Remove Design tag">x</button>
  </span>
</div>
```

```css
.badge {
  display: inline-block;
  padding: 4px 8px;
  font-size: 12px;
  font-weight: 700;
  line-height: 1;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: 10px;
  color: #fff;
}

.badge.primary { background-color: #007bff; }
.badge.success { background-color: #28a745; }
.badge.warning { background-color: #ffc107; color: #212529; }
.badge.danger  { background-color: #dc3545; }

.tag {
  display: inline-flex;
  align-items: center;
  padding: 4px 12px;
  background-color: #e9ecef;
  border-radius: 16px;
  font-size: 14px;
  color: #495057;
  gap: 8px;
}

.close-btn {
  background: none;
  border: none;
  font-size: 14px;
  font-weight: bold;
  cursor: pointer;
  color: #6c757d;
  padding: 0;
  line-height: 1;
}

.close-btn:hover { color: #000; }
```

## Accessibility (ARIA)
-   `role="status"`: For dynamic updates.
-   `aria-label`: Essential for icon-only badges.

---

[Back to Component Library](../README.md#3-component-library)
