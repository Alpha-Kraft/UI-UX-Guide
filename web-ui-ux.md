# Web UI/UX Guidelines

The web is a flexible medium. Interfaces must adapt to various screen sizes, input methods (mouse, touch, keyboard), and browser capabilities.

## 1. Responsive Layout

We use a **fluid grid system** that adapts to breakpoints.

### Breakpoints (Mobile First)
-   **Mobile**: < 576px (100% width, single column)
-   **Tablet**: ≥ 576px (2 columns or adjusted margins)
-   **Laptop**: ≥ 992px (Maximum container width 960px)
-   **Desktop**: ≥ 1200px (Maximum container width 1140px)

### CSS Grid & Flexbox
Prefer modern layout techniques over float-based grids.

```css
/* Example: Responsive Card Grid */
.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 24px; /* 3 units of 8px */
}
```

## 2. Navigation

Navigation should be intuitive and consistent.

-   **Header**: Keep it sticky or visible.
-   **Links**: Links within text paragraphs must be underlined or have a distinct color (contrast > 3:1 against surrounding text).
-   **Breadcrumbs**: Essential for deep hierarchies (e.g., E-commerce, Documentation).

### States
Every interactive element must have defined states:
1.  **Default**: The resting state.
2.  **Hover**: Visual feedback when the cursor is over the element (Desktop only).
3.  **Focus**: High-contrast outline for keyboard navigation.
4.  **Active**: Visual feedback when clicked/tapped.
5.  **Disabled**: Muted visual style (reduced opacity), not interactable.

```css
/* Professional Button States */
.btn-primary {
  background-color: #0056b3;
  color: white;
  transition: background-color 0.2s ease;
}

.btn-primary:hover {
  background-color: #004494; /* Slightly darker */
}

.btn-primary:focus {
  outline: 3px solid rgba(0, 86, 179, 0.5); /* Visible focus ring */
  outline-offset: 2px;
}

.btn-primary:disabled {
  background-color: #e9ecef;
  color: #adb5bd;
  cursor: not-allowed;
}
```

## 3. Forms and Inputs

Forms are the primary way users interact with web applications. Clarity is key.

-   **Labels**: Always place labels *above* the input field for best readability on all screen sizes.
-   **Placeholders**: Do not use placeholders as replacements for labels. They disappear when the user types.
-   **Validation**:
    -   Show errors inline, immediately after the field.
    -   Use clear, helpful error messages (e.g., "Email is required" instead of just "Error").
    -   Don't rely on color alone (use an icon or text prefix).

## 4. Typography on the Web

-   **Line Length**: optimal line length for reading is 45-75 characters.
-   **Web Fonts**: Use `woff2` format for best performance. Implement `font-display: swap` to avoid invisible text during loading.

## 5. Performance as UX

A slow interface feels unprofessional.
-   **Loading States**: Use skeletons (gray placeholders) instead of generic spinners for content loading.
-   **Feedback**: Any action taking > 100ms should provide visual feedback.

---

[Next: Mobile UI/UX Guidelines](./mobile-ui-ux.md) | [Back to Home](./README.md)
