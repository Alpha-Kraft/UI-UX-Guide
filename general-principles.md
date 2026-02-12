# General Principles

This document outlines the foundational UI/UX rules that apply across all platforms (Web, Mobile, Desktop). These principles ensure a consistent, professional, and accessible user experience.

## 1. Color Palette

Our color strategy is **professional, subtle, and functional**. We avoid overly saturated or "punchy" colors.

### Core Philosophy: The 60-30-10 Rule
-   **60% Neutral**: Backgrounds, surfaces (White, Off-white, Light Gray).
-   **30% Secondary**: Borders, dividers, subtle backgrounds (Medium Gray, Slate).
-   **10% Primary**: Actions, highlights, focus states (Deep Blue, Forest Green, Charcoal).

### Professional Palette Examples

| Usage | Color Name | Hex Code | Description |
| :--- | :--- | :--- | :--- |
| **Primary Action** | Corporate Blue | `#0056b3` | Primary buttons, links, active states. |
| **Secondary Action** | Slate Gray | `#6c757d` | Secondary buttons, less important text. |
| **Background** | Clean White | `#ffffff` | Main content background. |
| **Surface** | Light Gray | `#f8f9fa` | Card backgrounds, sidebars. |
| **Text Primary** | Dark Charcoal | `#212529` | Headings, body text (high contrast). |
| **Text Secondary** | Muted Gray | `#495057` | Metadata, hints (medium contrast). |
| **Error** | Muted Red | `#dc3545` | Validation errors (avoid neon red). |
| **Success** | Muted Green | `#28a745` | Success messages (avoid neon green). |

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

---

[Next: Web UI/UX Guidelines](./web-ui-ux.md) | [Back to Home](./README.md)
