# Steps (Stepper)

Steps visualize linear progress through a multi-screen process (e.g., checkout, survey).

## Anatomy

1.  **Step Indicator**: Circle with number or checkmark.
2.  **Label**: Title of the step (e.g., "Shipping").
3.  **Connector**: Line linking steps.
4.  **State**:
    -   *Active*: Current step (highlighted).
    -   *Completed*: Past steps (green check).
    -   *Pending*: Future steps (grayed out).

## Usage Guidelines

-   **When to Use**: Wizard-like flows with 3-7 steps.
-   **Navigation**: Users should generally complete steps in order, but may be able to click back to edit previous steps.

## Code Example

```html
<ol class="stepper">
  <li class="step completed">
    <span class="step-icon">✔</span>
    <span class="step-label">Cart</span>
  </li>
  <li class="step active" aria-current="step">
    <span class="step-icon">2</span>
    <span class="step-label">Shipping</span>
  </li>
  <li class="step">
    <span class="step-icon">3</span>
    <span class="step-label">Payment</span>
  </li>
</ol>
```

```css
.stepper {
  display: flex;
  justify-content: space-between;
  list-style: none;
  padding: 0;
  max-width: 600px;
  margin: 0 auto 32px;
}

.step {
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  flex: 1;
}

.step::after {
  content: "";
  position: absolute;
  top: 12px;
  left: 50%;
  width: 100%;
  height: 2px;
  background-color: #dee2e6;
  z-index: -1;
}

.step:last-child::after { display: none; }

.step.completed::after { background-color: #28a745; }

.step-icon {
  width: 24px;
  height: 24px;
  border-radius: 50%;
  background-color: #dee2e6;
  color: #6c757d;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 12px;
  font-weight: bold;
}

.step.active .step-icon {
  background-color: #0056b3;
  color: white;
}

.step.completed .step-icon {
  background-color: #28a745;
  color: white;
}

.step-label {
  margin-top: 8px;
  font-size: 14px;
  color: #6c757d;
}

.step.active .step-label { color: #0056b3; font-weight: 600; }
```

## Accessibility (ARIA)
-   `aria-current="step"`: Indicates the current step.

---

[Back to Component Library](../README.md#3-component-library)
