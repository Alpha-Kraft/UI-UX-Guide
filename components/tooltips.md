# Tooltips

Tooltips provide additional information about an element when the user hovers over or focuses on it.

## Anatomy

1.  **Container**: Small box with a background color (usually dark gray/black).
2.  **Text**: Short, explanatory text (max 2 lines).
3.  **Arrow (Optional)**: A small triangle pointing to the trigger element.

## Usage Guidelines

-   **When to Use**:
    -   Clarifying icons (e.g., "Settings" for a gear icon).
    -   Providing context for a truncated text (e.g., "...").
    -   Defining a term.
-   **When NOT to Use**:
    -   Hiding essential information (e.g., "Password Requirements").
    -   Displaying critical errors.
    -   Replacing labels on form fields.

## Positioning

-   **Top**: Default. Best for most cases.
-   **Bottom**: Use if the element is near the top edge.
-   **Left/Right**: Use for sidebars or list items.
-   **Logic**: Always keep the tooltip within the viewport. If it goes off-screen, flip its position.

## Code Example (CSS-Only)

```html
<button class="tooltip-container" aria-label="More Info">
  ℹ️
  <span class="tooltip-text">Click for more details about this feature.</span>
</button>
```

```css
.tooltip-container {
  position: relative;
  display: inline-block;
  cursor: pointer;
  background: none;
  border: none;
  font-size: 16px;
}

.tooltip-text {
  visibility: hidden;
  width: 200px;
  background-color: #333;
  color: #fff;
  text-align: center;
  border-radius: 4px;
  padding: 8px;
  position: absolute;
  z-index: 1;
  bottom: 125%; /* Position above */
  left: 50%;
  margin-left: -100px; /* Center horizontally */
  opacity: 0;
  transition: opacity 0.2s;
  font-size: 12px;
  pointer-events: none; /* Prevent blocking */
}

/* Arrow */
.tooltip-text::after {
  content: "";
  position: absolute;
  top: 100%; /* At bottom of tooltip */
  left: 50%;
  margin-left: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: #333 transparent transparent transparent;
}

.tooltip-container:hover .tooltip-text,
.tooltip-container:focus .tooltip-text {
  visibility: visible;
  opacity: 1;
}
```

## Accessibility (ARIA)
-   `aria-describedby`: Use this on the trigger element if the tooltip text is visible elsewhere in the DOM.
-   `aria-label`: Use this on the trigger element if the tooltip *is* the label (e.g., an icon-only button).
-   **Keyboard Access**: Tooltips must appear on Focus, not just Hover.

---

[Back to Component Library](../README.md#3-component-library)
