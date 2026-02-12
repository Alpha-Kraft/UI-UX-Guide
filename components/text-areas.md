# Text Areas

Text areas allow users to input multiple lines of text.

## Anatomy

1.  **Label**: Describes the field.
2.  **Container**: Rectangular box (usually resizable).
3.  **Placeholder**: Example text.
4.  **Character Count**: Shows limit (e.g., "140/500").
5.  **Resize Handle**: Bottom-right corner.

## Usage Guidelines

-   **When to Use**:
    -   Comments, Feedback, Descriptions.
    -   Any text > 50 characters.
-   **Height**: Start with a minimum height (e.g., 3-4 lines).
-   **Auto-Grow**: Ideally, the text area should expand automatically as the user types, up to a max-height.

## Code Example

```html
<div class="textarea-container">
  <label for="feedback">Your Feedback</label>
  <textarea id="feedback" name="feedback" rows="4" maxlength="500"></textarea>
  <div class="char-count">0/500</div>
</div>
```

```css
textarea {
  display: block;
  width: 100%;
  padding: 12px;
  font-family: inherit;
  font-size: 16px;
  line-height: 1.5;
  color: #495057;
  background-color: #fff;
  border: 1px solid #ced4da;
  border-radius: 4px;
  resize: vertical; /* Allow vertical resize only */
}

textarea:focus {
  border-color: #80bdff;
  outline: 0;
  box-shadow: 0 0 0 3px rgba(0, 86, 179, 0.25);
}

.char-count {
  text-align: right;
  font-size: 12px;
  color: #6c757d;
  margin-top: 4px;
}
```

## Accessibility (ARIA)
-   `aria-describedby`: Use this to link the character count to the textarea so screen readers announce it.
-   `rows`: Sets the default visible height.

---

[Back to Component Library](../README.md#3-component-library)
