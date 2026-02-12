# Buttons

Buttons are the primary way users take action. They should be clear, concise, and indicate their purpose.

## Button Types

1.  **Primary**: The main action of a screen (e.g., "Submit", "Save", "Sign Up"). Use only one per view to guide focus.
2.  **Secondary**: Alternative actions (e.g., "Cancel", "Back"). Use muted colors or outlines.
3.  **Tertiary**: Subtle actions (e.g., "Read More", "Forgot Password"). Often look like links or text buttons.
4.  **Destructive**: Actions that cannot be easily undone (e.g., "Delete Account"). Use red or a warning color.

## Code Example (CSS)

```css
/* Base Button Styles */
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 10px 20px; /* 10px vertical, 20px horizontal */
  font-family: inherit;
  font-size: 16px;
  font-weight: 500;
  border-radius: 4px; /* Slight rounding, professional look */
  border: none;
  cursor: pointer;
  transition: all 0.2s ease-in-out;
  text-decoration: none;
}

/* Primary Button */
.btn-primary {
  background-color: #0056b3; /* Corporate Blue */
  color: #ffffff;
}

.btn-primary:hover {
  background-color: #004494;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.btn-primary:active {
  background-color: #003366;
  transform: translateY(1px);
}

/* Secondary Button */
.btn-secondary {
  background-color: #e9ecef; /* Light Gray */
  color: #212529; /* Dark Gray Text */
}

.btn-secondary:hover {
  background-color: #dee2e6;
}

/* Outline Button */
.btn-outline {
  background-color: transparent;
  border: 1px solid #6c757d;
  color: #6c757d;
}

.btn-outline:hover {
  background-color: #6c757d;
  color: #ffffff;
}

/* Destructive Button */
.btn-danger {
  background-color: #dc3545;
  color: white;
}
```

## Do's and Don'ts

-   **Do**: Use verbs for button labels (e.g., "Save Changes" instead of "Save").
-   **Do**: Ensure buttons have a minimum width (e.g., 100px) for touch targets on mobile.
-   **Don't**: Use generic labels like "Click Here" or "Go".
-   **Don't**: Have multiple primary buttons on a single screen.

---

[Back to Component Library](../README.md#3-component-library)
