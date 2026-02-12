# Accordions

Accordions allow users to toggle the visibility of content sections, saving vertical space.

## Anatomy

1.  **Header**: The clickable area containing the title and expansion indicator.
2.  **Title**: Descriptive label for the section.
3.  **Icon (Chevron)**: Indicates the state (expanded/collapsed). Usually rotates 180 degrees.
4.  **Panel**: The content area revealed upon expansion.

## Usage Guidelines

-   **When to Use**:
    -   Organizing complex settings.
    -   FAQs (Frequently Asked Questions).
    -   Mobile menus where vertical space is premium.
-   **Behavior**:
    -   *Single Expand*: Only one section open at a time (standard for FAQs).
    -   *Multi Expand*: Multiple sections open simultaneously (standard for filters).

## Code Example

```html
<div class="accordion">
  <div class="accordion-item">
    <button class="accordion-header" aria-expanded="false" aria-controls="sect1">
      <span>Section 1</span>
      <span class="icon">▼</span>
    </button>
    <div id="sect1" class="accordion-panel" hidden>
      <p>Content for section 1.</p>
    </div>
  </div>

  <div class="accordion-item">
    <button class="accordion-header" aria-expanded="false" aria-controls="sect2">
      <span>Section 2</span>
      <span class="icon">▼</span>
    </button>
    <div id="sect2" class="accordion-panel" hidden>
      <p>Content for section 2.</p>
    </div>
  </div>
</div>
```

```css
.accordion-item {
  border-bottom: 1px solid #e9ecef;
}

.accordion-header {
  width: 100%;
  display: flex;
  justify-content: space-between;
  padding: 16px;
  background: none;
  border: none;
  font-weight: 600;
  cursor: pointer;
}

.accordion-panel {
  padding: 0 16px 16px;
}
```

## Accessibility (ARIA)
-   `aria-expanded="true/false"`: Toggle this on click.
-   `aria-controls="ID"`: Links header to panel.
-   `hidden`: Attribute to hide content (remove it to show).

---

[Back to Component Library](../README.md#3-component-library)
