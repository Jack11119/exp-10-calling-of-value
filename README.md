
1. **Start.**

2. **Initialize variables.**
   Set `a = 5`, `b = 2`.

3. **Call the swap function with addresses.**
   Execute `swap(&a, &b)`.

   * Inside the call: `x` points to `a`, `y` points to `b`.

4. **Inside `swap(int *x, int *y)`:**

   1. `temp = *x`

      * Store the value at address `x` (current value of `a`, i.e., 5) into `temp`.
   2. `*x = *y`

      * Write the value at address `y` (current value of `b`, i.e., 2) into the location pointed to by `x` (so `a` becomes 2).
   3. `*y = temp`

      * Write `temp` (5) into the location pointed to by `y` (so `b` becomes 5).
   4. **Return** to `main`.

5. **After return to `main`:**

   * `a` now holds `2`, `b` now holds `5`.

6. **Output results.**
   Print:

   * `value of a is: 2`
   * `value of b  is: 5`

7. **End.**

**Why this works:** Passing `&a` and `&b` gives the function direct access to the original variables via pointers, so changing `*x` and `*y` modifies `a` and `b` in place.
