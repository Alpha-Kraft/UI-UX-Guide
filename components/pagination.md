# Pagination

Pagination breaks large datasets into manageable chunks.

## Anatomy

1.  **Previous/Next**: Directional navigation buttons.
2.  **Page Numbers**: Direct links to specific pages (truncated for large ranges).
3.  **Active Page**: Clearly highlighted (usually bold or filled background).
4.  **Ellipsis**: Indicates skipped page numbers (e.g., `1 ... 5 6 7 ... 20`).

## Usage Guidelines

-   **When to Use**: Lists with 20+ items where random access (jumping to page 10) is useful.
-   **When NOT to Use**: Social feeds (use Infinite Scroll) or small lists (< 20 items).

## Code Example

```html
<nav aria-label="Pagination">
  <ul class="pagination">
    <li><button aria-label="Previous Page" disabled>&laquo;</button></li>
    <li><button class="active" aria-current="page">1</button></li>
    <li><button>2</button></li>
    <li><button>3</button></li>
    <li><button aria-label="Next Page">&raquo;</button></li>
  </ul>
</nav>
```

```css
.pagination {
  list-style: none;
  display: flex;
  gap: 4px;
}

.pagination button {
  padding: 8px 12px;
  border: 1px solid #dee2e6;
  background: white;
  cursor: pointer;
  border-radius: 4px;
}

.pagination button.active {
  background-color: #0056b3;
  color: white;
  border-color: #0056b3;
}

.pagination button:hover:not(.active):not(:disabled) {
  background-color: #e9ecef;
}
```

## Accessibility (ARIA)
-   `aria-current="page"`: Essential for screen readers.
-   `disabled`: Prevents clicking "Previous" on page 1.

---

[Back to Component Library](../README.md#3-component-library)
