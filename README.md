# PHP Foreach Loop Pass-by-Reference Issue

This repository demonstrates a common, yet subtle, error in PHP related to how foreach loops handle references.  When using pass-by-reference within a foreach loop, modifications to elements can have unintended consequences if not carefully managed. The `bug.php` file showcases the problem, while `bugSolution.php` offers a corrected approach.

The core issue stems from the `&` (ampersand) in the `foreach` loop's declaration (`foreach ($data as &$value)`). This creates a reference, meaning any change made to `$value` directly affects the original array element. In the example, the intention is to lowercase only string values, but the numerical value is inadvertently converted to a string.

The solution demonstrates how to avoid this problem.