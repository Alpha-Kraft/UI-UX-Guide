# Progress Bars

Progress bars indicate the completion status of a task.

## Anatomy

1.  **Track**: Total range (0% to 100%).
2.  **Fill**: Amount completed.
3.  **Label**: Percentage text or description ("Uploading...").

## Usage Guidelines

-   **Determinate**: Used when completion time is known (e.g., File Upload: 45%).
-   **Indeterminate**: Used when completion time is unknown (e.g., "Scanning..."). Use a striped or pulsating animation.
-   **Placement**: Top of a modal, or inline within a list item.

## Code Example

```html
<div class="progress-wrapper">
  <div class="progress-label">Uploading image.jpg</div>
  <div class="progress-track" role="progressbar" aria-valuenow="45" aria-valuemin="0" aria-valuemax="100">
    <div class="progress-fill" style="width: 45%"></div>
  </div>
  <div class="progress-percent">45%</div>
</div>
```

```css
.progress-wrapper {
  margin-bottom: 16px;
}

.progress-label {
  font-size: 14px;
  color: #6c757d;
  margin-bottom: 4px;
}

.progress-track {
  height: 8px;
  background-color: #e9ecef;
  border-radius: 4px;
  overflow: hidden;
}

.progress-fill {
  height: 100%;
  background-color: #007bff;
  transition: width 0.3s ease;
}

.progress-percent {
  text-align: right;
  font-size: 12px;
  color: #6c757d;
  margin-top: 2px;
}
```

## Accessibility (ARIA)
-   `role="progressbar"`: Semantic role.
-   `aria-valuenow`, `aria-valuemin`, `aria-valuemax`: Required attributes.
-   `aria-label`: If no visible label exists.

---

[Back to Component Library](../README.md#3-component-library)
