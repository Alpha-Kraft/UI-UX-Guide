# Mobile UI/UX Guidelines

Mobile interfaces demand a focus on touch interaction, limited screen real estate, and platform conventions.

## 1. Touch Targets

Fingers are less precise than mouse cursors.

-   **Minimum Size**: Interactive elements must be at least **44x44 points (iOS)** or **48x48 dp (Android)**.
-   **Spacing**: Ensure adequate spacing (minimum 8px) between touch targets to prevent accidental taps.

## 2. Navigation Patterns

Mobile navigation differs significantly from web and desktop.

### Primary Navigation
-   **Bottom Navigation Bar**: Best for top-level views (3-5 items).
    -   *iOS*: Translucent, labeled icons.
    -   *Android*: Labeled icons, shifting behavior if > 3 items (Material Design).
-   **Tabs**: Used for segemented content within a view.

### Secondary Navigation
-   **Navigation Drawer (Hamburger Menu)**: Use sparingly. Prefer bottom navigation for primary tasks. Drawers are better for settings or less frequent actions.
-   **Back Navigation**:
    -   *iOS*: Top-left back button with label of previous screen. Swipe from left edge.
    -   *Android*: Top-left arrow (Up button) or system Back button/gesture.

## 3. Gestures

Gestures should feel natural and provide immediate feedback.

-   **Tap**: Primary action.
-   **Long Press**: Context menu or selection mode.
-   **Swipe**: Navigation (back/forward), list actions (delete/archive), or carousel scrolling.
-   **Pinch**: Zooming content (maps, images).

**Rule**: Do not rely *solely* on complex gestures for critical actions. Provide a visible alternative (e.g., a delete button in addition to swipe-to-delete).

## 4. Platform Conventions (iOS vs. Android)

Respect the platform to make the app feel native and professional.

| Feature | iOS (Human Interface Guidelines) | Android (Material Design) |
| :--- | :--- | :--- |
| **Typography** | San Francisco (SF Pro) | Roboto |
| **Icons** | Thin strokes, outlined or filled. | Filled, geometric shapes. |
| **Dialogs** | Center-aligned, rounded corners. | Center-aligned, slightly sharper corners. |
| **Shadows** | Soft, diffused shadows. | Elevation-based shadows (depth). |
| **Toggles** | Switches (Green when active). | Switches (Accent color when active). |

## 5. One-Handed Use

Design for how people hold their phones.
-   **Reachability**: Place primary actions in the bottom half of the screen (the "Thumb Zone").
-   **destructive Actions**: Place destructive actions (Delete, Sign Out) away from primary interaction areas to prevent accidental taps.

## 6. Feedback & Haptics

-   **Visual Feedback**: Instant color change or ripple effect on tap.
-   **Haptic Feedback**: Use subtle vibrations for confirmation of significant actions (e.g., success, error, long press).

---

[Next: Desktop UI/UX Guidelines](./desktop-ui-ux.md) | [Back to Home](./README.md)
