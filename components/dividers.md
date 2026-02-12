# Dividers

Dividers visually separate content groups.

## Anatomy

1.  **Line**: Horizontal (hr) or Vertical (vl).
2.  **Color**: Usually a light gray (`#e9ecef`) for subtlety.
3.  **Weight**: 1px (standard). 2-4px (section breaks).

## Usage Guidelines

-   **When to Use**:
    -   Separating list items.
    -   Separating sections in a card (Header / Body / Footer).
    -   Separating major content blocks.
-   **When NOT to Use**:
    -   Between every single element (clutter). Use whitespace instead.
-   **Style**:
    -   *Full Width*: Spans the entire container.
    -   *Inset*: Has left/right padding (common in lists with avatars).

## Code Example

```html
<div class="content">
  <p>Section 1</p>
  <hr class="divider">
  <p>Section 2</p>
  <div class="vertical-divider-container">
    <span>Item 1</span>
    <span class="divider-vertical"></span>
    <span>Item 2</span>
  </div>
</div>
```

```css
.divider {
  border: 0;
  border-top: 1px solid #e9ecef;
  margin: 16px 0;
}

.divider-vertical {
  display: inline-block;
  width: 1px;
  height: 16px;
  background-color: #e9ecef;
  margin: 0 8px;
  vertical-align: middle;
}
```

## Accessibility (ARIA)
-   `role="separator"`: Use if the divider implies a thematic break.
-   `aria-hidden="true"`: Use if purely decorative.

---

[Back to Component Library](../README.md#3-component-library)
