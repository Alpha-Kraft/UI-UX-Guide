# General Principles

This document outlines the foundational UI/UX rules that apply across all platforms (Web, Mobile, Desktop). These principles ensure a consistent, professional, and accessible user experience.

## 1. Color Palette

Our color strategy is **professional, subtle, and functional**. We avoid overly saturated or "punchy" colors.

### Core Philosophy: The 60-30-10 Rule
-   **60% Neutral**: Backgrounds, surfaces (White, Off-white, Light Gray).
-   **30% Secondary**: Borders, dividers, subtle backgrounds (Medium Gray, Slate).
-   **10% Primary**: Actions, highlights, focus states (Deep Blue, Forest Green, Charcoal).

### Professional Palette Examples

| Usage | Color Name | Hex Code (Light) | Hex Code (Dark) | Description |
| :--- | :--- | :--- | :--- | :--- |
| **Primary Action** | Corporate Blue | `#0056b3` | `#4da3ff` | Primary buttons, links, active states. |
| **Secondary Action** | Slate Gray | `#6c757d` | `#aeb5bc` | Secondary buttons, less important text. |
| **Background** | Clean White | `#ffffff` | `#121212` | Main content background. |
| **Surface** | Light Gray | `#f8f9fa` | `#1e1e1e` | Card backgrounds, sidebars. |
| **Text Primary** | Dark Charcoal | `#212529` | `#e9ecef` | Headings, body text (high contrast). |
| **Text Secondary** | Muted Gray | `#495057` | `#adb5bd` | Metadata, hints (medium contrast). |
| **Error** | Muted Red | `#dc3545` | `#e57373` | Validation errors (avoid neon red). |
| **Success** | Muted Green | `#28a745` | `#81c784` | Success messages (avoid neon green). |

**Tip**: Always check contrast ratios. Primary text on white backgrounds should have a contrast ratio of at least 4.5:1.

## 2. Typography

We prioritize **readability and clarity**. Use modern sans-serif typefaces that work well on screens.

### Font Family
-   **Primary**: System San-Serif stack (San Francisco on macOS/iOS, Segoe UI on Windows, Roboto on Android).
    -   *Fallback*: Inter, Helvetica Neue, Arial.
-   **Monospace**: SF Mono, Consolas, Roboto Mono (for code snippets).

### Hierarchy & Scale
Establish a clear visual hierarchy using size and weight.

| Role | Size (px/rem) | Weight | Line Height |
| :--- | :--- | :--- | :--- |
| **H1 (Page Title)** | 32px / 2rem | Bold (700) | 1.2 |
| **H2 (Section)** | 24px / 1.5rem | Semi-Bold (600) | 1.3 |
| **H3 (Subsection)** | 20px / 1.25rem | Medium (500) | 1.4 |
| **Body Text** | 16px / 1rem | Regular (400) | 1.5 |
| **Small Text** | 14px / 0.875rem | Regular (400) | 1.5 |
| **Caption/Label** | 12px / 0.75rem | Medium (500) | 1.5 |

**Rule**: Never use more than 2 font families. Stick to one family with multiple weights if possible.

## 3. Spacing & Grid System

We use an **8-point grid system** to ensure consistent alignment and rhythm.

### The 8pt Rule
All spacing, margins, padding, and element dimensions should be multiples of 8 (e.g., 8px, 16px, 24px, 32px).
-   *Exception*: 4px is allowed for very tight spacing (icons inside buttons).

### Spacing Scale
-   **XS (4px)**: Tight grouping (icon + text).
-   **S (8px)**: Related elements (label + input).
-   **M (16px)**: Standard separation (between form fields).
-   **L (24px)**: Section separation.
-   **XL (32px)**: Large section breaks.
-   **XXL (48px+)**: Major layout divisions.

**Tip**: Consistent spacing creates a sense of order and professionalism. Avoid arbitrary values like 13px or 27px.

