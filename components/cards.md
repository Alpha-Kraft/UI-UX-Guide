# Cards

Cards are flexible containers that group related content and actions. They are widely used for lists, grids, and dashboards.

## Design Principles

1.  **Containment**: A card must clearly define its boundaries with a border or shadow.
2.  **Hierarchy**: Use typography and spacing to create a clear visual hierarchy within the card (e.g., Title > Description > Metadata > Action).
3.  **Interaction**: The entire card can be clickable (common in mobile) or contain specific interactive elements (buttons).

## Code Example (CSS)

```css
/* Card Container */
.card {
  background-color: #ffffff;
  border: 1px solid #e9ecef; /* Subtle border */
  border-radius: 8px; /* Smooth corners */
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05); /* Very subtle shadow */
  transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
  overflow: hidden; /* Ensures content doesn't spill out */
  display: flex;
  flex-direction: column;
}

/* Hover State (Desktop) */
.card:hover {
  transform: translateY(-2px); /* Slight lift */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* Card Content Areas */
.card-header {
  padding: 16px;
  border-bottom: 1px solid #f1f3f5;
  background-color: #f8f9fa;
  font-weight: 600;
}

.card-body {
  padding: 16px;
  flex-grow: 1; /* Pushes footer to bottom */
}

.card-footer {
  padding: 12px 16px;
  border-top: 1px solid #f1f3f5;
  background-color: #ffffff;
  display: flex;
  justify-content: flex-end; /* Align actions to right */
  gap: 8px;
}

/* Typography inside Card */
.card-title {
  margin: 0 0 8px 0;
  font-size: 18px;
  color: #212529;
}

.card-text {
  margin: 0;
  color: #495057;
  line-height: 1.5;
}
```

## Responsive Considerations

-   **Grid Layout**: Cards work best in a responsive grid (`display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));`).
-   **Mobile**: On mobile, cards often stack vertically and take full width. Consider removing shadows and using full-width dividers for a cleaner list view on small screens.

---

[Back to Component Library](../README.md#3-component-library)
