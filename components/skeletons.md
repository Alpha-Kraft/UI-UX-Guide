# Skeletons (Loading States)

Skeletons are placeholders that mimic the layout of content while it loads, reducing perceived wait time.

## Anatomy

1.  **Block**: Rectangular shape representing text or images.
2.  **Animation**: Subtle pulse or shimmer effect indicating activity.
3.  **Color**: Usually light gray (`#e9ecef`) with a slightly lighter/darker animation.

## Usage Guidelines

-   **When to Use**:
    -   Initial page load.
    -   Large data fetches (e.g., Table rows).
-   **When NOT to Use**:
    -   Short operations (< 300ms).
    -   Background processes.
-   **Structure**: Match the layout of the loaded content (e.g., Avatar circle + 2 lines of text).

## Code Example

```html
<div class="skeleton-card" aria-busy="true" aria-label="Loading content...">
  <div class="skeleton skeleton-img"></div>
  <div class="skeleton skeleton-title"></div>
  <div class="skeleton skeleton-text"></div>
  <div class="skeleton skeleton-text short"></div>
</div>
```

```css
.skeleton-card {
  padding: 16px;
  border: 1px solid #e9ecef;
  border-radius: 8px;
  background: white;
}

.skeleton {
  background-color: #e9ecef;
  border-radius: 4px;
  margin-bottom: 8px;
  position: relative;
  overflow: hidden;
}

/* Shimmer Animation */
.skeleton::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.5),
    transparent
  );
  transform: translateX(-100%);
  animation: shimmer 1.5s infinite;
}

@keyframes shimmer {
  100% { transform: translateX(100%); }
}

.skeleton-img { width: 100%; height: 150px; border-radius: 8px; margin-bottom: 12px; }
.skeleton-title { width: 60%; height: 24px; margin-bottom: 12px; }
.skeleton-text { width: 100%; height: 16px; }
.skeleton-text.short { width: 80%; }
```

## Accessibility (ARIA)
-   `aria-busy="true"`: Indicates content is loading.
-   `aria-label="Loading..."`: Provides context to screen readers.
-   Ensure focus management returns to the content once loaded.

---

[Back to Component Library](../README.md#3-component-library)