## 4. Accessibility (A11y)

Accessibility is not optional. A professional product is usable by everyone.

### Key Guidelines
1.  **Contrast**: Ensure all text meets WCAG AA standards (4.5:1 for normal text, 3:1 for large text).
2.  **Focus States**: Never remove outline styles on focusable elements without providing a clear alternative. Focus indicators should be visible and high-contrast.
3.  **Semantic HTML**: Use proper tags (`<button>`, `<a>`, `<input>`, `<label>`) for their intended purpose.
4.  **Alt Text**: All meaningful images must have descriptive `alt` text. Decorative images should have `alt=""`.

## 5. Dark Mode

Designing for dark mode requires more than just inverting colors.

-   **Elevation**: Use lighter grays (`#1e1e1e`, `#2c2c2c`) to indicate elevation (cards, modals) rather than shadows, which are less visible on dark backgrounds.
-   **Desaturation**: Avoid fully saturated colors. Bright blue on black causes eye strain. Use a desaturated blue (e.g., `#4da3ff` instead of `#0056b3`).
-   **Text**: Avoid pure white text (`#ffffff`) on pure black (`#000000`). Use off-white (`#e9ecef`) on dark gray (`#121212`) to reduce harsh contrast.

## 6. Iconography

Icons should be clear, metaphorical, and consistent.

-   **Stroke Weight**: Use a consistent stroke width (e.g., 1.5px or 2px) for all icons.
-   **Style**: Choose *either* outlined (more modern, airy) or filled (more solid, better for active states). Do not mix styles unless indicating state (e.g., heart outline = unliked, heart filled = liked).
-   **Optical Alignment**: Center icons optically, not just mathematically. Some shapes (triangles, circles) need to shift slightly to look centered.
-   **Size**: Standard icon sizes are 16px, 20px, 24px.

## 7. Motion & Animation

Motion should be purposeful, not decorative. It guides the user's attention and explains relationships between elements.

-   **Duration**:
    -   *Fast (100-200ms)*: Hover effects, toggles, button clicks.
    -   *Normal (200-300ms)*: Modals opening, dropdowns expanding.
    -   *Slow (300-500ms)*: Large page transitions.
-   **Easing**:
    -   *Ease-Out*: Use for entering elements (starts fast, slows down). Feels natural.
    -   *Ease-In*: Use for exiting elements (starts slow, speeds up).
    -   *Linear*: Use only for continuous loops (spinners).
-   **Purpose**: Use motion to show *continuity* (e.g., a card expanding into a detail view) or *feedback* (e.g., a shake animation for an invalid password).

## 8. Micro-Interactions

Micro-interactions are single-task based interactions that provide feedback and improve user experience.

-   **Definition**: Subtle animations or state changes responding to user input.
-   **Principles**:
    -   *Fast*: Feedback must be instant (< 100ms perception).
    -   *Subtle*: Should not distract from the main task.
    -   *Meaningful*: Must communicate status (e.g., a "loading" spinner inside a button after clicking "Save").
-   **Examples**:
    -   A "Like" button turning red and popping slightly.
    -   A toggle switch sliding from off to on.
    -   Input field border turning red on error.

## 9. UX Copywriting

Words are part of the design. The tone should be professional, concise, and human.

-   **Tone**: Helpful, direct, and polite. Avoid robotic language ("Invalid Input") or overly casual slang ("Whoopsie!").
-   **Clarity**: Use simple words. "Buy" is better than "Purchase". "Join" is better than "Register".
-   **Error Messages**:
    -   *Bad*: "Error 500."
    -   *Better*: "Something went wrong."
    -   *Best*: "We couldn't save your changes. Please check your connection and try again."
-   **Labels**: Be consistent. If you use "Sign In" on one page, don't use "Log In" on another.

---

[Next: Web UI/UX Guidelines](./web-ui-ux.md) | [Back to Home](./README.md)
