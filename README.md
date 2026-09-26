    # Lab 02: Asymptotic Analysis and Algorithm Running Times

    Work with your Project 1 team to complete the exercises found in `exercises.pdf`. Put your solutions and explanations below. When you are finished, commit and push your repo.

    # Part 1:

    ## Problem 1.1
    1. 3n² is O(n²) by **Reflexivity** (dropping constant 3).
    2. 15n is O(n) by **Reflexivity** (dropping constant 15).
    3. n is O(n²) by **Polynomial degree grows faster** (1 < 2).
    4. 15n is O(n²) by **Transitivity** (from steps 2 and 3).
    5. 100 is O(1) by **Reflexivity**.
    6. 100 is O(n²) by **Polynomial degree grows faster** (0 < 2) and **Transitivity**.
    7. 3n² + 15n + 100 is O(max(n², n², n²)) = O(n²) by the **Summation Rule** (Summing is a max).

    ## Problem 1.2
    1. 2ⁿ is O(2ⁿ) by **Reflexivity**.
    2. 4 · 2ⁿ is O(2ⁿ) by **Dropping multiplicative constants** (applied to step 1).
    3. n⁵ is O(2ⁿ) by **Exp is faster than polynomial**.
    4. 8n⁵ is O(n⁵) by **Reflexivity** (dropping constant 8).
    5. 8n⁵ is O(2ⁿ) by **Transitivity** (from steps 3 and 4).
    6. 4 · 2ⁿ + 8n⁵ is O(max(2ⁿ, 2ⁿ)) = O(2ⁿ) by the **Summation Rule** (Summing is a max).



    # Part 2:

    ## Algorithm A
    1. **Exact Worst-Case Step Count T(n):**
   * `count = 0`: 1 step
   * `for i = 1 to n:` outer loop runs n times:
     * `print(i)`: executed n times (n steps)
     * `for j = 1 to n:` middle loop runs n × n = n² times
     * `for k = 1 to n:` inner loop runs n × n × n = n³ times:
       * `count = count + 1`: executed n³ times (n³ steps)
   * `return count`: 1 step

   **T(n) = n³ + n + 2**

2. **Tightest Big-O Bound:**
   **O(n³)**

    ## Algorithm B
    1. **Exact Worst-Case Step Count T(n):**
   * `val = n`: 1 step
   * `steps = 0`: 1 step
   * The loop condition `while val >= 1` runs m = ⌊log₂(n)⌋ + 1 times. Inside the loop:
     * `val = val / 2`: m steps
     * `steps = steps + 1`: m steps
     * `print("Processing steps: ", steps)`: m steps
   * Total loop body operations: 3m = 3(⌊log₂(n)⌋ + 1) steps.

   **T(n) = 3⌊log₂(n)⌋ + 5**

2. **Tightest Big-O Bound:**
   **O(log n)**


    # Part 3:



    ## Reflection
    * **Which Big-O rule feels the least intuitive?**
  Dropping multiplicative constants feels the least intuitive at first because constants significantly affect real-world execution speeds for smaller values of n, even though they do not change asymptotic growth.

* **Challenging parts:**
  Writing out the line-by-line formal proofs in Part 1 was the most challenging part, as it required justifying every step explicitly using only the specific rules provided rather than making standard mathematical jumps.

* **Feedback about the class:**
  The tracing hint in Part 2 was very helpful for visualizing how halving n on every iteration connects directly to base-2 logarithmic growth.


