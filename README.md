```markdown
# 100 Doors Problem

This project models the classic "100 Doors" puzzle, where you have 100 doors initially closed, and perform multiple passes to toggle their states. Only doors that are perfect squares remain open after all passes.

## Problem Description

- There are 100 doors in a row, all initially closed.
- You make 100 passes:
  - On the 1st pass, toggle every door.
  - On the 2nd pass, toggle every 2nd door.
  - On the 3rd pass, toggle every 3rd door.
  - Continue until the 100th pass, toggling only the 100th door.
- Determine which doors are open after the last pass.

## Solution Explanation

- Each door's final state depends on the number of divisors it has.
- Doors with an odd number of divisors (perfect squares) end up open.
- Doors with an even number of divisors (non-perfect squares) end up closed.

**Therefore, the open doors are perfect squares within 1 to 100:**

`1, 4, 9, 16, 25, 36, 49, 64, 81, 100`

## Implementation

The main function `getFinalOpenedDoors()` returns an array of the door numbers that are open after all passes.

```javascript
function getFinalOpenedDoors() {
  const openDoors = [];
  for (let i = 1; i <= 100; i++) {
    if (Number.isInteger(Math.sqrt(i))) {
      openDoors.push(i);
    }
  }
  return openDoors;
}
``

## Usage

Call the function to get the list of open doors:

```javascript
console.log(getFinalOpenedDoors());  // Output: [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
``

## License

This project is for educational purposes only.

---

Feel free to modify or extend this code!
