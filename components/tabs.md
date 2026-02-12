# Tabs

Tabs organize related content into parallel sections within the same context.

## Anatomy

1.  **Tab Bar**: The container for all tabs. Can be top-aligned (default) or left/right (vertical).
2.  **Tab Button**: The interactive element. Shows the label and state (Active/Inactive).
3.  **Active Indicator**: A visual cue (e.g., underline, pill, background color) showing the current tab.
4.  **Content Pane**: The area displaying the content associated with the active tab.

## Usage Guidelines

-   **Scope**: Use tabs to switch between views of the same object (e.g., User Profile: Info | Settings | Activity).
-   **Limit**: Keep tabs to 2-7 items. If more, use a dropdown or sidebar.
-   **Content**: Content in tabs should be related. Don't mix unrelated workflows.
-   **Persistence**: Ideally, remember the last active tab if the user navigates away and returns.

## Code Example (HTML/CSS)

```html
<div class="tabs-container">
  <div role="tablist" aria-label="Settings Tabs">
    <button
      role="tab"
      aria-selected="true"
      aria-controls="panel-1"
      id="tab-1"
      class="tab-btn active"
    >
      Account
    </button>
    <button
      role="tab"
      aria-selected="false"
      aria-controls="panel-2"
      id="tab-2"
      class="tab-btn"
    >
      Notifications
    </button>
    <button
      role="tab"
      aria-selected="false"
      aria-controls="panel-3"
      id="tab-3"
      class="tab-btn"
    >
      Billing
    </button>
  </div>

  <div id="panel-1" role="tabpanel" aria-labelledby="tab-1" class="tab-panel active">
    <!-- Account Content -->
  </div>
  <div id="panel-2" role="tabpanel" aria-labelledby="tab-2" class="tab-panel hidden">
    <!-- Notifications Content -->
  </div>
  <!-- ... -->
</div>
```

```css
.tabs-container {
  border-bottom: 1px solid #dee2e6;
  margin-bottom: 24px;
}

.tablist {
  display: flex;
  gap: 24px;
}

.tab-btn {
  background: none;
  border: none;
  border-bottom: 3px solid transparent;
  padding: 12px 16px;
  font-size: 16px;
  color: #6c757d;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.2s ease;
}

.tab-btn:hover {
  color: #495057;
  background-color: #f8f9fa;
}

.tab-btn.active {
  color: #0056b3; /* Primary Color */
  border-bottom-color: #0056b3; /* Active Indicator */
}

.tab-panel.hidden { display: none; }
.tab-panel.active { display: block; animation: fadeIn 0.2s; }

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}
```

## Accessibility (ARIA)
-   `role="tablist"`: Container.
-   `role="tab"`: Individual tab buttons.
-   `role="tabpanel"`: The content area.
-   `aria-controls`: Links tab to panel ID.
-   `aria-selected`: Indicates active state.
-   **Keyboard Support**: Users should be able to navigate tabs with Arrow keys (Left/Right) and activate with Enter/Space.

---

[Back to Component Library](../README.md#3-component-library)
