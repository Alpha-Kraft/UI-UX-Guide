# Modals (Dialogs)

Modals are critical overlays that demand user attention for a specific task.

## Anatomy

1.  **Overlay/Backdrop**: A semi-transparent dark layer behind the modal to de-emphasize the background.
2.  **Container**: The box containing the modal content.
3.  **Title**: Clear header describing the task (e.g., "Delete User").
4.  **Content**: The message or form fields.
5.  **Actions**: Buttons (usually "Cancel" and a Primary Action) at the bottom.
6.  **Close Button**: An "X" icon in the top-right corner.

## Design Guidelines

-   **Focus**: When a modal opens, focus must move to the first interactive element inside it.
-   **Trapping**: Keyboard users (Tab) should be "trapped" inside the modal until it is closed. They should not be able to tab to the background page.
-   **Closing**: Allow closing via:
    -   Clicking the backdrop.
    -   Clicking the "X" button.
    -   Clicking the "Cancel" button.
    -   Pressing the `Esc` key.

## Code Example

```html
<div class="modal-backdrop" role="presentation">
  <div
    class="modal-container"
    role="dialog"
    aria-labelledby="modal-title"
    aria-modal="true"
  >
    <div class="modal-header">
      <h2 id="modal-title">Confirm Deletion</h2>
      <button class="close-btn" aria-label="Close modal">&times;</button>
    </div>

    <div class="modal-body">
      <p>Are you sure you want to delete this item? This action cannot be undone.</p>
    </div>

    <div class="modal-footer">
      <button class="btn btn-secondary">Cancel</button>
      <button class="btn btn-danger">Delete</button>
    </div>
  </div>
</div>
```

```css
.modal-backdrop {
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-container {
  background-color: white;
  border-radius: 8px;
  width: 100%;
  max-width: 500px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
  animation: slideDown 0.2s ease-out;
}

@keyframes slideDown {
  from { transform: translateY(-20px); opacity: 0; }
  to { transform: translateY(0); opacity: 1; }
}

.modal-header, .modal-footer {
  padding: 16px 24px;
}

.modal-body {
  padding: 0 24px;
}
```

## Accessibility (ARIA)
-   `role="dialog"`: Tells screen readers this is a dialog.
-   `aria-modal="true"`: Tells assistive technology that background content is inert.
-   `aria-labelledby`: Points to the ID of the title element.

---

[Back to Component Library](../README.md#3-component-library)
