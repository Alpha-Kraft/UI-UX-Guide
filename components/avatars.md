# Avatars

Avatars represent users, groups, or entities with an image or initials.

## Anatomy

1.  **Image**: Circular crop of a photo.
2.  **Fallback**: Initials (e.g., "JD") or generic icon if no image.
3.  **Status Indicator (Optional)**: Small dot for online/offline status.

## Usage Guidelines

-   **Sizes**:
    -   *Small (24px)*: Lists, comments.
    -   *Medium (40px)*: Top navigation, headers.
    -   *Large (64px+)*: User profiles.
-   **Shape**: Use circles for people, squares (with rounded corners) for organizations/apps.
-   **Background**: Use a contrasting color for fallback initials (e.g., hash of username).

## Code Example

```html
<div class="avatar-group">
  <!-- Image Avatar -->
  <div class="avatar">
    <img src="user.jpg" alt="Jane Doe">
    <span class="status online"></span>
  </div>

  <!-- Initials Fallback -->
  <div class="avatar fallback" aria-label="John Smith">JS</div>
</div>
```

```css
.avatar {
  position: relative;
  display: inline-block;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  overflow: hidden;
  background-color: #e9ecef;
}

.avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.avatar.fallback {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #0056b3;
  color: white;
  font-weight: 600;
  font-size: 14px;
}

.status {
  position: absolute;
  bottom: 0;
  right: 0;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  border: 2px solid white;
}

.status.online { background-color: #28a745; }
.status.offline { background-color: #6c757d; }
```

## Accessibility (ARIA)
-   `alt="Name"`: Describe the person shown.
-   `aria-label="Name"`: Use for initial fallbacks.

---

[Back to Component Library](../README.md#3-component-library)
