# Checkboxes & Radio Buttons

Standard components for selecting options from a list.

## Anatomy

1.  **Checkbox**: Square box. Allows **multiple** selections (or none).
2.  **Radio Button**: Circular button. Allows **single** selection from a group.
3.  **Label**: Text description. Clicking the label must toggle the control.

## Usage Guidelines

-   **Checkboxes**: "Select all that apply." Also used for single binary choices (e.g., "I agree to terms").
-   **Radio Buttons**: "Select one option." If more than 5 options, use a Dropdown.
-   **Indeterminate State**: A checkbox state (often a dash `-`) used in "Select All" scenarios when only *some* child items are selected.

## Code Example

```html
<form>
  <!-- Checkbox Group -->
  <fieldset>
    <legend>Interests</legend>
    <label class="control checkbox">
      <input type="checkbox" name="interests" value="coding">
      <span class="indicator"></span>
      Coding
    </label>
    <label class="control checkbox">
      <input type="checkbox" name="interests" value="design" checked>
      <span class="indicator"></span>
      Design
    </label>
  </fieldset>

  <!-- Radio Group -->
  <fieldset>
    <legend>Notification Frequency</legend>
    <label class="control radio">
      <input type="radio" name="frequency" value="daily" checked>
      <span class="indicator"></span>
      Daily
    </label>
    <label class="control radio">
      <input type="radio" name="frequency" value="weekly">
      <span class="indicator"></span>
      Weekly
    </label>
  </fieldset>
</form>
```

```css
.control {
  display: block;
  position: relative;
  padding-left: 32px;
  margin-bottom: 12px;
  cursor: pointer;
  font-size: 16px;
  user-select: none;
}

.control input {
  position: absolute;
  opacity: 0; /* Hide native input */
  cursor: pointer;
  height: 0;
  width: 0;
}

.indicator {
  position: absolute;
  top: 0;
  left: 0;
  height: 20px;
  width: 20px;
  background-color: #eee;
  border: 1px solid #ced4da;
  border-radius: 4px; /* Checkbox radius */
}

/* Radio Specifics */
.radio .indicator {
  border-radius: 50%;
}

/* Hover */
.control:hover input ~ .indicator {
  background-color: #e2e6ea;
}

/* Checked */
.control input:checked ~ .indicator {
  background-color: #0056b3;
  border-color: #0056b3;
}

/* Checkmark/Dot (Pseudo-element) */
.indicator:after {
  content: "";
  position: absolute;
  display: none;
}

.control input:checked ~ .indicator:after {
  display: block;
}

.checkbox .indicator:after {
  left: 6px;
  top: 2px;
  width: 5px;
  height: 10px;
  border: solid white;
  border-width: 0 2px 2px 0;
  transform: rotate(45deg);
}

.radio .indicator:after {
  top: 6px;
  left: 6px;
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: white;
}
```

## Accessibility (ARIA)
-   Use `<fieldset>` and `<legend>` to group related controls semantically.
-   Ensure labels are associated via `for` attribute or nesting (as shown above).
-   Keyboard focus must be visible on the custom indicator.

---

[Back to Component Library](../README.md#3-component-library)
