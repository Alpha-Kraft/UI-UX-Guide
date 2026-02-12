# Toasts (Snackbars)

Toasts are non-blocking notifications that provide brief feedback about an operation.

## Anatomy

1.  **Container**: Small, rectangular surface.
2.  **Icon (Optional)**: Indicates the type (Success checkmark, Info 'i', Error '!').
3.  **Message**: Concise text (e.g., "File saved").
4.  **Action (Optional)**: A single text button (e.g., "Undo").
5.  **Close Button**: An "X" to dismiss early.

## Usage Guidelines

-   **Placement**:
    -   *Desktop*: Top-right corner (stacking vertically).
    -   *Mobile*: Bottom-center (floating above navigation).
-   **Timing**:
    -   *Auto-Dismiss*: 4-5 seconds for short messages.
    -   *Persistent*: If the message contains an Action (like "Undo"), it can stay longer (7-10s) or until interaction.
-   **Do Not Use**: For critical errors that require user intervention (use a Modal).

## Code Example (CSS)

```css
.toast-container {
  position: fixed;
  top: 24px;
  right: 24px;
  z-index: 2000;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.toast {
  background-color: #323232; /* Dark background for high contrast */
  color: white;
  padding: 12px 16px;
  border-radius: 4px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
  display: flex;
  align-items: center;
  gap: 12px;
  min-width: 280px;
  animation: slideIn 0.3s ease-out;
}

.toast-success { border-left: 4px solid #28a745; }
.toast-error { border-left: 4px solid #dc3545; }

.toast-action {
  margin-left: auto;
  background: none;
  border: none;
  color: #4da3ff; /* Accent color */
  font-weight: 600;
  cursor: pointer;
  padding: 0 8px;
}

@keyframes slideIn {
  from { transform: translateX(100%); opacity: 0; }
  to { transform: translateX(0); opacity: 1; }
}
```

## Accessibility (ARIA)
-   `role="status"`: For non-critical updates (polite announcement).
-   `role="alert"`: For critical errors (assertive announcement).
-   Ensure the toast is reachable via keyboard if it contains an action.

---

[Back to Component Library](../README.md#3-component-library)
