# Switches (Toggles)

Switches are a digital representation of a physical on/off switch.

## Anatomy

1.  **Track**: The background pill shape (gray when off, color when on).
2.  **Thumb**: The circle that slides back and forth.
3.  **Label**: Description of the setting.

## Usage Guidelines

-   **When to Use**:
    -   Instant actions (e.g., "Enable Dark Mode").
    -   Preferences that don't require a "Save" button.
-   **When NOT to Use**:
    -   Multiple options (use Radios).
    -   Data entry forms (use Checkboxes).
-   **State**: Should clearly indicate "On" (usually green or primary color) vs "Off" (gray).

## Code Example

```html
<label class="switch">
  <input type="checkbox" id="notifications-toggle" checked>
  <span class="slider round"></span>
  Enable Push Notifications
</label>
```

```css
.switch {
  position: relative;
  display: inline-block;
  width: 50px;
  height: 28px;
}

.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  transition: .4s;
  border-radius: 34px;
}

.slider:before {
  position: absolute;
  content: "";
  height: 20px;
  width: 20px;
  left: 4px;
  bottom: 4px;
  background-color: white;
  transition: .4s;
  border-radius: 50%;
}

input:checked + .slider {
  background-color: #28a745;
}

input:checked + .slider:before {
  transform: translateX(22px);
}

input:focus + .slider {
  box-shadow: 0 0 1px #28a745;
}
```

## Accessibility (ARIA)
-   `role="switch"`: Semantically identifies the control as a switch.
-   `aria-checked="true/false"`: Communicates state.

---

[Back to Component Library](../README.md#3-component-library)
