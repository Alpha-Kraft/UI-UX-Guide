# Data Tables

Data tables are essential for displaying structured information efficiently.

## Anatomy

1.  **Header Row**: Contains column titles. Must be sortable (with visual indicators).
2.  **Sort Indicator**: An arrow (▲ or ▼) showing the active sort direction.
3.  **Row**: A single record. Can be selectable (checkbox) or actionable (click to view details).
4.  **Pagination**: Controls at the bottom (e.g., "1-10 of 240" | "Next >").
5.  **Actions Column**: A specific column for row-level actions like "Edit" or "Delete".

## Design Guidelines

-   **Alignment**:
    -   *Text*: Left-aligned.
    -   *Numbers*: Right-aligned (makes comparing magnitudes easier).
    -   *Dates/Status*: Left-aligned or centered.
-   **Zebra Striping**: Alternating row colors (`#f8f9fa`) improves readability for wide tables.
-   **Sticky Header**: Keep the header visible when scrolling vertically.
-   **Checkboxes**: If bulk actions are available, include a "Select All" checkbox in the header.

## Code Example

```html
<div class="table-container">
  <table class="data-table">
    <thead>
      <tr>
        <th scope="col" aria-sort="ascending">Name <span class="sort-icon">▲</span></th>
        <th scope="col">Role</th>
        <th scope="col" class="text-right">Salary</th>
        <th scope="col">Status</th>
        <th scope="col" class="text-center">Actions</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Jane Doe</td>
        <td>Developer</td>
        <td class="text-right">$95,000</td>
        <td><span class="badge success">Active</span></td>
        <td class="text-center">
          <button class="icon-btn" aria-label="Edit Jane Doe">✏️</button>
          <button class="icon-btn" aria-label="Delete Jane Doe">🗑️</button>
        </td>
      </tr>
      <!-- More rows... -->
    </tbody>
  </table>

  <div class="pagination">
    <span>Showing 1-10 of 50</span>
    <div class="page-controls">
      <button disabled>Previous</button>
      <button>Next</button>
    </div>
  </div>
</div>
```

```css
.table-container {
  border: 1px solid #e9ecef;
  border-radius: 8px;
  overflow: hidden; /* For rounded corners */
}

.data-table {
  width: 100%;
  border-collapse: collapse;
  font-size: 14px;
}

th, td {
  padding: 12px 16px;
  border-bottom: 1px solid #e9ecef;
}

th {
  background-color: #f8f9fa;
  font-weight: 600;
  text-align: left;
  cursor: pointer; /* Suggests sortability */
}

th:hover {
  background-color: #e9ecef;
}

tr:hover {
  background-color: #f1f3f5; /* Row hover state */
}

.text-right { text-align: right; }
.text-center { text-align: center; }

.badge {
  padding: 4px 8px;
  border-radius: 12px;
  font-size: 12px;
  font-weight: 500;
}

.badge.success {
  background-color: #d4edda;
  color: #155724;
}
```

## Accessibility (ARIA)
-   `scope="col"`: Defines header cells for columns.
-   `scope="row"`: Defines header cells for rows (if applicable).
-   `aria-sort`: Indicates the current sort order (`ascending`, `descending`, `none`).

---

[Back to Component Library](../README.md#3-component-library)
