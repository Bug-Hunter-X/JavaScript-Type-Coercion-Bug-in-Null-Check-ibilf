# JavaScript Type Coercion Bug

This repository demonstrates a subtle bug in JavaScript related to type coercion and null checks. The `foo` function is intended to return `null` if either input `a` or `b` is `null`. However, it doesn't correctly handle cases where a falsy value (other than `null`) is passed as an argument.  This example highlights the importance of carefully considering type coercion when working with JavaScript's loose typing system.

## Bug

The `bug.js` file contains the buggy code.  The issue lies in the use of strict equality (`===`) in the conditional statement.  While this correctly identifies `null`, it doesn't account for other falsy values that might be considered equivalent to `null` in a less strict comparison.

## Solution

The `bugSolution.js` file provides a corrected version of the function.  The solution demonstrates better handling of potentially falsy values.  Instead of relying solely on strict equality, it explicitly checks for both `null` and `undefined` values.