# Breadcrumbs

Breadcrumbs show the user their current location within the site's hierarchy.

## Anatomy

1.  **Link**: Clickable text for parent pages.
2.  **Separator**: Visual divider (e.g., `>` or `/`).
3.  **Current Page**: The last item. Not clickable.

## Usage Guidelines

-   **When to Use**: Deep hierarchies (3+ levels). E-commerce product pages, documentation.
-   **Placement**: Top-left, below the main navigation.
-   **Truncation**: If the path is too long, collapse middle items with `...`.

## Code Example

```html
<nav aria-label="Breadcrumb">
  <ol class="breadcrumbs">
    <li><a href="/">Home</a></li>
    <li aria-hidden="true">/</li>
    <li><a href="/products">Products</a></li>
    <li aria-hidden="true">/</li>
    <li><span aria-current="page">Wireless Headphones</span></li>
  </ol>
</nav>
```

```css
.breadcrumbs {
  list-style: none;
  padding: 0;
  display: flex;
  align-items: center;
  font-size: 14px;
}

.breadcrumbs li {
  color: #6c757d;
}

.breadcrumbs a {
  color: #0056b3;
  text-decoration: none;
}

.breadcrumbs a:hover {
  text-decoration: underline;
}

.breadcrumbs li + li::before {
  content: "/";
  margin: 0 8px;
  color: #adb5bd;
}
```

## Accessibility (ARIA)
-   `nav aria-label="Breadcrumb"`: Identifies the navigation type.
-   `aria-current="page"`: Marks the current location.

---

[Back to Component Library](../README.md#3-component-library)
