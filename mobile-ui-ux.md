# Mobile UI/UX Guidelines

Mobile interfaces demand a focus on touch interaction, limited screen real estate, and platform conventions.

## 1. Touch Targets & Safe Areas

Fingers are less precise than mouse cursors.

-   **Minimum Size**: Interactive elements must be at least **44x44 points (iOS)** or **48x48 dp (Android)**.
-   **Spacing**: Ensure adequate spacing (minimum 8px) between touch targets.
-   **Safe Areas**: Respect the "Safe Area" defined by the OS (avoiding the notch at the top and the home indicator at the bottom). Content should not be clipped by rounded corners.

## 2. Navigation Patterns

Mobile navigation differs significantly from web and desktop.

### Primary Navigation
-   **Bottom Navigation Bar**: Best for top-level views (3-5 items).
    -   *iOS*: Translucent, labeled icons.
    -   *Android*: Labeled icons, shifting behavior if > 3 items.
-   **Tabs**: Used for segemented content within a view.

### Secondary Navigation
-   **Navigation Drawer**: Use sparingly. Drawers are hidden by default, lowering discoverability.
-   **Back Navigation**:
    -   *iOS*: Top-left back button + Swipe from left edge.
    -   *Android*: Top-left arrow + System Back button/gesture.

## 3. Native Components (iOS vs Android)

Respect platform conventions to make the app feel native.

| Component | iOS (UIKit/SwiftUI) | Android (Material Design) |
| :--- | :--- | :--- |
| **Pickers** | "Wheel" picker at bottom of screen. | Dropdown menu or full-screen dialog. |
| **Action Sheet** | Slides up from bottom. | Bottom Sheet (modal or persistent). |
| **Alerts** | Center modal, rounded, minimal. | Center modal, slightly sharper, clearer elevation. |
| **Toggles** | Green switch. | Accent-colored switch. |
| **Tabs** | Segmented Control (pill shape). | Text tabs with underline indicator. |

## 4. Gestures

Gestures should feel natural and provide immediate feedback.

-   **Tap**: Primary action.
-   **Swipe**: Navigation (back/forward) or list actions.
    -   *Threshold*: A swipe must travel > 50% of width to commit, or be fast (high velocity).
-   **Pull-to-Refresh**: Standard gesture for reloading lists.

**Rule**: Do not rely *solely* on complex gestures. Provide visible buttons for accessibility.

## 5. One-Handed Use

Design for how people hold their phones.
-   **The Thumb Zone**: The bottom 1/3 of the screen is the easiest to reach. Place primary actions (FABs, Submit buttons) here.
-   **Destructive Actions**: Place Delete/Sign Out buttons at the top or in a secondary menu to prevent accidental taps.

## 6. Feedback & Haptics

-   **Visual Feedback**: Instant color change (ripple on Android, opacity drop on iOS) on tap.
-   **Haptic Feedback**: Use subtle vibrations (Taptic Engine) for success, error, or selection changes.

---

[Next: Desktop UI/UX Guidelines](./desktop-ui-ux.md) | [Back to Home](./README.md)
