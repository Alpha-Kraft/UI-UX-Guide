# Forms

Forms are critical for data entry and application interactions.

## Anatomy

1.  **Label**: Describes the input. MUST be visible at all times (no placeholder-only labels).
2.  **Input Field**: The interactive area (text box, dropdown, checkbox).
3.  **Placeholder (Optional)**: Example text (e.g., "e.g., jane@example.com"). Not a replacement for a label.
4.  **Helper Text (Optional)**: Instructions or context below the field (e.g., "Password must be 8+ chars").
5.  **Validation Message (Error/Success)**: Feedback appearing below the field or to the right.

## Design Principles

1.  **Labels Above**: Place labels above input fields for consistent readability across all devices.
2.  **Clear Validation**: Provide immediate feedback when fields are invalid.
3.  **Grouping**: Use fieldsets or visual separation for related fields (e.g., Shipping vs. Billing).

## Code Example (HTML/CSS)

```html
<form class="form-group" novalidate>
  <!-- Text Input -->
  <div class="field-container">
    <label for="email" class="label">Email Address <span class="required">*</span></label>
    <input
      type="email"
      id="email"
      name="email"
      class="input-field"
      placeholder="you@company.com"
      required
      aria-describedby="email-helper"
    >
    <span id="email-helper" class="helper-text">We'll never share your email.</span>
  </div>

  <!-- Password Input with Error -->
  <div class="field-container error">
    <label for="password" class="label">Password <span class="required">*</span></label>
    <input
      type="password"
      id="password"
      name="password"
      class="input-field error-border"
      aria-invalid="true"
      aria-describedby="password-error"
    >
    <span id="password-error" class="error-message" role="alert">
      <svg width="12" height="12" viewBox="0 0 12 12"><!-- Error Icon --></svg>
      Password must be at least 8 characters.
    </span>
  </div>
</form>
```

```css
/* Container Spacing */
.field-container {
  margin-bottom: 24px; /* 3 units of 8px */
  display: flex;
  flex-direction: column;
}

/* Label Styling */
.label {
  font-size: 14px;
  font-weight: 600;
  color: #343a40;
  margin-bottom: 8px;
}

.required {
  color: #dc3545;
}

/* Input Styling */
.input-field {
  padding: 10px 12px;
  font-size: 16px;
  border: 1px solid #ced4da;
  border-radius: 4px;
  background-color: #ffffff;
  transition: border-color 0.15s ease-in-out;
}

/* Focus State */
.input-field:focus {
  border-color: #80bdff;
  outline: 0;
  box-shadow: 0 0 0 3px rgba(0, 86, 179, 0.25);
}

/* Helper Text */
.helper-text {
  font-size: 12px;
  color: #6c757d;
  margin-top: 4px;
}

/* Error State */
.error-border {
  border-color: #dc3545;
}

.error-message {
  font-size: 12px;
  color: #dc3545;
  margin-top: 4px;
  display: flex;
  align-items: center;
  gap: 4px;
}
```

## Accessibility (ARIA)
-   `aria-describedby`: Links the input to its helper text or error message ID. Critical for screen readers.
-   `aria-invalid="true"`: Programmatically indicates the field has an error.
-   `role="alert"`: Announces the error message immediately when it appears.
-   `autocomplete`: Use standard values (`email`, `username`, `current-password`) to help users fill forms faster.

## Tips

-   **Auto-complete**: Enable browser auto-complete attributes (`autocomplete="email"`, `autocomplete="new-password"`) to speed up filling.
-   **Keyboard Navigation**: Ensure users can Tab through fields in a logical order.
-   **Password Visibility**: Include a toggle to show/hide password text.

---

[Back to Component Library](../README.md#3-component-library)
