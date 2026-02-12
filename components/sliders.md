# Sliders

Sliders allow users to select a value (or range) from a continuous or discrete set.

## Anatomy

1.  **Track**: Represents the full range (min to max).
2.  **Thumb**: The handle used to select a value.
3.  **Fill**: The colored portion of the track indicating the selected value.
4.  **Ticks (Optional)**: Indicators for specific steps.
5.  **Labels**: Min, Max, and Current Value.

## Usage Guidelines

-   **When to Use**:
    -   Selecting a value where precision is less important (e.g., Volume, Brightness).
    -   Selecting a price range (e.g., $0 - $1000).
-   **When NOT to Use**:
    -   Selecting exact values (e.g., "Quantity: 5"). Use a number input.

## Code Example

```html
<label for="volume">Volume: <span id="volume-val">50%</span></label>
<input
  type="range"
  id="volume"
  name="volume"
  min="0"
  max="100"
  value="50"
  oninput="document.getElementById('volume-val').innerText = this.value + '%'"
>
```

```css
input[type=range] {
  -webkit-appearance: none;
  width: 100%;
  height: 8px;
  background: #dee2e6;
  outline: none;
  border-radius: 4px;
}

input[type=range]::-webkit-slider-thumb {
  -webkit-appearance: none;
  appearance: none;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  background: #0056b3;
  cursor: pointer;
  box-shadow: 0 2px 4px rgba(0,0,0,0.2);
}

input[type=range]::-moz-range-thumb {
  width: 20px;
  height: 20px;
  border-radius: 50%;
  background: #0056b3;
  cursor: pointer;
}
```

## Accessibility (ARIA)
-   `role="slider"`: Semantic role.
-   `aria-valuemin`, `aria-valuemax`, `aria-valuenow`: Required attributes.
-   Ensure keyboard users can adjust the slider using Arrow keys.

---

[Back to Component Library](../README.md#3-component-library)
