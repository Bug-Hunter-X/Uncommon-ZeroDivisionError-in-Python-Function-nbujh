# Uncommon ZeroDivisionError in Python
This repository demonstrates a subtle edge case that can lead to a `ZeroDivisionError` in a Python function. The error is not immediately obvious and highlights the importance of comprehensive error handling and testing.

## Bug Description
The function `function_with_uncommon_error` is designed to return `b` if `a` is 0, `a` if `b` is 0, and `a / b` otherwise. However, the condition only checks if `a` OR `b` is zero which means if both inputs are zero, the function goes to the `else` statement and causes an error.  This represents an uncommon error scenario that might not be immediately apparent in standard testing.

## Solution
The solution involves adding an explicit check for both `a` and `b` being zero to handle the edge case appropriately.