# Web UI/UX Guidelines

The web is a flexible medium. Interfaces must adapt to various screen sizes, input methods (mouse, touch, keyboard), and browser capabilities.

## 1. Responsive Layout

We use a **fluid grid system** that adapts to breakpoints.

### Breakpoints (Mobile First)
-   **Mobile**: < 576px (100% width, single column)
-   **Tablet**: ≥ 576px (2 columns or adjusted margins)
-   **Laptop**: ≥ 992px (Maximum container width 960px)
-   **Desktop**: ≥ 1200px (Maximum container width 1140px)

### The 12-Column Grid
A standard 12-column grid provides flexibility for almost any layout.

```css
/* Example: CSS Grid Container */
.grid-container {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 24px; /* Gutter width */
}

/* Span classes */
.col-12 { grid-column: span 12; }
.col-6  { grid-column: span 6; }
.col-4  { grid-column: span 4; }
.col-3  { grid-column: span 3; }

/* Responsive adjustments */
@media (max-width: 768px) {
  .col-6, .col-4, .col-3 {
    grid-column: span 12; /* Stack on mobile */
  }
}
```

## 2. Navigation

Navigation should be intuitive and consistent.

### Header Navigation
-   **Sticky Headers**: Keep headers visible but shrink them on scroll to save space.
-   **Mega Menus**: Use for sites with deep hierarchies (e.g., E-commerce). Group links by category with clear headings. Do not nest menus more than 2 levels deep in a dropdown.

### Pagination vs. Infinite Scroll
-   **Pagination**: Best for goal-oriented tasks (e.g., finding a specific order, search results). Allows the user to reach the footer.
-   **Infinite Scroll**: Best for exploration (e.g., social feeds). **Warning**: Accessibility nightmare if not handled correctly. Users cannot reach the footer.

## 3. Interaction States

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

## 4. Forms and Inputs

Forms are the primary way users interact with web applications. Clarity is key.

-   **Labels**: Always place labels *above* the input field.
-   **Placeholders**: Do not use placeholders as replacements for labels.
-   **Inline Validation**: Show positive validation (green check) for complex fields (username availability) and immediate error messages for formatting issues.

## 5. Empty States

Don't leave the user staring at a blank screen when there is no data.

-   **Illustration**: Use a subtle, grayscale illustration (no cartoons) to indicate emptiness.
-   **Text**: "No projects found" (Clear status) + "Create a new project to get started" (Call to action).
-   **Action**: Provide a button to resolve the empty state immediately.

```html
<div class="empty-state">
  <img src="/assets/empty-box.svg" alt="" aria-hidden="true">
  <h3>No documents yet</h3>
  <p>Upload a document to start collaborating.</p>
  <button class="btn btn-primary">Upload Document</button>
</div>
```

## 6. Search Experience

Search is often the primary navigation method.

-   **Auto-Complete**: Suggest search terms as the user types. Highlight matched characters in bold.
-   **Recent Searches**: Show recent queries when the search field is focused.
-   **Results Page**:
    -   *Layout*: List or grid view toggle.
    -   *Filters*: Sidebar filters for complex data (e.g., E-commerce).
    -   *No Results*: "We couldn't find 'xyz'. Did you mean 'abc'?" + Popular categories.

## 7. Progress Indicators

Communicate status clearly for multi-step processes.

-   **Steppers**: Use for linear workflows (e.g., Checkout: Shipping -> Payment -> Review). Show "Completed", "Active", and "Pending" states clearly.
-   **Progress Bars**: Use for loading deterministically (e.g., File Upload: 45%).
-   **Spinners**: Use for indeterminate loading (e.g., "Fetching data...").

## 8. Notifications

Use the right level of interruption.

-   **Toasts (Snackbars)**: Non-blocking, auto-dismissing messages (e.g., "File saved"). Display at top-right (desktop) or bottom-center (mobile).
-   **Banners**: Persistent messages within the content area (e.g., "Your trial expires in 3 days"). Require user dismissal.
-   **Modals**: Blocking, critical messages (e.g., "Session expired"). Use sparingly.

## 9. Performance as UX

A slow interface feels unprofessional.
-   **Loading States**: Use skeletons (gray placeholders) instead of generic spinners for content loading.
-   **Feedback**: Any action taking > 100ms should provide visual feedback.

---

[Next: Mobile UI/UX Guidelines](./mobile-ui-ux.md) | [Back to Home](./README.md)
