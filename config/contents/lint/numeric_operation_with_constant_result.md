Certain numeric operations have a constant result, usually 0 or 1.
Subtracting a number from itself or multiplying it by 0 will always return 0.
Additionally, a variable modulo 0 or itself will always return 0.
Dividing a number by itself or raising it to the power of 0 will always return 1.
As such, they can be replaced with that result.
These are probably leftover from debugging, or are mistakes.
Other numeric operations that are similarly leftover from debugging or mistakes
are handled by Lint/UselessNumericOperation.

### Example:

    # bad
    x - x
    x * 0
    x % 1
    x % x

    # good
    0

    # bad
    x -= x
    x *= 0
    x %= 1
    x %= x

    # good
    x = 0

    # bad
    x / x
    x ** 0

    # good
    1

    # bad
    x /= x
    x **= 0

    # good
    x = 1
