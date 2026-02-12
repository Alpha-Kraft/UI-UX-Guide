# Dropdowns (Selects)

Dropdowns allow users to select one or multiple items from a list, saving space.

## Anatomy

1.  **Label**: Describes the field.
2.  **Field**: The box showing the current selection (or placeholder).
3.  **Chevron**: Icon indicating expandability.
4.  **Menu**: The list of options (appears on click).

## Usage Guidelines

-   **When to Use**:
    -   Lists with > 5 items (e.g., Country, State).
    -   When screen space is limited.
-   **When NOT to Use**:
    -   Lists with < 5 items (use Radio Buttons).
    -   Binary choices (use Switch or Checkbox).
-   **Search**: Include a search bar inside the menu if > 15 options.

## Code Example

```html
<div class="dropdown">
  <label for="country">Country</label>
  <select id="country" name="country" class="form-select">
    <option value="" disabled selected>Select a country</option>
    <option value="US">United States</option>
    <option value="CA">Canada</option>
    <option value="UK">United Kingdom</option>
  </select>
</div>
```

```css
.form-select {
  display: block;
  width: 100%;
  padding: 10px 36px 10px 12px;
  font-size: 16px;
  color: #495057;
  background-color: #fff;
  background-image: url("data:image/svg+xml,..."); /* Chevron Icon */
  background-repeat: no-repeat;
  background-position: right 12px center;
  border: 1px solid #ced4da;
  border-radius: 4px;
  appearance: none; /* Removes native styling */
}

.form-select:focus {
  border-color: #80bdff;
  outline: 0;
  box-shadow: 0 0 0 3px rgba(0, 86, 179, 0.25);
}
```

## Accessibility (ARIA)
-   Native `<select>` is usually best for accessibility on mobile.
-   Custom dropdowns need `role="listbox"`, `aria-expanded`, `aria-activedescendant`.

---

[Back to Component Library](../README.md#3-component-library)
