# CSS Positions

> CSS positions are used to control the layout of an HTML element. There are five types of positions in CSS: `static`, `relative`, `fixed`, `absolute` or `sticky`

### 1. Static Positioning

- This is the default position of an element.
- The element will be positioned according to the normal flow of the document.
- The `top`, `right`, `bottom`, and `left` properties do not apply to statically positioned elements.

### 2. Relative Positioning

- The element with `position: relative;` is positioned relative to its normal position.
- The `top`, `right`, `bottom`, and `left` properties can be used to adjusted away from its normal position.
- The element will still occupy the space of its normal position.
- Other content _will not be adjusted_ to fit into any gap left by the element.

### 3. Absolute Positioning

- The element is positioned relative to its nearest positioned ancestor.
- The element is removed from the normal document flow.
- a positioned ancestor is any element with a position value besides static, the default.
- The `top`, `right`, `bottom`, and `left` properties can be used to position the element.
- If the element has no positioned ancestors, it will be positioned relative to the initial containing block.

### 4. Fixed Positioning

- The element is positioned relative to the `viewport`,which means it always stays in the same place even if the page is scrolled.
- The element is removed from the normal document flow.
- The `top`, `right`, `bottom`, and `left` properties can be used to position the element.
- The element will stay in the same position even when the user scrolls.

### 5. Sticky Positioning

- An element with `position: sticky;` is positioned based on the user's scroll position.
- A sticky element toggles between `relative` and `fixed`, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "_sticks_" in place (like position:fixed).

### All CSS Positioning Properties

| Property | Description |
| --- | --- |
| bottom | Sets the bottom margin edge for a positioned box |
| clip | Clips an absolutely positioned element |
| left | Sets the left margin edge for a positioned box |
| position | Specifies the type of positioning for an element |
| right | Sets the right margin edge for a positioned box |
| top | Sets the top margin edge for a positioned box |

### Comparison of Positions

| Position | Relative to | Normal Flow | Top/Right/Bottom/Left | Ancestor |
| --- | --- | --- | --- | --- |
| Static | Normal Position | Yes | N/A | N/A |
| Relative | Normal Position | Yes | (auto) | N/A |
| Absolute | Nearest Positioned Ancestor | No | (auto) | Nearest Positioned Ancestor |
| Fixed | Viewport | No | (auto) | N/A |
| Sticky | Nearest Positioned Ancestor | Yes | (auto) | Nearest Positioned Ancestor |

### Learn More

For more information about CSS Positions, visit: 
> - [Best Example](https://blog.hubspot.com/website/css-position)
> - [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units).
> - [YouTube](https://www.youtube.com/watch?v=Wa3kvQusRUc&list=PLfEr2kn3s-br9ZFmejfLhAgMbGgbpdof8&index=23)