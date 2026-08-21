# Sample Solution

We know that $F(0) = 0$ and $F(1) = 1$, so we can define both base cases. It happens that we can detect and treat these cases together to reduce the amount of code that must be written and executed each time the function is called. To do this, if `n`{.python} is less than `2`{.python}, we return <code class="language-python"></code>n</code>. If this `return`{.python} statement is not executed, we can call the function recursively and add together the results.

```py-cell
def fibonacci(n):
    if n < 2:
        return n
    return fibonacci(n - 1) + fibonacci(n - 2)
```

# Step 3: Test the function

```py-cell
print(fibonacci(0))
print(fibonacci(1))
print(fibonacci(2))
print(fibonacci(8))
```

# Discussion

This recursive implementation of the Fibonacci function is elegant and directly follows the mathematical definition. However, as (while `n`{.python} is greater than `1`{.python}) it recursively calls itself twice, the number of function calls increases dramatically as `n`{.python} increases. This leads to an exponential tim  e complexity due to repeated calculations of the same Fibonacci numbers. For large values of `n`{.python}, this can be very slow. Alternative approaches allow for faster computation.
